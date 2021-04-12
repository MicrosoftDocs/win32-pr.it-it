---
description: Questi identificatori vengono usati con la funzione ImmSimulateHotKey.
ms.assetid: a262ef4e-d8ab-4eb6-88c6-023b90850cc6
title: Identificatori di tasti di scelta rapida IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407bffa76558626e88d8fbb88343d82df5557a78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129738"
---
# <a name="ime-hot-key-identifiers"></a><span data-ttu-id="310b3-103">Identificatori di tasti di scelta rapida IME</span><span class="sxs-lookup"><span data-stu-id="310b3-103">IME Hot Key Identifiers</span></span>

<span data-ttu-id="310b3-104">Questi identificatori vengono usati con la funzione [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey) .</span><span class="sxs-lookup"><span data-stu-id="310b3-104">These identifiers are used with the [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey) function.</span></span>



| <span data-ttu-id="310b3-105">Identificatori</span><span class="sxs-lookup"><span data-stu-id="310b3-105">Identifiers</span></span>                       | <span data-ttu-id="310b3-106">Significato</span><span class="sxs-lookup"><span data-stu-id="310b3-106">Meaning</span></span>                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="310b3-107">\_ \_ \_ interruttore attiva disattiva IME CHOTKEY \_ IME</span><span class="sxs-lookup"><span data-stu-id="310b3-107">IME\_CHOTKEY\_IME\_NONIME\_TOGGLE</span></span> | <span data-ttu-id="310b3-108">(Cinese semplificato) Consente di passare da un'operazione IME a un'altra quando il linguaggio è in cinese semplificato.</span><span class="sxs-lookup"><span data-stu-id="310b3-108">(Simplified Chinese) Toggle between IME and non-IME operation when the language is Simplified Chinese.</span></span>                                                                                                  |
| <span data-ttu-id="310b3-109">\_ \_ interruttore forma CHOTKEY \_ IME</span><span class="sxs-lookup"><span data-stu-id="310b3-109">IME\_CHOTKEY\_SHAPE\_TOGGLE</span></span>       | <span data-ttu-id="310b3-110">(Cinese semplificato) Consente di abilitare o disabilitare la modalità di conversione delle forme di IME.</span><span class="sxs-lookup"><span data-stu-id="310b3-110">(Simplified Chinese) Toggle the shape conversion mode of IME.</span></span>                                                                                                                                           |
| <span data-ttu-id="310b3-111">\_interruttore del \_ simbolo \_ CHOTKEY IME</span><span class="sxs-lookup"><span data-stu-id="310b3-111">IME\_CHOTKEY\_SYMBOL\_TOGGLE</span></span>      | <span data-ttu-id="310b3-112">(Cinese semplificato) Consente di abilitare o disabilitare la modalità di conversione dei simboli di IME.</span><span class="sxs-lookup"><span data-stu-id="310b3-112">(Simplified Chinese) Toggle the symbol conversion mode of IME.</span></span> <span data-ttu-id="310b3-113">La modalità simbolo indica che l'utente può inserire segni di punteggiatura e simboli cinesi eseguendo il mapping alla punteggiatura e ai simboli sulla tastiera.</span><span class="sxs-lookup"><span data-stu-id="310b3-113">Symbol mode indicates that the user can input Chinese punctuation and symbols by mapping to the punctuation and symbols on the keyboard.</span></span> |
| <span data-ttu-id="310b3-114">\_RECONVERTSTRING ITHOTKEY \_ IME</span><span class="sxs-lookup"><span data-stu-id="310b3-114">IME\_ITHOTKEY\_RECONVERTSTRING</span></span>    | <span data-ttu-id="310b3-115">**Windows Me/98, windows 2000, Windows XP:** (cinese tradizionale) riconversione del trigger.</span><span class="sxs-lookup"><span data-stu-id="310b3-115">**Windows Me/98, Windows 2000, Windows XP:** (Traditional Chinese) Trigger reconversion.</span></span>                                                                                                                |
| <span data-ttu-id="310b3-116">\_ \_ chiusura apertura JHOTKEY \_ IME</span><span class="sxs-lookup"><span data-stu-id="310b3-116">IME\_JHOTKEY\_CLOSE\_OPEN</span></span>         | <span data-ttu-id="310b3-117">Giapponese In alternativa, aprire e chiudere l'IME.</span><span class="sxs-lookup"><span data-stu-id="310b3-117">(Japanese) Alternately open and close the IME.</span></span>                                                                                                                                                          |
| <span data-ttu-id="310b3-118">IME \_ KHOTKEY \_ inglese</span><span class="sxs-lookup"><span data-stu-id="310b3-118">IME\_KHOTKEY\_ENGLISH</span></span>             | <span data-ttu-id="310b3-119">Coreano Passa a inglese.</span><span class="sxs-lookup"><span data-stu-id="310b3-119">(Korean) Switch to English.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="310b3-120">\_ \_ interruttore forma KHOTKEY \_ IME</span><span class="sxs-lookup"><span data-stu-id="310b3-120">IME\_KHOTKEY\_SHAPE\_TOGGLE</span></span>       | <span data-ttu-id="310b3-121">Coreano Consente di abilitare o disabilitare la modalità di conversione delle forme di IME.</span><span class="sxs-lookup"><span data-stu-id="310b3-121">(Korean) Toggle the shape conversion mode of IME.</span></span>                                                                                                                                                       |
| <span data-ttu-id="310b3-122">\_HANJACONVERT KHOTKEY \_ IME</span><span class="sxs-lookup"><span data-stu-id="310b3-122">IME\_KHOTKEY\_HANJACONVERT</span></span>        | <span data-ttu-id="310b3-123">Coreano Passa alla conversione Hanja.</span><span class="sxs-lookup"><span data-stu-id="310b3-123">(Korean) Switch to Hanja conversion.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="310b3-124">\_ \_ \_ interruttore attiva disattiva IME thotkey \_ IME</span><span class="sxs-lookup"><span data-stu-id="310b3-124">IME\_THOTKEY\_IME\_NONIME\_TOGGLE</span></span> | <span data-ttu-id="310b3-125">(Cinese tradizionale) Consente di passare da un'operazione IME a un'altra quando il linguaggio è cinese tradizionale.</span><span class="sxs-lookup"><span data-stu-id="310b3-125">(Traditional Chinese) Toggle between IME and non-IME operation when the language is Traditional Chinese.</span></span>                                                                                                |
| <span data-ttu-id="310b3-126">\_ \_ interruttore forma thotkey \_ IME</span><span class="sxs-lookup"><span data-stu-id="310b3-126">IME\_THOTKEY\_SHAPE\_TOGGLE</span></span>       | <span data-ttu-id="310b3-127">(Cinese tradizionale) Consente di abilitare o disabilitare la modalità di conversione delle forme di IME.</span><span class="sxs-lookup"><span data-stu-id="310b3-127">(Traditional Chinese) Toggle the shape conversion mode of IME.</span></span>                                                                                                                                          |
| <span data-ttu-id="310b3-128">\_interruttore del \_ simbolo \_ thotkey IME</span><span class="sxs-lookup"><span data-stu-id="310b3-128">IME\_THOTKEY\_SYMBOL\_TOGGLE</span></span>      | <span data-ttu-id="310b3-129">(Cinese tradizionale) Consente di abilitare o disabilitare la modalità di conversione dei simboli di IME.</span><span class="sxs-lookup"><span data-stu-id="310b3-129">(Traditional Chinese) Toggle the symbol conversion mode of IME.</span></span>                                                                                                                                         |



 

 

 



