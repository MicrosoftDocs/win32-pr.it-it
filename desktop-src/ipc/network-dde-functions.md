---
description: Le funzioni seguenti vengono usate con DDE di rete.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Funzioni DDE di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b37e83dd6b335e1acd2e77010fa61d0da5e3e26af5b46eef54d5ee20cf2eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756310"
---
# <a name="network-dde-functions"></a>Funzioni DDE di rete

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Le funzioni seguenti vengono usate con DDE di rete.



| Funzione                                                   | Descrizione                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**NDdeGetErrorString**](nddegeterrorstring.md)           | Converte un codice di errore restituito da una funzione DDE di rete in una stringa di errore che spiega il codice di errore restituito. |
| [**NDdeGetShareSecurity**](nddegetsharesecurity.md)       | Recupera il descrittore di sicurezza associato alla condivisione DDE.                                                      |
| [**NDdeGetTrustedShare**](nddegettrustedshare.md)         | Recupera le opzioni associate a una condivisione DDE presente nell'elenco di condivisioni attendibili dell'utente del server.                |
| [**NDdeIsValidAppTopicList**](nddeisvalidapptopiclist.md) | Determina se una stringa dell'applicazione e dell'argomento ("*AppName* \| *TopicName*") usa la sintassi corretta.                 |
| [**NDdeIsValidShareName**](nddeisvalidsharename.md)       | Determina se un nome di condivisione usa la sintassi corretta.                                                               |
| [**NDdeSetShareSecurity**](nddesetsharesecurity.md)       | Imposta il descrittore di sicurezza associato alla condivisione DDE.                                                           |
| [**NDdeSetTrustedShare**](nddesettrustedshare.md)         | Concede lo stato attendibile della condivisione DDE specificata all'interno del contesto dell'utente corrente.                                      |
| [**NDdeShareAdd**](nddeshareadd.md)                       | Crea e aggiunge una nuova condivisione DDE al gestore del database di condivisione DDE.                                            |
| [**NDdeShareDel**](nddesharedel.md)                       | Elimina una condivisione DDE da DSDM.                                                                                    |
| [**NDdeShareEnum**](nddeshareenum.md)                     | Recupera l'elenco di condivisioni DDE disponibili.                                                                           |
| [**NDdeShareGetInfo**](nddesharegetinfo.md)               | Recupera le informazioni sulla condivisione DDE.                                                                                      |
| [**NDdeShareSetInfo**](nddesharesetinfo.md)               | Imposta le informazioni sulla condivisione DDE.                                                                                           |
| [**NDdeTrustedShareEnum**](nddetrustedshareenum.md)       | Recupera i nomi di tutte le condivisioni DDE di rete attendibili nel contesto del processo chiamante.                 |



 

 

 



