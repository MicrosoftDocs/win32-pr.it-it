---
description: Costanti smon delle impostazioni locali \_ \*
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: Costanti LOCALE_SMON *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309500"
---
# <a name="locale_smon-constants"></a><span data-ttu-id="cf902-103">Costanti smon delle impostazioni locali \_ \*</span><span class="sxs-lookup"><span data-stu-id="cf902-103">LOCALE\_SMON\* Constants</span></span>

<span data-ttu-id="cf902-104">In questo argomento vengono definite le \_ costanti smon delle impostazioni locali \* utilizzate da NLS per la rappresentazione dei valori monetari.</span><span class="sxs-lookup"><span data-stu-id="cf902-104">This topic defines the LOCALE\_SMON\* constants used by NLS in representing monetary values.</span></span>



| <span data-ttu-id="cf902-105">Valore</span><span class="sxs-lookup"><span data-stu-id="cf902-105">Value</span></span>                   | <span data-ttu-id="cf902-106">Significato</span><span class="sxs-lookup"><span data-stu-id="cf902-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf902-107">impostazioni locali \_ SMONDECIMALSEP</span><span class="sxs-lookup"><span data-stu-id="cf902-107">LOCALE\_SMONDECIMALSEP</span></span>  | <span data-ttu-id="cf902-108">Caratteri utilizzati come separatore decimale monetario.</span><span class="sxs-lookup"><span data-stu-id="cf902-108">Character(s) used as the monetary decimal separator.</span></span> <span data-ttu-id="cf902-109">Il numero massimo di caratteri consentiti per questa stringa è quattro, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="cf902-109">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="cf902-110">Se, ad esempio, un importo monetario viene visualizzato come "$3,40", nel Stati Uniti viene visualizzato "tre dollari e 40 centesimi", quindi il separatore decimale è ".".</span><span class="sxs-lookup"><span data-stu-id="cf902-110">For example, if a monetary amount is displayed as "$3.40", just as "three dollars and forty cents" is displayed in the United States, then the monetary decimal separator is ".".</span></span>                                                                                                                                             |
| <span data-ttu-id="cf902-111">impostazioni locali \_ SMONGROUPING</span><span class="sxs-lookup"><span data-stu-id="cf902-111">LOCALE\_SMONGROUPING</span></span>    | <span data-ttu-id="cf902-112">Dimensioni di ogni gruppo di cifre monetarie a sinistra del separatore decimale.</span><span class="sxs-lookup"><span data-stu-id="cf902-112">Sizes for each group of monetary digits to the left of the decimal.</span></span> <span data-ttu-id="cf902-113">Il numero massimo di caratteri consentiti per questa stringa è dieci, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="cf902-113">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="cf902-114">Per ogni gruppo sono necessarie dimensioni esplicite e le dimensioni sono separate da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="cf902-114">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="cf902-115">Se l'ultimo valore è 0, il valore precedente viene ripetuto.</span><span class="sxs-lookup"><span data-stu-id="cf902-115">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="cf902-116">Per raggruppare le migliaia, ad esempio, specificare 3; 0.</span><span class="sxs-lookup"><span data-stu-id="cf902-116">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="cf902-117">Lingue indiane raggruppate le prime migliaia e quindi raggruppate per centinaia.</span><span class="sxs-lookup"><span data-stu-id="cf902-117">Indic languages group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="cf902-118">Ad esempio, 12, 34, 56789 è rappresentato da 3, 2; 0.</span><span class="sxs-lookup"><span data-stu-id="cf902-118">For example 12,34,56,789 is represented by 3;2;0.</span></span> |
| <span data-ttu-id="cf902-119">impostazioni locali \_ SMONTHOUSANDSEP</span><span class="sxs-lookup"><span data-stu-id="cf902-119">LOCALE\_SMONTHOUSANDSEP</span></span> | <span data-ttu-id="cf902-120">Caratteri utilizzati come separatore monetario tra i gruppi di cifre a sinistra del separatore decimale.</span><span class="sxs-lookup"><span data-stu-id="cf902-120">Character(s) used as the monetary separator between groups of digits to the left of the decimal.</span></span> <span data-ttu-id="cf902-121">Il numero massimo di caratteri consentiti per questa stringa è quattro, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="cf902-121">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="cf902-122">In genere, i gruppi rappresentano migliaia.</span><span class="sxs-lookup"><span data-stu-id="cf902-122">Typically, the groups represent thousands.</span></span> <span data-ttu-id="cf902-123">Tuttavia, a seconda del valore specificato per le impostazioni locali \_ SMONGROUPING, possono rappresentare qualcos'altro.</span><span class="sxs-lookup"><span data-stu-id="cf902-123">However, depending on the value specified for LOCALE\_SMONGROUPING, they can represent something else.</span></span>                                                                                                                                 |



 

 

 



