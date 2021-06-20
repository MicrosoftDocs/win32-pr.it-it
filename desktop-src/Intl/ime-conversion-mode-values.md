---
description: Esaminare l'elenco dei valori della modalità di conversione IME (Input Method Editor). Questi valori vengono usati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valori della modalità di conversione IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406754"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="35edd-104">Valori della modalità di conversione IME</span><span class="sxs-lookup"><span data-stu-id="35edd-104">IME Conversion Mode Values</span></span>

<span data-ttu-id="35edd-105">Questi valori vengono usati con le [**funzioni ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)</span><span class="sxs-lookup"><span data-stu-id="35edd-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="35edd-106">bit</span><span class="sxs-lookup"><span data-stu-id="35edd-106">Bit</span></span>                      | <span data-ttu-id="35edd-107">Significato</span><span class="sxs-lookup"><span data-stu-id="35edd-107">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="35edd-108">CARATTERE \_ ALFANUMERICO IME CMODE \_</span><span class="sxs-lookup"><span data-stu-id="35edd-108">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="35edd-109">Modalità di input alfanumerica.</span><span class="sxs-lookup"><span data-stu-id="35edd-109">Alphanumeric input mode.</span></span> <span data-ttu-id="35edd-110">Si tratta dell'impostazione predefinita, definita come 0x0000.</span><span class="sxs-lookup"><span data-stu-id="35edd-110">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="35edd-111">IME \_ CMODE \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="35edd-111">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="35edd-112">Impostare su 1 se la modalità di input del codice carattere; 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="35edd-112">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="35edd-113">IME \_ CMODE \_ EUDC</span><span class="sxs-lookup"><span data-stu-id="35edd-113">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="35edd-114">Impostare su 1 se la modalità di conversione EUDC; 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="35edd-114">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="35edd-115">IME \_ CMODE \_ FISSO</span><span class="sxs-lookup"><span data-stu-id="35edd-115">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="35edd-116">**Windows Me/98, Windows 2000, Windows XP:** Impostare su 1 se la modalità di conversione fissa; 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="35edd-116">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="35edd-117">IME \_ CMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="35edd-117">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="35edd-118">Impostare su 1 se la modalità forma completa; 0 se la modalità half shape.</span><span class="sxs-lookup"><span data-stu-id="35edd-118">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="35edd-119">IME \_ CMODE \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="35edd-119">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="35edd-120">Impostare su 1 se la modalità di conversione HANJA; 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="35edd-120">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="35edd-121">IME \_ CMODE \_ KATAKANA</span><span class="sxs-lookup"><span data-stu-id="35edd-121">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="35edd-122">Impostare su 1 se la modalità KATAKANA; 0 se la modalità HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="35edd-122">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="35edd-123">IME \_ CMODE \_ NATIVO</span><span class="sxs-lookup"><span data-stu-id="35edd-123">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="35edd-124">Impostare su 1 se la modalità NATIVA; 0 se la modalità ALPHANUMERIC.</span><span class="sxs-lookup"><span data-stu-id="35edd-124">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="35edd-125">IME \_ CMODE \_ NOCONVERSION</span><span class="sxs-lookup"><span data-stu-id="35edd-125">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="35edd-126">Impostare su 1 per impedire l'elaborazione delle conversioni tramite IME. 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="35edd-126">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="35edd-127">IME \_ CMODE \_ ROMAN</span><span class="sxs-lookup"><span data-stu-id="35edd-127">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="35edd-128">Impostare su 1 se la modalità di input ROMAN; 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="35edd-128">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="35edd-129">IME \_ CMODE \_ SOFTKBD</span><span class="sxs-lookup"><span data-stu-id="35edd-129">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="35edd-130">Impostare su 1 se la modalità Soft Keyboard; 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="35edd-130">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="35edd-131">SIMBOLO \_ CMODE IME \_</span><span class="sxs-lookup"><span data-stu-id="35edd-131">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="35edd-132">Impostare su 1 se la modalità di conversione SYMBOL; 0 in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="35edd-132">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="35edd-133">Tutti gli altri bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="35edd-133">All other bits are reserved.</span></span>

 

 



