// Función para registrar usuarios
const registerUser = (event) => {
    event.preventDefault();

    const id = document.getElementById('id').value;
    const cedula = document.getElementById('cedula').value;
    const name = document.getElementById('name').value;
    const dob = document.getElementById('dob').value;
    const city = document.getElementById('city').value;

    const user = {
        id,
        cedula,
        name,
        dob,
        city
    };

    // Guardar datos en localStorage
    let users = JSON.parse(localStorage.getItem('users')) || [];
    users.push(user);
    localStorage.setItem('users', JSON.stringify(users));

    // Redirigir a la sección de datos registrados
    showUsers();
};

// Función para mostrar los datos registrados
const showUsers = () => {
    const users = JSON.parse(localStorage.getItem('users')) || [];
    const table = document.getElementById('user-table');

    // Limpiar la tabla antes de mostrar los datos
    table.innerHTML = `
        <tr>
            <th>ID</th>
            <th>Cédula</th>
            <th>Nombres y Apellidos</th>
            <th>Fecha de Nacimiento</th>
            <th>Ciudad de Procedencia</th>
        </tr>
    `;

    // Añadir los datos de los usuarios a la tabla
    users.forEach(user => {
        const row = document.createElement('tr');
        Object.values(user).forEach(value => {
            const cell = document.createElement('td');
            cell.innerText = value;
            row.appendChild(cell);
        });
        table.appendChild(row);
    });
};

// Mostrar los datos registrados al cargar la página de datos
if (document.getElementById('user-table')) {
    showUsers();
}
