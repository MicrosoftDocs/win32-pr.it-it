---
description: Questi valori vengono utilizzati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valori della modalità di conversione IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129739"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="3d9e1-103">Valori della modalità di conversione IME</span><span class="sxs-lookup"><span data-stu-id="3d9e1-103">IME Conversion Mode Values</span></span>

<span data-ttu-id="3d9e1-104">Questi valori vengono utilizzati con le funzioni [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3d9e1-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="3d9e1-105">bit</span><span class="sxs-lookup"><span data-stu-id="3d9e1-105">Bit</span></span>                      | <span data-ttu-id="3d9e1-106">Significato</span><span class="sxs-lookup"><span data-stu-id="3d9e1-106">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9e1-107">\_ \_ alfanumerico cmode IME</span><span class="sxs-lookup"><span data-stu-id="3d9e1-107">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="3d9e1-108">Modalità di input alfanumerico.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-108">Alphanumeric input mode.</span></span> <span data-ttu-id="3d9e1-109">Si tratta dell'impostazione predefinita, definita come 0x0000.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-109">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="3d9e1-110">\_CHARCODE cmode \_ IME</span><span class="sxs-lookup"><span data-stu-id="3d9e1-110">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="3d9e1-111">Impostare su 1 se la modalità di input del codice carattere; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-111">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="3d9e1-112">\_EUDC cmode \_ IME</span><span class="sxs-lookup"><span data-stu-id="3d9e1-112">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="3d9e1-113">Impostare su 1 se la modalità di conversione EUDC; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-113">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="3d9e1-114">\_cmode IME \_ corretti</span><span class="sxs-lookup"><span data-stu-id="3d9e1-114">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="3d9e1-115">**Windows Me/98, windows 2000, Windows XP:** Impostare su 1 se la modalità di conversione è fissa; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-115">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="3d9e1-116">\_FULLSHAPE cmode \_ IME</span><span class="sxs-lookup"><span data-stu-id="3d9e1-116">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="3d9e1-117">Impostare su 1 se la modalità di forma completa; 0 se la modalità a metà forma.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-117">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="3d9e1-118">\_HANJACONVERT cmode \_ IME</span><span class="sxs-lookup"><span data-stu-id="3d9e1-118">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="3d9e1-119">Impostare su 1 se la modalità di conversione HANJA; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-119">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="3d9e1-120">\_katakana cmode \_ IME</span><span class="sxs-lookup"><span data-stu-id="3d9e1-120">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="3d9e1-121">Impostare su 1 se la modalità KATAKANA; 0 se la modalità HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-121">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="3d9e1-122">IME \_ cmode \_ nativo</span><span class="sxs-lookup"><span data-stu-id="3d9e1-122">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="3d9e1-123">Impostare su 1 se la modalità nativa; 0 se la modalità ALFANUMERICa.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-123">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="3d9e1-124">noconversione IME \_ cmode \_</span><span class="sxs-lookup"><span data-stu-id="3d9e1-124">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="3d9e1-125">Impostare su 1 per impedire l'elaborazione di conversioni da IME; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="3d9e1-126">IME \_ cmode \_ Roman</span><span class="sxs-lookup"><span data-stu-id="3d9e1-126">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="3d9e1-127">Impostare su 1 se la modalità di input romana; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-127">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="3d9e1-128">\_SOFTKBD cmode \_ IME</span><span class="sxs-lookup"><span data-stu-id="3d9e1-128">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="3d9e1-129">Impostare su 1 se la modalità tastiera soft; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-129">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="3d9e1-130">\_simbolo cmode \_ IME</span><span class="sxs-lookup"><span data-stu-id="3d9e1-130">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="3d9e1-131">Impostare su 1 se la modalità di conversione del simbolo. 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-131">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="3d9e1-132">Tutti gli altri bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="3d9e1-132">All other bits are reserved.</span></span>

 

 



