---
title: LDAP ADsPath
description: Questo argomento illustra la sintassi da usare per LDAP ADsPath.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- LDAP ADsPath
- ADsPath, LDAP, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1850c30ff8a5a086fbd697080ac32b5e55549496739d9388a6d5e7ab251403d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839471"
---
# <a name="ldap-adspath"></a>LDAP ADsPath

Il provider LDAP Microsoft ADsPath richiede il formato seguente.


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> I caratteri parentesi quadre sinistra e destra ( \[ \] ) indicano parametri facoltativi; non è una parte letterale della stringa di associazione.

 

"HostName" può essere un nome di computer, un indirizzo IP o un nome di dominio. È anche possibile specificare un nome di server nella stringa di associazione. La maggior parte dei provider LDAP segue un modello che richiede la specifica di un nome di server.

"PortNumber" specifica la porta da usare per la connessione. Se non viene specificato alcun numero di porta, il provider LDAP usa il numero di porta predefinito. Il numero di porta predefinito è 389 se non si usa una connessione SSL o 636 se si usa una connessione SSL.

"DistinguishedName" specifica il nome distinto di un oggetto specifico. È garantito che un nome distinto per un determinato oggetto sia univoco.

Nella tabella seguente sono elencati esempi di stringhe di associazione.



| Esempio di LDAP ADsPath                                      | Descrizione                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| Ldap:                                                     | Eseguire il binding alla radice dello spazio dei nomi LDAP.                    |
| LDAP://server01                                           | Eseguire l'associazione a un server specifico.                                 |
| LDAP://server01:390                                       | Eseguire l'associazione a un server specifico usando il numero di porta specificato. |
| LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com          | Eseguire l'associazione a un oggetto specifico.                                 |
| LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com | Eseguire l'associazione a un oggetto specifico tramite un server specifico.       |



 

Se l'autenticazione Kerberos è necessaria per il corretto completamento di una richiesta di directory specifica, la stringa di associazione deve usare un ADsPath serverless, ad esempio LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, oppure deve usare un ADsPath con un nome di server DNS completo, ad esempio LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com. L'associazione al server tramite un nome NETBIOS semplice o un nome DNS breve, ad esempio usando il server dei nomi01 anziché server01.fabrikam.com, non garantisce la produzione dell'autenticazione Kerberos.

Per altre informazioni ed esempi di stringhe di associazione LDAP, nonché una descrizione dei caratteri speciali che possono essere usati nelle stringhe di associazione LDAP, vedere LDAP ADsPath.

**Windows 2000 con SP1 e versioni successive:** Con il provider LDAP, se una stringa di associazione include un nome del server, è possibile migliorare le prestazioni usando il flag **ADS \_ SERVER \_ BIND** con la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o il metodo [**IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) Il flag **ADS \_ SERVER \_ BIND** indica che è stato specificato un nome di server, che consente ad ADSI di evitare traffico di rete aggiuntivo e non necessario.

## <a name="ldap-special-characters"></a>Caratteri speciali LDAP

LDAP include diversi caratteri speciali riservati per l'uso da parte dell'API LDAP. L'elenco dei caratteri speciali è disponibile in [Nomi distinti.](/previous-versions/windows/desktop/ldap/distinguished-names) Per usare uno di questi caratteri in ADsPath senza generare un errore, il carattere deve essere preceduto da una barra rovesciata ( \\ ) . Questa operazione è nota come *escape del* carattere. Ad esempio, se un nome utente viene specificato nel formato " , ", la virgola nel valore del nome deve essere preceduta da un carattere <last name> <first name> di escape. La stringa risultante sarà simile alla seguente:


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



Il carattere di escape può essere specificato anche dal relativo codice carattere esadecimale a due cifre. come illustrato nell'esempio seguente.


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



I caratteri non stampabili, ad esempio l'avanzamento riga e il ritorno a capo, devono essere preceduti da un carattere di escape e devono essere specificati dal relativo codice carattere esadecimale a due cifre. come illustrato nell'esempio seguente.


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>Ulteriori informazioni

Per altre informazioni sulla notazione del nome distinto usata dai servizi directory conformi a LDAP, vedere [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .

 

 