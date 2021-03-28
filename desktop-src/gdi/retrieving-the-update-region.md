---
description: Le funzioni GetUpdateRect e GetUpdateRgn recuperano l'area di aggiornamento corrente per la finestra.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Recupero dell'area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226666"
---
# <a name="retrieving-the-update-region"></a><span data-ttu-id="316df-103">Recupero dell'area di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="316df-103">Retrieving the Update Region</span></span>

<span data-ttu-id="316df-104">Le funzioni [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) recuperano l'area di aggiornamento corrente per la finestra.</span><span class="sxs-lookup"><span data-stu-id="316df-104">The [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) functions retrieve the current update region for the window.</span></span> <span data-ttu-id="316df-105">GetUpdateRect Recupera il rettangolo più piccolo (nelle coordinate logiche) che racchiude l'intera area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="316df-105">GetUpdateRect retrieves the smallest rectangle (in logical coordinates) that encloses the entire update region.</span></span> <span data-ttu-id="316df-106">GetUpdateRgn recupera l'area di aggiornamento stessa.</span><span class="sxs-lookup"><span data-stu-id="316df-106">GetUpdateRgn retrieves the update region itself.</span></span> <span data-ttu-id="316df-107">Queste funzioni possono essere usate per calcolare le dimensioni correnti dell'area di aggiornamento per determinare la posizione in cui eseguire un'operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="316df-107">These functions can be used to calculate the current size of the update region to determine where to carry out a drawing operation.</span></span>

<span data-ttu-id="316df-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) recupera anche le dimensioni del rettangolo più piccolo che racchiude l'area di aggiornamento corrente, copiando le dimensioni nel membro **RcPaint** nella struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="316df-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) also retrieves the dimensions of the smallest rectangle enclosing the current update region, copying the dimensions to the **rcPaint** member in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="316df-109">Poiché **BeginPaint** convalida l'area di aggiornamento, qualsiasi chiamata a [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediatamente dopo una chiamata a **BeginPaint** restituisce un'area di aggiornamento vuota.</span><span class="sxs-lookup"><span data-stu-id="316df-109">Because **BeginPaint** validates the update region, any call to [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediately after a call to **BeginPaint** returns an empty update region.</span></span>

 

 



