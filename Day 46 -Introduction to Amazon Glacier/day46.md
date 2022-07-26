* What is Amazon Glacier?

    * Data Archiving Solution
    * It’s designed for infrequently accessed data (you may require that data later for business need or legal purpose)
    * Long term storage solution for low cost
    99.999999999(11 9’s of durability)

* Key Terms

    * Archive: Any object that you store in a Glacier or basic unit of storage in Glacier
    * Vault: Vault is the container for storing archive.
    * Access Policy: Determine who can and can’t access the data stored in the Vault. It also controls what action user can and can’t perform on the Vault. You can also create a Vault lock policy so that Vault can’t be altered.

* Data retrieval from Glacier

    * Expedited: 1–5 min(highest cost)
    * Standard: 3–5 hour
    * Bulk: 5–12 hour(lowest cost)

* Security with Amazon Glacier

    * Glacier access can be control using IAM
    * Glacier encrypt your data using AES-256
    * Glacier manages key for you

* Go to the Glacier tab using AWS console [**here**](https://us-west-2.console.aws.amazon.com/glacier) → Create Vault

* Choose all the default options and create Vault
* Most of the time, I see people use LifeCycle Policies to move the object from S3 to a glacier.

* LifeCycle Management

* Why do we need LifeCycle Management?

    * To save cost
    * In most of the cases, data which is generated by our application is relevant for us for the first 30 days and after that, we don’t access that data as frequently.

* LifeCycle object supports the following but I am going to enable just the required parameters

    * enabled — (Required) Specifies lifecycle rule status.
    * transition - (Optional) Specifies a period in the object's transitions

* Here I am defining after 30 days move the objects to STANDARD_IA and after 60 days to GLACIER.