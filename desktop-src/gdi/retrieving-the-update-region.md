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
# <a name="retrieving-the-update-region"></a>Recupero dell'area di aggiornamento

Le funzioni [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) recuperano l'area di aggiornamento corrente per la finestra. GetUpdateRect Recupera il rettangolo più piccolo (nelle coordinate logiche) che racchiude l'intera area di aggiornamento. GetUpdateRgn recupera l'area di aggiornamento stessa. Queste funzioni possono essere usate per calcolare le dimensioni correnti dell'area di aggiornamento per determinare la posizione in cui eseguire un'operazione di disegno.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) recupera anche le dimensioni del rettangolo più piccolo che racchiude l'area di aggiornamento corrente, copiando le dimensioni nel membro **RcPaint** nella struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) . Poiché **BeginPaint** convalida l'area di aggiornamento, qualsiasi chiamata a [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediatamente dopo una chiamata a **BeginPaint** restituisce un'area di aggiornamento vuota.

 

 



