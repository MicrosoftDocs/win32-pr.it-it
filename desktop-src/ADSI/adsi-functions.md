---
title: Funzioni ADSI
description: Active Directory interfacce del servizio espongono le funzioni di supporto seguenti ai client che non utilizzano l'automazione.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, informazioni di riferimento, funzioni
- ADSI funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328444"
---
# <a name="adsi-functions"></a>Funzioni ADSI

Active Directory interfacce del servizio espongono le funzioni di supporto seguenti ai client che non utilizzano l'automazione.



| Funzione                                           | Descrizione                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | Crea un oggetto enumeratore per l'oggetto contenitore ADSI specificato.                              |
| [**ADsBuildVarArrayInt**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | Compila una matrice Variant da una matrice di **DWORD**.                                                |
| [**ADsBuildVarArrayStr**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | Compila una matrice Variant da una matrice di stringhe Unicode.                                           |
| [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | Converte un BLOB di dati binari nel formato appropriato per un filtro di ricerca.                         |
| [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | Popola una matrice Variant con gli elementi recuperati dall'oggetto enumeratore specificato.            |
| [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | Libera un oggetto enumeratore creato in precedenza da [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator). |
| [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | Recupera l'ultimo valore del codice di errore del thread chiamante.                                         |
| [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | Esegue l'associazione a un oggetto ADSI utilizzando le credenziali correnti.                                             |
| [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | Esegue l'associazione a un oggetto ADSI utilizzando le credenziali specificate                                                |
| [**ADsSetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | Imposta il valore del codice di errore del thread chiamante.                                                   |
| [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | Alloca un blocco di memoria.                                                                       |
| [**AllocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | Alloca memoria per una determinata stringa.                                                               |
| [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | Libera la memoria allocata da [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).                                  |
| [**FreeADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | Libera la memoria allocata per la stringa specificata.                                                   |
| [**ReallocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | Assegna il contenuto di memoria esistente a una posizione di memoria appena creata.                            |
| [**ReallocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | Sostituisce una stringa esistente con una nuova.                                                        |



 

Le funzioni ADSI seguenti sono obsolete.



| Funzione                                                  | Descrizione |
|-----------------------------------------------------------|-------------|
| [**AdsFreeAllErrorRecords**](obsolete-adsi-functions.md) | Obsoleta.   |
| [**AdsDecodeBinaryData**](obsolete-adsi-functions.md)    | Obsoleta.   |
| [**PropVariantToAdsType**](obsolete-adsi-functions.md)   | Obsoleta.   |
| [**AdsTypeToPropVariant**](obsolete-adsi-functions.md)   | Obsoleta.   |
| [**AdsFreeAdsValues**](obsolete-adsi-functions.md)       | Obsoleta.   |
| [**InitAdsMem**](obsolete-adsi-functions.md)             | Obsoleta.   |
| [**AssertAdsmemLeaks**](obsolete-adsi-functions.md)      | Obsoleta.   |
| [**DumpMemorytracker**](obsolete-adsi-functions.md)      | Obsoleta.   |



 

 

 




