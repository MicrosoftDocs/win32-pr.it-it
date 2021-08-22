---
description: Consente di tenere traccia delle schede all'interno dei lettori. Queste routine usano in genere la struttura \_ SCARD READERSTATE all'interno di una matrice.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Funzioni di rilevamento delle smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b81ce357cf683d29c1a86d48993c16b7f363635b8e6e3c7e0f2a6ad0900f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917341"
---
# <a name="smart-card-tracking-functions"></a>Funzioni di rilevamento delle smart card

Le funzioni seguenti consentono di tenere traccia delle schede all'interno dei lettori. Queste routine usano in genere la [**struttura \_ SCARD READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) all'interno di una matrice.



| Argomento                                                | Descrizione                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Cercare una scheda la cui [*stringa ATR corrisponde*](../secgloss/a-gly.md) a un nome di scheda specificato. |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Blocca l'esecuzione fino a quando non cambia la disponibilità corrente delle schede.                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Terminare le azioni in sospeso.                                                                                                         |



 

 

 
