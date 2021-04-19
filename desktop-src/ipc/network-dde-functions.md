---
description: Le funzioni seguenti vengono utilizzate con la rete DDE.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Funzioni DDE di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319618"
---
# <a name="network-dde-functions"></a>Funzioni DDE di rete

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Le funzioni seguenti vengono utilizzate con la rete DDE.



| Funzione                                                   | Descrizione                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**NDdeGetErrorString**](nddegeterrorstring.md)           | Converte un codice di errore restituito da una funzione DDE di rete in una stringa di errore che descrive il codice di errore restituito. |
| [**NDdeGetShareSecurity**](nddegetsharesecurity.md)       | Recupera il descrittore di sicurezza associato alla condivisione DDE.                                                      |
| [**NDdeGetTrustedShare**](nddegettrustedshare.md)         | Recupera le opzioni associate a una condivisione DDE presente nell'elenco di condivisioni attendibili dell'utente del server.                |
| [**NDdeIsValidAppTopicList**](nddeisvalidapptopiclist.md) | Determina se un'applicazione e una stringa di argomento ("*appname* \| *topicName*") utilizzano la sintassi corretta.                 |
| [**NDdeIsValidShareName**](nddeisvalidsharename.md)       | Determina se un nome di condivisione utilizza la sintassi corretta.                                                               |
| [**NDdeSetShareSecurity**](nddesetsharesecurity.md)       | Imposta il descrittore di sicurezza associato alla condivisione DDE.                                                           |
| [**NDdeSetTrustedShare**](nddesettrustedshare.md)         | Concede lo stato attendibile della condivisione DDE specificato all'interno del contesto dell'utente corrente.                                      |
| [**NDdeShareAdd**](nddeshareadd.md)                       | Crea e aggiunge una nuova condivisione DDE alla gestione del database di condivisione DDE (DSDM).                                            |
| [**NDdeShareDel**](nddesharedel.md)                       | Elimina una condivisione DDE dal DSDM.                                                                                    |
| [**NDdeShareEnum**](nddeshareenum.md)                     | Recupera l'elenco delle condivisioni DDE disponibili.                                                                           |
| [**NDdeShareGetInfo**](nddesharegetinfo.md)               | Recupera le informazioni sulla condivisione DDE.                                                                                      |
| [**NDdeShareSetInfo**](nddesharesetinfo.md)               | Imposta le informazioni sulla condivisione DDE.                                                                                           |
| [**NDdeTrustedShareEnum**](nddetrustedshareenum.md)       | Recupera i nomi di tutte le condivisioni DDE di rete considerate attendibili nel contesto del processo chiamante.                 |



 

 

 



