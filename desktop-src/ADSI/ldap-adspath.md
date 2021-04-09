---
title: ADsPath LDAP
description: In questo argomento viene illustrata la sintassi da utilizzare per il ADsPath LDAP.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- ADsPath LDAP
- ADsPath, LDAP, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730306"
---
# <a name="ldap-adspath"></a><span data-ttu-id="879f5-105">ADsPath LDAP</span><span class="sxs-lookup"><span data-stu-id="879f5-105">LDAP ADsPath</span></span>

<span data-ttu-id="879f5-106">Il provider LDAP Microsoft ADsPath richiede il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="879f5-106">The Microsoft LDAP provider ADsPath requires the following format.</span></span>


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> <span data-ttu-id="879f5-107">I caratteri di parentesi quadra sinistra e destra ( \[ \] ) indicano parametri facoltativi. non è una parte letterale della stringa di associazione.</span><span class="sxs-lookup"><span data-stu-id="879f5-107">The left and right bracket characters (\[ \]) indicate optional parameters; it is not a literal part of the binding string.</span></span>

 

<span data-ttu-id="879f5-108">Il nome host può essere un nome di computer, un indirizzo IP o un nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="879f5-108">The "HostName" can be a computer name, an IP address, or a domain name.</span></span> <span data-ttu-id="879f5-109">È inoltre possibile specificare un nome di server nella stringa di associazione.</span><span class="sxs-lookup"><span data-stu-id="879f5-109">A server name can also be specified in the binding string.</span></span> <span data-ttu-id="879f5-110">La maggior parte dei provider LDAP segue un modello che richiede la specifica di un nome di server.</span><span class="sxs-lookup"><span data-stu-id="879f5-110">Most LDAP providers follow a model that requires a server name to be specified.</span></span>

<span data-ttu-id="879f5-111">"NumeroPorta" specifica la porta da utilizzare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="879f5-111">The "PortNumber" specifies the port to be used for the connection.</span></span> <span data-ttu-id="879f5-112">Se non viene specificato alcun numero di porta, il provider LDAP utilizzerà il numero di porta predefinito.</span><span class="sxs-lookup"><span data-stu-id="879f5-112">If no port number is specified, the LDAP provider uses the default port number.</span></span> <span data-ttu-id="879f5-113">Il numero di porta predefinito è 389 se non si usa una connessione SSL o 636 se si usa una connessione SSL.</span><span class="sxs-lookup"><span data-stu-id="879f5-113">The default port number is 389 if not using an SSL connection or 636 if using an SSL connection.</span></span>

<span data-ttu-id="879f5-114">"Distinguishname" specifica il nome distinto di un oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="879f5-114">The "DistinguishedName" specifies the distinguished name of a specific object.</span></span> <span data-ttu-id="879f5-115">Un nome distinto per un determinato oggetto è sicuramente univoco.</span><span class="sxs-lookup"><span data-stu-id="879f5-115">A distinguished name for a given object is guaranteed to be unique.</span></span>

<span data-ttu-id="879f5-116">Nella tabella seguente sono elencati esempi di stringhe di associazione.</span><span class="sxs-lookup"><span data-stu-id="879f5-116">The following table lists examples of binding strings.</span></span>



| <span data-ttu-id="879f5-117">Esempio di ADsPath LDAP</span><span class="sxs-lookup"><span data-stu-id="879f5-117">LDAP ADsPath example</span></span>                                      | <span data-ttu-id="879f5-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="879f5-118">Description</span></span>                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="879f5-119">LDAP</span><span class="sxs-lookup"><span data-stu-id="879f5-119">LDAP:</span></span>                                                     | <span data-ttu-id="879f5-120">Eseguire l'associazione alla radice dello spazio dei nomi LDAP.</span><span class="sxs-lookup"><span data-stu-id="879f5-120">Bind to the root of the LDAP namespace.</span></span>                    |
| <span data-ttu-id="879f5-121">LDAP://server01</span><span class="sxs-lookup"><span data-stu-id="879f5-121">LDAP://server01</span></span>                                           | <span data-ttu-id="879f5-122">Eseguire l'associazione a un server specifico.</span><span class="sxs-lookup"><span data-stu-id="879f5-122">Bind to a specific server.</span></span>                                 |
| <span data-ttu-id="879f5-123">LDAP://server01:390</span><span class="sxs-lookup"><span data-stu-id="879f5-123">LDAP://server01:390</span></span>                                       | <span data-ttu-id="879f5-124">Consente di eseguire l'associazione a un server specifico utilizzando il numero di porta specificato.</span><span class="sxs-lookup"><span data-stu-id="879f5-124">Bind to a specific server using the specified port number.</span></span> |
| <span data-ttu-id="879f5-125">LDAP://CN = Jeff Smith, CN = Users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="879f5-125">LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span>          | <span data-ttu-id="879f5-126">Esegue l'associazione a un oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="879f5-126">Bind to a specific object.</span></span>                                 |
| <span data-ttu-id="879f5-127">LDAP://server01/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="879f5-127">LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span> | <span data-ttu-id="879f5-128">Consente di eseguire il binding a un oggetto specifico tramite un server specifico.</span><span class="sxs-lookup"><span data-stu-id="879f5-128">Bind to a specific object through a specific server.</span></span>       |



 

