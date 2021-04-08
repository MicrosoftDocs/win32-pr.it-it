---
title: Funzioni di callback yield
description: Funzioni di callback yield
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Funzioni di callback AVICap, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3666ea24a1d37402ffc13c09ca8ab95fcd19e1f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725855"
---
# <a name="yield-callback-functions"></a><span data-ttu-id="c3b3d-104">Funzioni di callback yield</span><span class="sxs-lookup"><span data-stu-id="c3b3d-104">Yield Callback Functions</span></span>

<span data-ttu-id="c3b3d-105">Le applicazioni possono usare le funzioni di callback yield durante l'acquisizione di flussi.</span><span class="sxs-lookup"><span data-stu-id="c3b3d-105">Applications can use yield callback functions during streaming capture.</span></span> <span data-ttu-id="c3b3d-106">Una funzione di callback yield è in genere costituita da un ciclo di messaggi che chiama [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)e [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage). La finestra di acquisizione chiama la funzione di callback yield almeno una volta per ogni fotogramma video acquisito, ma la velocità esatta dipende dalla frequenza dei fotogrammi e dal sovraccarico del driver e del disco di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c3b3d-106">(A yield callback function typically consists of a message loop that calls [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), and [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage).) The capture window calls the yield callback function at least once for every captured video frame, but the exact rate depends on the frame rate and the overhead of the capture driver and disk.</span></span>

 

 