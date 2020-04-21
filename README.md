# A website about Jovanni

A website :)
Here is a youtube video:
https://www.youtube.com/watch?v=kNPu2orPB8Y&list=RDMM&index=27

// Read the file into an array
$users = file("names.txt");

if (count($users)) {
    // Open the table
    echo "<table>";

    // Cycle through the array
    foreach ($users as $user) {

        // Parse the line, retriving the name and e-mail address
        list($name, $email) = explode(" ", $user);

        // Remove newline from $email
        $email = trim($email);

        // Output a row
        echo "<tr>";
        echo "<td>$name</td>";
        echo "<td><a href=\"mailto:$email\">$email</a></td>";
        echo "</tr>";
    }

    // Close the table
    echo "</table>";
}
