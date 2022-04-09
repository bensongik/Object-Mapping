# Object-Mapping
The same user table uses annotations so that Hibernate can map "automatically" as follows.
@Entity
@Table(name = "user")
@Data
public class UserModel {
@Id
@GeneratedValue(strategy = GenerationType.IDENTITY)
private Integer id;

@NotEmpty
@Column(name = "username")
private String username;

@NotEmpty
@Column(name = "password")
private String password;

@NotEmpty
@Column(name = "createdDate")
private Date createdDate;
}
