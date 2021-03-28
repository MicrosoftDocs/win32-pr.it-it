---
description: L'attributo color specifica il colore della penna.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Colore della penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d831994ac444207832574dc104a9d5c2582db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528302"
---
# <a name="pen-color"></a><span data-ttu-id="92d1e-103">Colore della penna</span><span class="sxs-lookup"><span data-stu-id="92d1e-103">Pen Color</span></span>

<span data-ttu-id="92d1e-104">L'attributo color specifica il colore della penna.</span><span class="sxs-lookup"><span data-stu-id="92d1e-104">The color attribute specifies the pen's color.</span></span> <span data-ttu-id="92d1e-105">Un'applicazione può creare una penna cosmetica con un colore univoco usando la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) per archiviare la tripletta rossa, verde, blu che specifica il colore desiderato in una struttura [COLORREF](colorref.md) e passando l'indirizzo della struttura alla funzione [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="92d1e-105">An application can create a cosmetic pen with a unique color by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro to store the red, green, blue triplet that specifies the desired color in a [COLORREF](colorref.md) structure and passing this structure's address to the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="92d1e-106">Le penne azionarie sono limitate a nero, bianco e invisibile. Per ulteriori informazioni sui triple e sui colori RGB, vedere [colori](colors.md).</span><span class="sxs-lookup"><span data-stu-id="92d1e-106">(The stock pens are limited to black, white, and invisible.) For more information about RGB triplets and color, see [Colors](colors.md).</span></span>

 

 



