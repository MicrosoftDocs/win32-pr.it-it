---
title: Messaggi di errore estesi ADSI
description: Questo argomento contiene un elenco di argomenti che illustrano come usare i messaggi di errore ADSI restituiti da IAD, IADsContainer, IDirectoryObject e IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Messaggi di errore estesi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2bf4c7faef20feeb868fdcbb0e36d7f1ad5d0b9c68cc8879d5019e81e186a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180875"
---
# <a name="adsi-extended-error-messages"></a>Messaggi di errore estesi ADSI

Oltre ai valori **HRESULT,** diversi provider di sistema ADSI (principalmente LDAP) restituiscono dati di errore aggiuntivi per le operazioni eseguite dalle interfacce seguenti:

-   [**IAD**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Una parte di tali dati di errore estesi è la stringa inviata dal server come parte del risultato del messaggio.

Chiamare [**ADsGetLastError per**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) recuperare tali messaggi di errore estesi. Il primo parametro di questa funzione, *lpError,* è un **valore DWORD.** Per un server Active Directory, ADSI tenta di eseguire il mapping di un messaggio di errore LDAP a un codice di errore Win32 appropriato e assegna il valore del codice di errore Win32 *a lpError*. Se non si risolve il mapping, ADSI assegna **ERROR \_ INVALID \_ DATA** a *lpError,* come per qualsiasi altro server di directory. In tutti i casi, ADSI inoltra la stringa della descrizione dell'errore dal server al client tramite *lpErrorBuf,* il secondo parametro della **funzione ADsGetLastError.**

 

 




