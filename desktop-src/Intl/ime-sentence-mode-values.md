---
description: Esaminare l'elenco dei valori della modalità frase IME (Input Method Editor). Questi valori vengono usati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valori della modalità frase IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406764"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="42f08-104">Valori della modalità frase IME</span><span class="sxs-lookup"><span data-stu-id="42f08-104">IME Sentence Mode Values</span></span>

<span data-ttu-id="42f08-105">Questi valori vengono usati con le [**funzioni ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) [**e ImmSetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)</span><span class="sxs-lookup"><span data-stu-id="42f08-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="42f08-106">Costante</span><span class="sxs-lookup"><span data-stu-id="42f08-106">Constant</span></span>                  | <span data-ttu-id="42f08-107">Definizione</span><span class="sxs-lookup"><span data-stu-id="42f08-107">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="42f08-108">IME \_ SMODE \_ AUTOMATIC</span><span class="sxs-lookup"><span data-stu-id="42f08-108">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="42f08-109">L'IME esegue l'elaborazione della conversione in modalità automatica.</span><span class="sxs-lookup"><span data-stu-id="42f08-109">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="42f08-110">IME \_ SMODE \_ NONE</span><span class="sxs-lookup"><span data-stu-id="42f08-110">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="42f08-111">Nessuna informazione per la frase.</span><span class="sxs-lookup"><span data-stu-id="42f08-111">No information for sentence.</span></span>                                               |
| <span data-ttu-id="42f08-112">IME \_ SMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="42f08-112">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="42f08-113">L'IME usa le informazioni sulle frasi per stimare il carattere successivo.</span><span class="sxs-lookup"><span data-stu-id="42f08-113">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="42f08-114">IME \_ SMODE \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="42f08-114">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="42f08-115">L'IME usa informazioni sulla clausola plurale per eseguire l'elaborazione della conversione.</span><span class="sxs-lookup"><span data-stu-id="42f08-115">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="42f08-116">IME \_ SMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="42f08-116">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="42f08-117">L'IME esegue l'elaborazione della conversione in modalità a carattere singolo.</span><span class="sxs-lookup"><span data-stu-id="42f08-117">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="42f08-118">CONVERSAZIONE \_ SMODE IME \_</span><span class="sxs-lookup"><span data-stu-id="42f08-118">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="42f08-119">L'IME usa la modalità conversazione.</span><span class="sxs-lookup"><span data-stu-id="42f08-119">The IME uses conversation mode.</span></span> <span data-ttu-id="42f08-120">Ciò è utile per le applicazioni di chat.</span><span class="sxs-lookup"><span data-stu-id="42f08-120">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="42f08-121">I bit da 16 a 31 sono riservati per l'uso IME.</span><span class="sxs-lookup"><span data-stu-id="42f08-121">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



