---
description: impostazioni locali \_ SGROUPING
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968759"
---
# <a name="locale_sgrouping"></a><span data-ttu-id="3f4dc-103">impostazioni locali \_ SGROUPING</span><span class="sxs-lookup"><span data-stu-id="3f4dc-103">LOCALE\_SGROUPING</span></span>

<span data-ttu-id="3f4dc-104">Dimensioni di ogni gruppo di cifre a sinistra del separatore decimale.</span><span class="sxs-lookup"><span data-stu-id="3f4dc-104">Sizes for each group of digits to the left of the decimal.</span></span> <span data-ttu-id="3f4dc-105">Il numero massimo di caratteri consentiti per questa stringa è dieci, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="3f4dc-105">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="3f4dc-106">Per ogni gruppo sono necessarie dimensioni esplicite e le dimensioni sono separate da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="3f4dc-106">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="3f4dc-107">Se l'ultimo valore è 0, il valore precedente viene ripetuto.</span><span class="sxs-lookup"><span data-stu-id="3f4dc-107">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="3f4dc-108">Per raggruppare le migliaia, ad esempio, specificare 3; 0.</span><span class="sxs-lookup"><span data-stu-id="3f4dc-108">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="3f4dc-109">Le impostazioni locali indiane raggruppano le prime migliaia e quindi raggruppate per centinaia.</span><span class="sxs-lookup"><span data-stu-id="3f4dc-109">Indic locales group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="3f4dc-110">Ad esempio, 12, 34, 56789 è rappresentato da 3, 2; 0.</span><span class="sxs-lookup"><span data-stu-id="3f4dc-110">For example, 12,34,56,789 is represented by 3;2;0.</span></span>

<span data-ttu-id="3f4dc-111">Altri esempi:</span><span class="sxs-lookup"><span data-stu-id="3f4dc-111">Further examples:</span></span>



| <span data-ttu-id="3f4dc-112">Specifiche</span><span class="sxs-lookup"><span data-stu-id="3f4dc-112">Specification</span></span> | <span data-ttu-id="3f4dc-113">Stringa risultante</span><span class="sxs-lookup"><span data-stu-id="3f4dc-113">Resulting string</span></span>   |
|---------------|--------------------|
| <span data-ttu-id="3f4dc-114">3; 0</span><span class="sxs-lookup"><span data-stu-id="3f4dc-114">3;0</span></span>           | <span data-ttu-id="3f4dc-115">3 mila miliardi</span><span class="sxs-lookup"><span data-stu-id="3f4dc-115">3,000,000,000,000</span></span>  |
| <span data-ttu-id="3f4dc-116">3; 2; 0</span><span class="sxs-lookup"><span data-stu-id="3f4dc-116">3;2;0</span></span>         | <span data-ttu-id="3f4dc-117">30, 00, 00, 00, 00000</span><span class="sxs-lookup"><span data-stu-id="3f4dc-117">30,00,00,00,00,000</span></span> |
| <span data-ttu-id="3f4dc-118">3</span><span class="sxs-lookup"><span data-stu-id="3f4dc-118">3</span></span>             | <span data-ttu-id="3f4dc-119">3 mila miliardi</span><span class="sxs-lookup"><span data-stu-id="3f4dc-119">3000000000,000</span></span>     |
| <span data-ttu-id="3f4dc-120">3; 2</span><span class="sxs-lookup"><span data-stu-id="3f4dc-120">3;2</span></span>           | <span data-ttu-id="3f4dc-121">30000000, 00000</span><span class="sxs-lookup"><span data-stu-id="3f4dc-121">30000000,00,000</span></span>    |



 

 

 



