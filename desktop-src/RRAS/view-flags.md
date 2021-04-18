---
title: Visualizza flag
description: Usare i flag di visualizzazione per controllare le viste delle tabelle di routing.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298803"
---
# <a name="view-flags"></a>Visualizza flag

Usare i flag di visualizzazione per controllare le viste delle tabelle di routing.



| Costante                 | Valore      | Descrizione                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| \_dimensioni massime \_ Indirizzo RTM \_ | 16         | Dimensioni massime degli indirizzi per una famiglia di indirizzi.                          |
| \_visualizzazioni massime RTM \_          | 32         | Numero massimo di visualizzazioni che possono essere attive nella tabella di routing. |
| \_ID vista \_ RTM \_ UCAST     | 0          | Specifica una visualizzazione unicast.                                        |
| \_ID vista \_ RTM \_ mcast     | 1          | Specifica una visualizzazione multicast.                                      |
| \_dimensioni della \_ maschera di visualizzazione RTM \_    | 0x20       | Specifica il numero massimo di visualizzazioni che è possibile configurare.    |
| \_maschera di visualizzazione RTM \_ \_ None    | 0x00000000 | Restituisce informazioni indipendentemente dalla visualizzazione.                      |
| \_maschera di visualizzazione RTM \_ \_ any     | 0x00000000 | Restituisce le destinazioni da tutte le visualizzazioni. Si tratta del valore predefinito.  |
| \_maschera di visualizzazione RTM \_ \_ UCAST   | 0x00000001 | Restituisce le destinazioni dalla visualizzazione unicast.                      |
| \_maschera di visualizzazione RTM \_ \_ mcast   | 0x00000002 | Restituisce le destinazioni dalla visualizzazione multicast.                    |
| \_maschera di visualizzazione RTM \_ \_ All     | 0xFFFFFFFF | Restituisce informazioni da tutte le visualizzazioni.                              |



 

 

 




