<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Confirmação de Presença - Chá de Casamento Lauanda & Josué</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #faf7f5;
            color: #5a4b41;
            line-height: 1.6;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            padding: 40px 0;
            background: linear-gradient(135deg, #f9e6e6 0%, #f5d3d3 100%);
            color: #8a3c3c;
            border-radius: 10px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: "❤";
            position: absolute;
            font-size: 200px;
            opacity: 0.05;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 0;
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .noivos {
            font-size: 1.5rem;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }

        .event-info {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 30px;
            border-left: 4px solid #e8c4c4;
        }

        .event-details {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin-bottom: 20px;
        }

        .detail-item {
            flex-basis: 48%;
            margin-bottom: 15px;
            padding: 10px;
        }

        .detail-item h3 {
            color: #8a3c3c;
            margin-bottom: 5px;
            display: flex;
            align-items: center;
        }

        .detail-item h3::before {
            content: "❤";
            margin-right: 8px;
            font-size: 14px;
        }

        .form-container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 30px;
            border-left: 4px solid #e8c4c4;
        }

        .form-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #8a3c3c;
        }

        input, select, textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #e8c4c4;
            border-radius: 5px;
            font-size: 16px;
            background-color: #fefbfb;
        }

        button {
            background: linear-gradient(135deg, #e8c4c4 0%, #d8a6a6 100%);
            color: #8a3c3c;
            border: none;
            padding: 15px 30px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 18px;
            font-weight: 600;
            width: 100%;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            background: linear-gradient(135deg, #d8a6a6 0%, #e8c4c4 100%);
        }

        .confirmation-message {
            display: none;
            text-align: center;
            padding: 40px;
            background-color: #f9e6e6;
            border-radius: 10px;
            margin-top: 20px;
            color: #8a3c3c;
        }

        .guest-list-admin { /* Novo estilo para a seção de administração */
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 30px;
            border-left: 4px solid #e8c4c4;
        }
        
        .guest-list-admin h2 {
            color: #8a3c3c;
            margin-bottom: 20px;
            text-align: center;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid #e8c4c4;
        }

        th {
            background-color: #f9e6e6;
            color: #8a3c3c;
        }

        tr:hover {
            background-color: #fefbfb;
        }

        .total-guests {
            margin-top: 20px;
            text-align: right;
            font-weight: bold;
            color: #8a3c3c;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #8a3c3c;
        }

        @media (max-width: 768px) {
            .detail-item {
                flex-basis: 100%;
            }

            th, td {
                padding: 8px 10px;
            }
        }
        
        /* Estilos para o formulário de Admin */
        #admin-login-section {
            background-color: #f0f0f0;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 30px;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        #admin-login-section input {
            max-width: 250px;
            margin: 5px auto;
            display: block;
        }
        #admin-login-section button {
            width: auto;
            padding: 8px 15px;
            font-size: 16px;
            margin-top: 10px;
        }
        #admin-info {
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Chá de Casamento</h1>
            <p class="noivos">Lauanda & Josué</p>
            <p>Confirmar presença até 15 de Novembro de 2023</p>
        </header>

        <section class="event-info">
            <h2>Detalhes do Evento</h2>
            <div class="event-details">
                <div class="detail-item">
                    <h3>Data e Hora</h3>
                    <p>25 de Novembro de 2023, às 15h</p>
                </div>
                <div class="detail-item">
                    <h3>Local</h3>
                    <p>Salão de Festas Jardim Primavera</p>
                    <p>Av. das Flores, 456 - Centro</p>
                </div>
                <div class="detail-item">
                    <h3>Traje</h3>
                    <p>Esporte fino</p>
                </div>
                <div class="detail-item">
                    <h3>Lista de Presentes</h3>
                    <p>Loja XYZ - Departamento de Utilidades</p>
                </div>
            </div>
        </section>

        <section class="form-container">
            <h2>Confirme sua presença</h2>
            <form id="confirmation-form">
                <div class="form-group">
                    <label for="name">Nome completo*</label>
                    <input type="text" id="name" required placeholder="Digite seu nome completo">
                </div>

                <div class="form-group">
                    <label for="email">E-mail</label>
                    <input type="email" id="email" placeholder="seu@email.com">
                </div>

                <div class="form-group">
                    <label for="phone">Telefone*</label>
                    <input type="tel" id="phone" required placeholder="(11) 99999-9999">
                </div>

                <div class="form-group">
                    <label for="guests">Número de pessoas*</label>
                    <select id="guests" required>
                        <option value="">Selecione...</option>
                        <option value="1">Apenas eu (1 pessoa)</option>
                        <option value="2">2 pessoas</option>
                        <option value="3">3 pessoas</option>
                        <option value="4">4 pessoas</option>
                        <option value="5">5 ou mais pessoas</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="message">Mensagem para os noivos (opcional)</label>
                    <textarea id="message" placeholder="Deixe uma mensagem carinhosa..." rows="3"></textarea>
                </div>

                <button type="submit">Confirmar Presença</button>
            </form>

            <div class="confirmation-message" id="confirmation-message">
                <h2>Obrigado por confirmar sua presença!</h2>
                <p>Sua confirmação foi recebida com sucesso.</p>
                <p>Estamos ansiosos para celebrar este momento especial com você!</p>
            </div>
        </section>
        
        <!-- Seção de Login Admin -->
        <section id="admin-login-section">
            <h2>Área Administrativa</h2>
            <div id="login-form-container">
                <input type="email" id="admin-email" placeholder="Seu e-mail de admin">
                <input type="password" id="admin-password" placeholder="Sua senha de admin">
                <button id="login-button">Login</button>
                <p id="login-error-message" style="color: red; margin-top: 5px;"></p>
            </div>
            <div id="admin-info-container" style="display: none;">
                <p id="admin-info">Olá, </p>
                <button id="logout-button">Sair</button>
            </div>
        </section>

        <!-- Seção da Lista de Convidados (Visível apenas para Admin) -->
        <section class="guest-list-admin" id="guest-list-section" style="display: none;">
            <h2>Lista de Confirmações</h2>
            <table id="guest-table">
                <thead>
                    <tr>
                        <th>Nome</th>
                        <th>Quantidade de Pessoas</th>
                        <th>Contato</th>
                        <th>Mensagem</th>
                        <th>Data Confirmação</th>
                    </tr>
                </thead>
                <tbody id="guest-list-body">
                    <!-- As confirmações serão adicionadas aqui via JavaScript do Firebase -->
                </tbody>
            </table>
            <div class="total-guests" id="total-guests">
                Total de pessoas confirmadas: 0
            </div>
        </section>

        <footer>
            <p>© 2023 Chá de Casamento Lauanda & Josué • Desenvolvido com ❤</p>
        </footer>
    </div>

    <script type="module">
        // Importações do Firebase SDK
        import { initializeApp } from "https://www.gstatic.com/firebasejs/12.2.1/firebase-app.js";
        import { getDatabase, ref, push, set, onValue } from "https://www.gstatic.com/firebasejs/12.2.1/firebase-database.js";
        import { getAuth, signInWithEmailAndPassword, signOut, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/12.2.1/firebase-auth.js";

        // Configuração do Firebase (usando as informações do seu projeto)
        const firebaseConfig = {
          apiKey: "AIzaSyD5YbrMzelqv_vvSyRcSt_sRHlbxkm9jMU",
          authDomain: "chacasamento-8bc0f.firebaseapp.com",
          databaseURL: "https://chacasamento-8bc0f-default-rtdb.firebaseio.com",
          projectId: "chacasamento-8bc0f",
          storageBucket: "chacasamento-8bc0f.firebasestorage.app",
          messagingSenderId: "1006739249795",
          appId: "1:1006739249795:web:3aa6d30afd4ddefc50d9b6",
          measurementId: "G-ZBJVY8J4J5"
        };

        // Inicializar Firebase
        const app = initializeApp(firebaseConfig);
        const db = getDatabase(app);
        const auth = getAuth(app); // Inicializa o Firebase Authentication
        const confirmationsRef = ref(db, 'confirmations'); 

        document.addEventListener('DOMContentLoaded', function() {
            const form = document.getElementById('confirmation-form');
            const confirmationMessageDiv = document.getElementById('confirmation-message');
            const submitButton = form.querySelector('button[type="submit"]');

            const guestListSection = document.getElementById('guest-list-section');
            const adminLoginSection = document.getElementById('admin-login-section');
            const loginFormContainer = document.getElementById('login-form-container');
            const adminInfoContainer = document.getElementById('admin-info-container');
            const adminInfoText = document.getElementById('admin-info');
            const loginButton = document.getElementById('login-button');
            const logoutButton = document.getElementById('logout-button');
            const adminEmailInput = document.getElementById('admin-email');
            const adminPasswordInput = document.getElementById('admin-password');
            const loginErrorMessage = document.getElementById('login-error-message');


            // -- Lógica de Confirmação de Presença (Para Convidados) --
            form.addEventListener('submit', async function(e) {
                e.preventDefault();

                const name = document.getElementById('name').value;
                const email = document.getElementById('email').value;
                const phone = document.getElementById('phone').value;
                const guests = document.getElementById('guests').value;
                const message = document.getElementById('message').value;

                if (!name.trim() || !phone.trim() || !guests) {
                    alert('Por favor, preencha todos os campos obrigatórios (Nome, Telefone, Número de Pessoas).');
                    return;
                }

                submitButton.disabled = true;
                submitButton.textContent = 'Enviando...';

                try {
                    await addConfirmation(name, guests, phone, email, message);
                    confirmationMessageDiv.style.display = 'block';
                    confirmationMessageDiv.scrollIntoView({ behavior: 'smooth' });
                    form.reset();
                    setTimeout(() => {
                        confirmationMessageDiv.style.display = 'none';
                    }, 5000);
                } catch (error) {
                    console.error("Erro ao salvar confirmação no Firebase:", error);
                    alert('Ocorreu um erro ao confirmar sua presença. Por favor, tente novamente.');
                    // Aqui o erro pode ser um Security Rules Denied (403), que não vai acontecer para escrita agora
                } finally {
                    submitButton.disabled = false;
                    submitButton.textContent = 'Confirmar Presença';
                }
            });

            // -- Lógica de Administração (Login/Logout e Exibição da Lista) --

            loginButton.addEventListener('click', async () => {
                const email = adminEmailInput.value;
                const password = adminPasswordInput.value;
                loginErrorMessage.textContent = ''; // Limpa mensagens de erro anteriores

                if (!email || !password) {
                    loginErrorMessage.textContent = 'Por favor, insira e-mail e senha.';
                    return;
                }

                try {
                    await signInWithEmailAndPassword(auth, email, password);
                } catch (error) {
                    console.error("Erro no login:", error.code, error.message);
                    switch (error.code) {
                        case 'auth/user-not-found':
                        case 'auth/wrong-password':
                            loginErrorMessage.textContent = 'E-mail ou senha inválidos.';
                            break;
                        case 'auth/invalid-email':
                            loginErrorMessage.textContent = 'Formato de e-mail inválido.';
                            break;
                        default:
                            loginErrorMessage.textContent = 'Erro ao fazer login. Tente novamente.';
                    }
                }
            });

            logoutButton.addEventListener('click', async () => {
                try {
                    await signOut(auth);
                } catch (error) {
                    console.error("Erro ao fazer logout:", error);
                    alert('Erro ao fazer logout. Tente novamente.');
                }
            });

            // Monitora o estado de autenticação do usuário
            onAuthStateChanged(auth, (user) => {
                if (user) {
                    // Usuário logado: mostra a área admin e esconde o formulário de login
                    loginFormContainer.style.display = 'none';
                    adminInfoContainer.style.display = 'block';
                    adminInfoText.textContent = `Olá, ${user.email}!`;
                    guestListSection.style.display = 'block';
                    loadConfirmations(); // Carrega a lista somente se o admin estiver logado
                } else {
                    // Usuário deslogado: esconde a área admin e mostra o formulário de login
                    loginFormContainer.style.display = 'block';
                    adminInfoContainer.style.display = 'none';
                    guestListSection.style.display = 'none';
                    // Opcional: limpar a lista de convidados se deslogar
                    document.getElementById('guest-list-body').innerHTML = `
                        <tr><td colspan="5" style="text-align: center;">Faça login para ver as confirmações.</td></tr>
                    `;
                    document.getElementById('total-guests').textContent = 'Total de pessoas confirmadas: 0';
                }
            });
        });

        async function addConfirmation(name, guestsCount, phone, email, message) {
            const newConfirmationRef = push(confirmationsRef);
            await set(newConfirmationRef, {
                name: name,
                guests: parseInt(guestsCount),
                phone: phone,
                email: email,
                message: message,
                timestamp: new Date().toISOString()
            });
        }

        function loadConfirmations() {
            const guestListBody = document.getElementById('guest-list-body');
            const totalGuestsElement = document.getElementById('total-guests');

            // onValue é chamado imediatamente e cada vez que os dados mudam
            onValue(confirmationsRef, (snapshot) => {
                guestListBody.innerHTML = '';
                let totalConfirmedPeople = 0;

                if (snapshot.exists()) {
                    const confirmations = snapshot.val();
                    const confirmationsArray = Object.keys(confirmations).map(key => ({
                        id: key,
                        ...confirmations[key]
                    }));

                    confirmationsArray.sort((a, b) => new Date(a.timestamp).getTime() - new Date(b.timestamp).getTime());

                    confirmationsArray.forEach(guest => {
                        const row = document.createElement('tr');
                        const numGuests = guest.guests || 0;
                        totalConfirmedPeople += numGuests;

                        row.innerHTML = `
                            <td>${guest.name}</td>
                            <td>${numGuests} pessoa(s)</td>
                            <td>${guest.phone} ${guest.email ? `<br>${guest.email}` : ''}</td>
                            <td>${guest.message || '-'}</td> <!-- Exibe a mensagem ou um traço -->
                            <td>${new Date(guest.timestamp).toLocaleDateString('pt-BR')} ${new Date(guest.timestamp).toLocaleTimeString('pt-BR')}</td>
                        `;
                        guestListBody.appendChild(row);
                    });
                } else {
                    guestListBody.innerHTML = `
                        <tr>
                            <td colspan="5" style="text-align: center;">Nenhuma confirmação ainda.</td>
                        </tr>
                    `;
                }

                totalGuestsElement.textContent = `Total de pessoas confirmadas: ${totalConfirmedPeople}`;
            }, (error) => {
                 // Captura erros de permissão ou outros erros de leitura
                console.error("Erro ao carregar confirmações:", error);
                if (error.code === 'PERMISSION_DENIED') {
                    guestListBody.innerHTML = `
                        <tr><td colspan="5" style="color: red; text-align: center;">Acesso negado. Faça login como administrador para ver as confirmações.</td></tr>
                    `;
                    totalGuestsElement.textContent = 'Total de pessoas confirmadas: N/A';
                }
            });
        }
    </script>
</body>
</html>
