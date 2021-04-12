---
title: Matrici di caratteri conteggiate
description: L'attributo \ size \_ is \ indica il limite superiore della matrice mentre l'attributo \ length \_ indica il numero di elementi della matrice da trasmettere.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473646"
---
# <a name="counted-character-arrays"></a><span data-ttu-id="492fb-103">Matrici di caratteri conteggiate</span><span class="sxs-lookup"><span data-stu-id="492fb-103">Counted Character Arrays</span></span>

<span data-ttu-id="492fb-104">L' \[ [attributo \_ size](/windows/desktop/Midl/size-is) \] indica il limite superiore della matrice mentre l' \[ attributo [length \_ ](/windows/desktop/Midl/length-is) \] indica il numero di elementi della matrice da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="492fb-104">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute indicates the upper bound of the array while the \[ [length\_is](/windows/desktop/Midl/length-is)\] attribute indicates the number of array elements to transmit.</span></span> <span data-ttu-id="492fb-105">Oltre alla matrice, il prototipo di procedura remota deve includere tutte le variabili che rappresentano la lunghezza o la dimensione che determinano gli elementi di matrice trasmessi (possono essere parametri separati o aggregati con la stringa in una struttura).</span><span class="sxs-lookup"><span data-stu-id="492fb-105">In addition to the array, the remote procedure prototype must include any variables representing length or size that determine the transmitted array elements (they can be separate parameters or bundled with the string in a structure).</span></span> <span data-ttu-id="492fb-106">Questi attributi possono essere usati con matrici di caratteri wide o a byte singolo come se fossero con matrici di altri tipi.</span><span class="sxs-lookup"><span data-stu-id="492fb-106">These attributes can be used with wide-character or single-byte character arrays just as they would be with arrays of other types.</span></span>

<span data-ttu-id="492fb-107">Le informazioni contenute in questa sezione descrivono i prototipi di parametri di procedura remota per le matrici di caratteri.</span><span class="sxs-lookup"><span data-stu-id="492fb-107">The information in this section describes remote procedure parameter prototypes for character arrays.</span></span> <span data-ttu-id="492fb-108">È divisa negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="492fb-108">It is divided into the following topics:</span></span>

-   <span data-ttu-id="492fb-109">[\[in, out, dimensioni \_ è un \] prototipo](-in-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="492fb-109">[\[in, out, size\_is\] Prototype](-in-out-size-is-prototype.md)</span></span>
-   <span data-ttu-id="492fb-110">[\[in, Size \_ is e out, Size \_ è \] Prototype](-in-size-is-and-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="492fb-110">[\[in, size\_is and out, size\_is\] Prototype](-in-size-is-and-out-size-is-prototype.md)</span></span>

 

 