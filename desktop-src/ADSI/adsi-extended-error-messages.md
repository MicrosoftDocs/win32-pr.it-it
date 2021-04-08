---
title: Messaggi di errore estesi ADSI
description: Questo argomento contiene un elenco di argomenti che illustrano come usare i messaggi di errore ADSI restituiti da IADs, IADsContainer, IDirectoryObject e IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Messaggi di errore estesi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044081"
---
# <a name="adsi-extended-error-messages"></a>Messaggi di errore estesi ADSI

Oltre ai valori **HRESULT** , diversi provider di sistema ADSI (per lo più LDAP) restituiscono dati di errore aggiuntivi per le operazioni eseguite dalle interfacce seguenti:

-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Una parte di tali dati degli errori estesi è la stringa inviata dal server come parte del risultato del messaggio.

Chiamare [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) per recuperare tali messaggi di errore estesi. Il primo parametro di questa funzione, *lpError*, è un valore **DWORD** . Per un server di Active Directory, ADSI tenta di eseguire il mapping di un messaggio di errore LDAP a un codice di errore Win32 appropriato e assegna il valore del codice di errore Win32 a *lpError*. Se non si riesce a risolvere il mapping, ADSI assegna i **dati di errore \_ non validi \_** a *lpError*, come per qualsiasi altro server di directory. In tutti i casi, ADSI inoltra in modo fedele la stringa della descrizione dell'errore dal server al client tramite *lpErrorBuf*, il secondo parametro della funzione **ADsGetLastError** .

 

 




