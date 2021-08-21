---
title: Composizione dei nomi SPN per un servizio con un SCP
description: L'esempio di codice seguente crea un nome SPN per un servizio che usa un punto di connessione del servizio (SCP).
ms.assetid: cbaa11ba-d32b-46cf-86a4-9050bb1be3a6
ms.tgt_platform: multiple
keywords:
- Composizione dei nomi SPN per un servizio con un'istanza di SCP AD
- Nome entità servizio AD, composizione di nomi SPN per un servizio con un SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e48175bc5fa3d686aab104f8e025d66d7900162235292ed5b853c3284285cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022221"
---
# <a name="composing-the-spns-for-a-service-with-an-scp"></a>Composizione dei nomi SPN per un servizio con un SCP

L'esempio di codice seguente crea un nome SPN per un servizio che usa un punto di connessione del servizio (SCP). Il formato del nome SPN restituito è il seguente.


```C++
<service class>/<host>/<service name>
```



" classe di servizio " e " nome del servizio &lt; &gt; " &lt; &gt; corrispondono ai parametri *pszDNofSCP* e *pszServiceClass.* L'impostazione predefinita di " host " è il &lt; nome DNS del computer &gt; locale.


```C++
DWORD
SpnCompose(
    TCHAR ***pspn,          // Output: an array of SPNs
    unsigned long *pulSpn,  // Output: the number of SPNs returned
    TCHAR *pszDNofSCP,      // Input: DN of the service's SCP
    TCHAR* pszServiceClass) // Input: the name of the service class
{
DWORD   dwStatus;    
 
dwStatus = DsGetSpn(
    DS_SPN_SERVICE, // Type of SPN to create (enumerated type)
    pszServiceClass, // Service class - a name in this case
    pszDNofSCP, // Service name - DN of the service SCP
    0, // Default: omit port component of SPN
    0, // Number of entries in hostnames and ports arrays
    NULL, // Array of hostnames. Default is local computer
    NULL, // Array of ports. Default omits port component
    pulSpn, // Receives number of SPNs returned in array
    pspn // Receives array of SPN(s)
    );
 
return dwStatus;
}
```



 

 




