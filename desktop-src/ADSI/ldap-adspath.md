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
# <a name="ldap-adspath"></a>ADsPath LDAP

Il provider LDAP Microsoft ADsPath richiede il formato seguente.


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> I caratteri di parentesi quadra sinistra e destra ( \[ \] ) indicano parametri facoltativi. non è una parte letterale della stringa di associazione.

 

Il nome host può essere un nome di computer, un indirizzo IP o un nome di dominio. È inoltre possibile specificare un nome di server nella stringa di associazione. La maggior parte dei provider LDAP segue un modello che richiede la specifica di un nome di server.

"NumeroPorta" specifica la porta da utilizzare per la connessione. Se non viene specificato alcun numero di porta, il provider LDAP utilizzerà il numero di porta predefinito. Il numero di porta predefinito è 389 se non si usa una connessione SSL o 636 se si usa una connessione SSL.

"Distinguishname" specifica il nome distinto di un oggetto specifico. Un nome distinto per un determinato oggetto è sicuramente univoco.

Nella tabella seguente sono elencati esempi di stringhe di associazione.



| Esempio di ADsPath LDAP                                      | Descrizione                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| LDAP                                                     | Eseguire l'associazione alla radice dello spazio dei nomi LDAP.                    |
| LDAP://server01                                           | Eseguire l'associazione a un server specifico.                                 |
| LDAP://server01:390                                       | Consente di eseguire l'associazione a un server specifico utilizzando il numero di porta specificato. |
| LDAP://CN = Jeff Smith, CN = Users, DC = Fabrikam, DC = com          | Esegue l'associazione a un oggetto specifico.                                 |
| LDAP://server01/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com | Consente di eseguire il binding a un oggetto specifico tramite un server specifico.       |



 

Se è necessaria l'autenticazione Kerberos per il corretto completamento di una richiesta di directory specifica, la stringa di binding deve usare un ADsPath senza server, ad esempio LDAP://CN = Jeff Smith, CN = Users, DC = Fabrikam, DC = com oppure un ADsPath con un nome di server DNS completo, ad esempio LDAP://server01.fabrikam.com/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com. Il binding al server utilizzando un nome NETBIOS flat o un nome DNS breve, ad esempio, utilizzando il nome Server01 anziché server01.fabrikam.com, non garantisce l'autenticazione Kerberos.

Per ulteriori informazioni ed esempi di stringhe di associazione LDAP, oltre a una descrizione dei caratteri speciali che possono essere utilizzati nelle stringhe di binding LDAP, vedere LDAP ADsPath.

**Windows 2000 con SP1 e versioni successive:** Con il provider LDAP, se una stringa di associazione include un nome di server, è possibile migliorare le prestazioni usando il flag di **\_ \_ binding server ADS** con la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . Il flag di **\_ \_ binding server ADS** indica che è stato specificato un nome di server, che consente a ADSI di evitare il traffico di rete aggiuntivo superfluo.

## <a name="ldap-special-characters"></a>Caratteri speciali LDAP

LDAP include diversi caratteri speciali riservati per l'uso da parte dell'API LDAP. L'elenco dei caratteri speciali si trova in [nomi distinti](/previous-versions/windows/desktop/ldap/distinguished-names). Per usare uno di questi caratteri in un ADsPath senza generare un errore, il carattere deve essere preceduto da un carattere di barra rovesciata ( \\ ). Questa operazione è nota come *escape* per il carattere. Se, ad esempio, si specifica un nome utente nel formato " <last name> , <first name> ", la virgola nel valore del nome deve essere preceduta da un carattere di escape. La stringa risultante avrà un aspetto simile al seguente:


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



Il carattere di escape può essere specificato anche dal relativo codice carattere esadecimale a due cifre. come illustrato nell'esempio seguente.


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



I caratteri non stampabili, ad esempio l'avanzamento riga e il ritorno a capo, devono essere preceduti da un carattere di escape e specificati dal rispettivo codice carattere esadecimale a due cifre. come illustrato nell'esempio seguente.


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>Ulteriori informazioni

Per ulteriori informazioni sulla notazione del nome distinto utilizzata dai servizi directory conformi a LDAP, vedere [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .

 

 