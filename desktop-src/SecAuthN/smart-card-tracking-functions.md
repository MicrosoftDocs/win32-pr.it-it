---
description: Consente di tenere traccia delle schede all'interno dei lettori. Queste routine usano in genere la \_ struttura READERSTATE spaventata all'interno di una matrice.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Funzioni di rilevamento delle smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884101"
---
# <a name="smart-card-tracking-functions"></a>Funzioni di rilevamento delle smart card

Le funzioni seguenti consentono di tenere traccia delle schede all'interno dei lettori. Queste routine usano in genere la struttura [**\_ READERSTATE spaventata**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) all'interno di una matrice.



| Argomento                                                | Descrizione                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Cercare una scheda la cui [*stringa ATR*](../secgloss/a-gly.md) corrisponda al nome di una scheda fornita. |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Blocca l'esecuzione fino a quando non viene modificata la disponibilità corrente delle schede.                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Termina le azioni in attesa.                                                                                                         |



 

 

 
