
        const loveButton = document.getElementById('loveButton');
        const loveMessage = document.getElementById('loveMessage');
        const floatingContainer = document.getElementById('floatingContainer');

        loveButton.addEventListener('click', () => {
            loveMessage.classList.toggle('hidden');
        });

        // Generate 100 "I Love You" texts and 100 flower images
        for (let i = 0; i < 100; i++) {
            // Create "I Love You" text
            const floatingText = document.createElement('div');
            floatingText.classList.add('floating-text');
            floatingText.innerText = 'I Love You ❤️';
            floatingText.style.left = `${Math.random() * 100}vw`;
            floatingText.style.animationDelay = `${Math.random() * 10}s`;
            floatingText.style.color = getRandomColor();
            floatingContainer.appendChild(floatingText);

            // Create flower image
            const floatingFlower = document.createElement('img');
            floatingFlower.src = 'bunga.png'; // Ganti dengan path gambar mawar Anda
            floatingFlower.classList.add('floating-flower');
            floatingFlower.style.left = `${Math.random() * 100}vw`;
            floatingFlower.style.animationDelay = `${Math.random() * 10}s`;
            floatingContainer.appendChild(floatingFlower);
        }

        // Function to generate random color for "I Love You" text
        function getRandomColor() {
            const colors = ['#FF5733', '#FFBD33', '#75FF33', '#33FF57', '#33FFBD', '#3380FF', '#A833FF', '#FF33A1'];
            return colors[Math.floor(Math.random() * colors.length)];
        }
    </script>
</body>
</html>