<span data-ttu-id="879f5-129">Se è necessaria l'autenticazione Kerberos per il corretto completamento di una richiesta di directory specifica, la stringa di binding deve usare un ADsPath senza server, ad esempio LDAP://CN = Jeff Smith, CN = Users, DC = Fabrikam, DC = com oppure un ADsPath con un nome di server DNS completo, ad esempio LDAP://server01.fabrikam.com/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="879f5-129">If Kerberos authentication is required for the successful completion of a specific directory request, the binding string must use either a serverless ADsPath, such as LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, or it must use an ADsPath with a fully qualified DNS server name, such as LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com.</span></span> <span data-ttu-id="879f5-130">Il binding al server utilizzando un nome NETBIOS flat o un nome DNS breve, ad esempio, utilizzando il nome Server01 anziché server01.fabrikam.com, non garantisce l'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="879f5-130">Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the name server01 instead of server01.fabrikam.com, is not guaranteed to yield Kerberos authentication.</span></span>

<span data-ttu-id="879f5-131">Per ulteriori informazioni ed esempi di stringhe di associazione LDAP, oltre a una descrizione dei caratteri speciali che possono essere utilizzati nelle stringhe di binding LDAP, vedere LDAP ADsPath.</span><span class="sxs-lookup"><span data-stu-id="879f5-131">For more information and examples of LDAP binding strings, as well as a description of special characters that can be used in LDAP binding strings, see LDAP ADsPath.</span></span>

<span data-ttu-id="879f5-132">**Windows 2000 con SP1 e versioni successive:** Con il provider LDAP, se una stringa di associazione include un nome di server, è possibile migliorare le prestazioni usando il flag di **\_ \_ binding server ADS** con la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="879f5-132">**Windows 2000 with SP1 and later:** With the LDAP provider, if a binding string includes a server name, you can increase performance by using the **ADS\_SERVER\_BIND** flag with the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span> <span data-ttu-id="879f5-133">Il flag di **\_ \_ binding server ADS** indica che è stato specificato un nome di server, che consente a ADSI di evitare il traffico di rete aggiuntivo superfluo.</span><span class="sxs-lookup"><span data-stu-id="879f5-133">The **ADS\_SERVER\_BIND** flag indicates that a server name was specified, which enables ADSI to avoid additional, unnecessary network traffic.</span></span>

## <a name="ldap-special-characters"></a><span data-ttu-id="879f5-134">Caratteri speciali LDAP</span><span class="sxs-lookup"><span data-stu-id="879f5-134">LDAP Special Characters</span></span>

<span data-ttu-id="879f5-135">LDAP include diversi caratteri speciali riservati per l'uso da parte dell'API LDAP.</span><span class="sxs-lookup"><span data-stu-id="879f5-135">LDAP has several special characters which are reserved for use by the LDAP API.</span></span> <span data-ttu-id="879f5-136">L'elenco dei caratteri speciali si trova in [nomi distinti](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="879f5-136">The list of special characters can be found in [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span> <span data-ttu-id="879f5-137">Per usare uno di questi caratteri in un ADsPath senza generare un errore, il carattere deve essere preceduto da un carattere di barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="879f5-137">To use one of these characters in an ADsPath without generating an error, the character must be preceded by a backslash (\\) character.</span></span> <span data-ttu-id="879f5-138">Questa operazione è nota come *escape* per il carattere.</span><span class="sxs-lookup"><span data-stu-id="879f5-138">This is known as *escaping* the character.</span></span> <span data-ttu-id="879f5-139">Se, ad esempio, si specifica un nome utente nel formato " <last name> , <first name> ", la virgola nel valore del nome deve essere preceduta da un carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="879f5-139">For example, if a user name is given in the form of "<last name>,<first name>", the comma in the name value must be escaped.</span></span> <span data-ttu-id="879f5-140">La stringa risultante avrà un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="879f5-140">The resulting string would look like this:</span></span>


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="879f5-141">Il carattere di escape può essere specificato anche dal relativo codice carattere esadecimale a due cifre.</span><span class="sxs-lookup"><span data-stu-id="879f5-141">The escaped character can also be specified by its two digit hexadecimal character code.</span></span> <span data-ttu-id="879f5-142">come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="879f5-142">This is shown in the following example.</span></span>


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="879f5-143">I caratteri non stampabili, ad esempio l'avanzamento riga e il ritorno a capo, devono essere preceduti da un carattere di escape e specificati dal rispettivo codice carattere esadecimale a due cifre.</span><span class="sxs-lookup"><span data-stu-id="879f5-143">Non-printable characters, such as the line feed and carriage return, must be escaped and specified by their two digit hexadecimal character code.</span></span> <span data-ttu-id="879f5-144">come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="879f5-144">This is shown in the following example.</span></span>


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a><span data-ttu-id="879f5-145">Ulteriori informazioni</span><span class="sxs-lookup"><span data-stu-id="879f5-145">For More Information</span></span>

<span data-ttu-id="879f5-146">Per ulteriori informazioni sulla notazione del nome distinto utilizzata dai servizi directory conformi a LDAP, vedere [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .</span><span class="sxs-lookup"><span data-stu-id="879f5-146">For more information about the distinguished name notation used by LDAP-compliant directory services, see [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt).</span></span>

 

 