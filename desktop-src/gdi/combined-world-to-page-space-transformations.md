---
description: Le cinque trasformazioni da mondo a pagina possono essere combinate in una singola matrice 3 per 3.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Trasformazioni di spazi globali combinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978730"
---
# <a name="combined-world-to-page-space-transformations"></a><span data-ttu-id="9367f-103">Trasformazioni di spazi globali combinate</span><span class="sxs-lookup"><span data-stu-id="9367f-103">Combined World-to-Page Space Transformations</span></span>

<span data-ttu-id="9367f-104">Le cinque trasformazioni da mondo a pagina possono essere combinate in una singola matrice 3 per 3.</span><span class="sxs-lookup"><span data-stu-id="9367f-104">The five world-to-page transformations can be combined into a single 3-by-3 matrix.</span></span> <span data-ttu-id="9367f-105">La funzione [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) può essere usata per combinare due trasformazioni dello spazio globale per la pagina.</span><span class="sxs-lookup"><span data-stu-id="9367f-105">The [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) function can be used to combine two world-space to page-space transformations.</span></span> <span data-ttu-id="9367f-106">Le trasformazioni combinate possono essere usate per modificare l'output associato a un particolare contesto di dispositivo (DC) chiamando la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) e fornendo gli elementi per questa matrice.</span><span class="sxs-lookup"><span data-stu-id="9367f-106">The combined transformations can be used to alter output associated with a particular device context (DC) by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function and supplying the elements for this matrix.</span></span> <span data-ttu-id="9367f-107">Quando un'applicazione chiama **SetWorldTransform**, archivia gli elementi della matrice 3 per 3 [**in una struttura**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="9367f-107">When an application calls **SetWorldTransform**, it stores the elements of the 3-by-3 matrix in an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span> <span data-ttu-id="9367f-108">I membri di questa struttura corrispondono alle prime due colonne di una matrice 3 per 3. L'ultima colonna della matrice non è obbligatoria perché i relativi valori sono costanti.</span><span class="sxs-lookup"><span data-stu-id="9367f-108">The members of this structure correspond to the first two columns of a 3-by-3 matrix; the last column of the matrix is not required because its values are constant.</span></span>

<span data-ttu-id="9367f-109">Gli elementi della matrice di trasformazione globale corrente possono essere riattivati chiamando la funzione [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) e specificando un puntatore a una [**struttura di**](/windows/win32/api/wingdi/ns-wingdi-xform) un elemento di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="9367f-109">The elements of the current world transformation matrix can be revived by calling the [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) function and supplying a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

 



