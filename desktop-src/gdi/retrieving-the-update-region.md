---
description: Le funzioni GetUpdateRect e GetUpdateRgn recuperano l'area di aggiornamento corrente per la finestra.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Recupero dell'area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28bf72bfcfd28ec0fc9a90485a94e19d0514bb0206de660c11a56d12f33671e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698244"
---
# <a name="retrieving-the-update-region"></a>Recupero dell'area di aggiornamento

Le [**funzioni GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) recuperano l'area di aggiornamento corrente per la finestra. GetUpdateRect recupera il rettangolo più piccolo (in coordinate logiche) che racchiude l'intera area di aggiornamento. GetUpdateRgn recupera l'area di aggiornamento stessa. Queste funzioni possono essere usate per calcolare le dimensioni correnti dell'area di aggiornamento per determinare dove eseguire un'operazione di disegno.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) recupera anche le dimensioni del rettangolo più piccolo che racchiude l'area di aggiornamento corrente, copiando le dimensioni nel membro **rcPaint** nella [**struttura PAINTSTRUCT.**](/windows/win32/api/winuser/ns-winuser-paintstruct) Poiché **BeginPaint convalida** l'area di aggiornamento, qualsiasi chiamata a [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediatamente dopo una chiamata a **BeginPaint** restituisce un'area di aggiornamento vuota.

 

 



