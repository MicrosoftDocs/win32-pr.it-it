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
# <a name="smart-card-tracking-functions"></a><span data-ttu-id="8b292-104">Funzioni di rilevamento delle smart card</span><span class="sxs-lookup"><span data-stu-id="8b292-104">Smart Card Tracking Functions</span></span>

<span data-ttu-id="8b292-105">Le funzioni seguenti consentono di tenere traccia delle schede all'interno dei lettori.</span><span class="sxs-lookup"><span data-stu-id="8b292-105">The following functions let you track cards within readers.</span></span> <span data-ttu-id="8b292-106">Queste routine usano in genere la struttura [**\_ READERSTATE spaventata**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) all'interno di una matrice.</span><span class="sxs-lookup"><span data-stu-id="8b292-106">These routines typically use the [**SCARD\_READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) structure within an array.</span></span>



| <span data-ttu-id="8b292-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="8b292-107">Topic</span></span>                                                | <span data-ttu-id="8b292-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b292-108">Description</span></span>                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b292-109">**SCardLocateCards**</span><span class="sxs-lookup"><span data-stu-id="8b292-109">**SCardLocateCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | <span data-ttu-id="8b292-110">Cercare una scheda la cui [*stringa ATR*](../secgloss/a-gly.md) corrisponda al nome di una scheda fornita.</span><span class="sxs-lookup"><span data-stu-id="8b292-110">Search for a card whose [*ATR string*](../secgloss/a-gly.md) matches a supplied card name.</span></span> |
| [<span data-ttu-id="8b292-111">**SCardGetStatusChange**</span><span class="sxs-lookup"><span data-stu-id="8b292-111">**SCardGetStatusChange**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | <span data-ttu-id="8b292-112">Blocca l'esecuzione fino a quando non viene modificata la disponibilità corrente delle schede.</span><span class="sxs-lookup"><span data-stu-id="8b292-112">Block execution until the current availability of cards changes.</span></span>                                                                       |
| [<span data-ttu-id="8b292-113">**SCardCancel**</span><span class="sxs-lookup"><span data-stu-id="8b292-113">**SCardCancel**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | <span data-ttu-id="8b292-114">Termina le azioni in attesa.</span><span class="sxs-lookup"><span data-stu-id="8b292-114">Terminate outstanding actions.</span></span>                                                                                                         |



 

 

 
