---
description: Ogni volta che un'applicazione crea un controller di dominio e inizia immediatamente a chiamare le funzioni di disegno o di output GDI, sfrutta lo spazio di pagina predefinito per lo spazio del dispositivo e le trasformazioni dello spazio del dispositivo a quelle dell'area client.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Trasformazioni predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5f13c764a92c005fad36c9f2599b99a654284f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978687"
---
# <a name="default-transformations"></a><span data-ttu-id="ad3ed-103">Trasformazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="ad3ed-103">Default Transformations</span></span>

<span data-ttu-id="ad3ed-104">Ogni volta che un'applicazione crea un controller di dominio e inizia immediatamente a chiamare le funzioni di disegno o di output GDI, sfrutta lo spazio di pagina predefinito per lo spazio del dispositivo e le trasformazioni dello spazio del dispositivo a quelle dell'area client.</span><span class="sxs-lookup"><span data-stu-id="ad3ed-104">Whenever an application creates a DC and immediately begins calling GDI drawing or output functions, it takes advantage of the default page-space to device-space, and device-space to client-area transformations.</span></span> <span data-ttu-id="ad3ed-105">Non è possibile eseguire una trasformazione dello spazio globale fino a quando l'applicazione non chiama prima la funzione [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) per impostare la modalità su GM \_ Advanced, quindi chiama la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .</span><span class="sxs-lookup"><span data-stu-id="ad3ed-105">A world-to-page space transformation cannot happen until the application first calls the [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) function to set the mode to GM\_ADVANCED and then calls the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function.</span></span>

<span data-ttu-id="ad3ed-106">L'uso del \_ testo mm (la trasformazione dello spazio della pagina predefinita nella trasformazione dello spazio del dispositivo) comporta un mapping uno-a-uno, ovvero un punto specifico nello spazio della pagina viene mappato allo stesso punto nello spazio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ad3ed-106">Use of MM\_TEXT (the default page-space to device-space transformation) results in a one-to-one mapping; that is, a given point in page space maps to the same point in device space.</span></span> <span data-ttu-id="ad3ed-107">Come indicato in precedenza, questa trasformazione non è specificata da una matrice.</span><span class="sxs-lookup"><span data-stu-id="ad3ed-107">As previously mentioned, this transformation is not specified by a matrix.</span></span> <span data-ttu-id="ad3ed-108">Viene invece ottenuto dividendo la larghezza del viewport per la larghezza della finestra e l'altezza del viewport in base all'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="ad3ed-108">Instead, it is obtained by dividing the width of the viewport by the width of the window and the height of the viewport by the height of the window.</span></span> <span data-ttu-id="ad3ed-109">Nel caso predefinito, le dimensioni del viewport sono di 1 pixel per 1 pixel e le dimensioni della finestra sono unità di 1 pagina per unità di 1 pagina.</span><span class="sxs-lookup"><span data-stu-id="ad3ed-109">In the default case, the viewport dimensions are 1-pixel by 1-pixel and the window dimensions are 1-page unit by 1-page unit.</span></span>

<span data-ttu-id="ad3ed-110">La trasformazione spazio-dispositivo a dispositivo fisico (area client, desktop o carta stampante) produce sempre un mapping uno-a-uno. ovvero, un'unità nello spazio del dispositivo è sempre equivalente a un'unità nell'area client, sul desktop o in una pagina.</span><span class="sxs-lookup"><span data-stu-id="ad3ed-110">The device-space to physical-device (client area, desktop, or printer paper) transformation always results in a one-to-one mapping; that is, one unit in device space is always equivalent to one unit in the client area, on the desktop, or on a page.</span></span> <span data-ttu-id="ad3ed-111">L'unico scopo di questa trasformazione è la traduzione; garantisce che l'output venga visualizzato correttamente nella finestra di un'applicazione, indipendentemente dalla posizione in cui tale finestra viene spostata sul desktop.</span><span class="sxs-lookup"><span data-stu-id="ad3ed-111">The sole purpose of this transformation is translation; it ensures that output appears correctly in an application's window no matter where that window is moved on the desktop.</span></span>

<span data-ttu-id="ad3ed-112">L'aspetto univoco del testo MM \_ è l'orientamento dell'asse y nello spazio della pagina.</span><span class="sxs-lookup"><span data-stu-id="ad3ed-112">The one unique aspect of MM\_TEXT is the orientation of the y-axis in page space.</span></span> <span data-ttu-id="ad3ed-113">Nel \_ testo mm l'asse y positivo si estende verso il basso e l'asse y negativo si estende verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="ad3ed-113">In MM\_TEXT, the positive y-axis extends downward and the negative y-axis extends upward.</span></span>

 

 



