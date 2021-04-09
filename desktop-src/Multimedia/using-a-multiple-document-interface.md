---
title: Uso di un'interfaccia a documenti multipli
description: Uso di un'interfaccia a documenti multipli
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- MCIWndRegisterClass (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872457"
---
# <a name="using-a-multiple-document-interface"></a><span data-ttu-id="a81d6-104">Uso di un'interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="a81d6-104">Using a Multiple Document Interface</span></span>

<span data-ttu-id="a81d6-105">Le applicazioni che usano un'interfaccia a documenti multipli (MDI) potrebbero dover specificare gli stili della finestra che non sono disponibili tramite la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="a81d6-105">Applications that use a multiple document interface (MDI) might need to specify window styles that are not available through the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span> <span data-ttu-id="a81d6-106">Per queste applicazioni, è possibile registrare e creare una finestra MCIWnd usando la funzione [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) con la funzione [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="a81d6-106">For these applications, you can register and create an MCIWnd window by using the [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) function with the [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="a81d6-107">La funzione **MCIWndRegisterClass** registra la \_ classe della finestra della classe della finestra MCIWND \_ e quindi **CreateWindowEx** crea un'istanza di una finestra MCIWND.</span><span class="sxs-lookup"><span data-stu-id="a81d6-107">The **MCIWndRegisterClass** function registers the MCIWND\_WINDOW\_CLASS window class and then **CreateWindowEx** creates an instance of an MCIWnd window.</span></span>

 

 