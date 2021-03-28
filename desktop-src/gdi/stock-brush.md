---
description: Sono disponibili sette pennelli logici predefiniti gestiti dall'interfaccia GDI (Graphics Device Interface). Sono presenti anche 21 pennelli logici predefiniti gestiti dall'interfaccia di gestione della finestra (USER).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Pennello azionario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980527"
---
# <a name="stock-brush"></a><span data-ttu-id="ce89c-104">Pennello azionario</span><span class="sxs-lookup"><span data-stu-id="ce89c-104">Stock Brush</span></span>

<span data-ttu-id="ce89c-105">Sono disponibili sette pennelli logici predefiniti gestiti dall'interfaccia GDI (Graphics Device Interface).</span><span class="sxs-lookup"><span data-stu-id="ce89c-105">There are seven predefined logical stock brushes maintained by the graphics device interface (GDI).</span></span> <span data-ttu-id="ce89c-106">Sono presenti anche 21 pennelli logici predefiniti gestiti dall'interfaccia di gestione della finestra (USER).</span><span class="sxs-lookup"><span data-stu-id="ce89c-106">There are also 21 predefined logical stock brushes maintained by the window management interface (USER).</span></span>

<span data-ttu-id="ce89c-107">Nella figura seguente sono illustrati i rettangoli disegnati usando i sette pennelli predefiniti.</span><span class="sxs-lookup"><span data-stu-id="ce89c-107">The following illustration shows rectangles painted by using the seven predefined stock brushes.</span></span>

![illustrazione che mostra sette caselle: una nera, tre tonalità di grigio e tre che risultano vuote](images/csbru-03.png)

<span data-ttu-id="ce89c-109">Un'applicazione può recuperare un handle che identifica uno dei sette pennelli azionari chiamando la funzione [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) , specificando il tipo di pennello.</span><span class="sxs-lookup"><span data-stu-id="ce89c-109">An application can retrieve a handle identifying one of the seven stock brushes by calling the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function, specifying the brush type.</span></span>

<span data-ttu-id="ce89c-110">I 21 pennelli azionari gestiti dall'interfaccia di gestione della finestra corrispondono ai colori degli elementi della finestra quali menu, barre di scorrimento e pulsanti.</span><span class="sxs-lookup"><span data-stu-id="ce89c-110">The 21 stock brushes maintained by the window management interface correspond to the colors of window elements such as menus, scroll bars, and buttons.</span></span> <span data-ttu-id="ce89c-111">Un'applicazione può ottenere un handle che identifica uno di questi pennelli chiamando la funzione [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) e specificando un valore di colore di sistema.</span><span class="sxs-lookup"><span data-stu-id="ce89c-111">An application can obtain a handle identifying one of these brushes by calling the [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) function and specifying a system-color value.</span></span> <span data-ttu-id="ce89c-112">Un'applicazione può recuperare il colore corrispondente a un particolare elemento della finestra chiamando la funzione [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) .</span><span class="sxs-lookup"><span data-stu-id="ce89c-112">An application can retrieve the color corresponding to a particular window element by calling the [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) function.</span></span> <span data-ttu-id="ce89c-113">Un'applicazione può impostare il colore corrispondente a un elemento della finestra chiamando la funzione [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="ce89c-113">An application can set the color corresponding to a window element by calling the [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) function.</span></span>

 

 
