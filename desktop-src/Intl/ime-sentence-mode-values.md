---
description: Questi valori vengono utilizzati con le funzioni ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valori della modalità frase IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231741"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="c9806-103">Valori della modalità frase IME</span><span class="sxs-lookup"><span data-stu-id="c9806-103">IME Sentence Mode Values</span></span>

<span data-ttu-id="c9806-104">Questi valori vengono utilizzati con le funzioni [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="c9806-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="c9806-105">Costante</span><span class="sxs-lookup"><span data-stu-id="c9806-105">Constant</span></span>                  | <span data-ttu-id="c9806-106">Definizione</span><span class="sxs-lookup"><span data-stu-id="c9806-106">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="c9806-107">\_SMODE IME \_ automatico</span><span class="sxs-lookup"><span data-stu-id="c9806-107">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="c9806-108">L'IME esegue l'elaborazione della conversione in modalità automatica.</span><span class="sxs-lookup"><span data-stu-id="c9806-108">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="c9806-109">\_SMODE IME \_ None</span><span class="sxs-lookup"><span data-stu-id="c9806-109">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="c9806-110">Nessuna informazione per la frase.</span><span class="sxs-lookup"><span data-stu-id="c9806-110">No information for sentence.</span></span>                                               |
| <span data-ttu-id="c9806-111">\_PHRASEPREDICT SMODE \_ IME</span><span class="sxs-lookup"><span data-stu-id="c9806-111">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="c9806-112">L'IME utilizza le informazioni sulla frase per stimare il carattere successivo.</span><span class="sxs-lookup"><span data-stu-id="c9806-112">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="c9806-113">\_PLURALCLAUSE SMODE \_ IME</span><span class="sxs-lookup"><span data-stu-id="c9806-113">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="c9806-114">L'IME utilizza le informazioni sulla clausola plurale per eseguire l'elaborazione della conversione.</span><span class="sxs-lookup"><span data-stu-id="c9806-114">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="c9806-115">\_SINGLECONVERT SMODE \_ IME</span><span class="sxs-lookup"><span data-stu-id="c9806-115">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="c9806-116">L'IME esegue l'elaborazione della conversione in modalità a carattere singolo.</span><span class="sxs-lookup"><span data-stu-id="c9806-116">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="c9806-117">\_conversazione SMODE \_ IME</span><span class="sxs-lookup"><span data-stu-id="c9806-117">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="c9806-118">L'IME utilizza la modalità conversazione.</span><span class="sxs-lookup"><span data-stu-id="c9806-118">The IME uses conversation mode.</span></span> <span data-ttu-id="c9806-119">Questa operazione è utile per le applicazioni di chat.</span><span class="sxs-lookup"><span data-stu-id="c9806-119">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="c9806-120">I bit da 16 a 31 sono riservati per l'uso di IME.</span><span class="sxs-lookup"><span data-stu-id="c9806-120">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



