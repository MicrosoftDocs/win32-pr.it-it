---
description: Le funzioni seguenti forniscono supporto per più monitoraggi.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Funzioni per più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978535"
---
# <a name="multiple-display-monitors-functions"></a><span data-ttu-id="e1769-103">Funzioni per più monitor di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="e1769-103">Multiple Display Monitors Functions</span></span>

<span data-ttu-id="e1769-104">Le funzioni seguenti forniscono supporto per più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="e1769-104">The following functions provide support for multiple monitors.</span></span>



| <span data-ttu-id="e1769-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="e1769-105">Function</span></span>                                           | <span data-ttu-id="e1769-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1769-106">Description</span></span>                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1769-107">**EnumDisplayMonitors**</span><span class="sxs-lookup"><span data-stu-id="e1769-107">**EnumDisplayMonitors**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | <span data-ttu-id="e1769-108">Enumera i monitoraggi di visualizzazione che intersecano un'area costituita dall'intersezione tra un rettangolo di ritaglio specificato e l'area visibile di un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1769-108">Enumerates display monitors that intersect a region formed by the intersection of a specified clipping rectangle and the visible region of a device context.</span></span> |
| [<span data-ttu-id="e1769-109">**GetMonitorInfo**</span><span class="sxs-lookup"><span data-stu-id="e1769-109">**GetMonitorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | <span data-ttu-id="e1769-110">Recupera le informazioni su un monitor di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e1769-110">Retrieves information about a display monitor.</span></span>                                                                                                               |
| [<span data-ttu-id="e1769-111">**MonitorEnumProc**</span><span class="sxs-lookup"><span data-stu-id="e1769-111">**MonitorEnumProc**</span></span>](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | <span data-ttu-id="e1769-112">Funzione di callback definita dall'applicazione chiamata dalla funzione [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="e1769-112">An application-defined callback function that is called by the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span>                                  |
| [<span data-ttu-id="e1769-113">**MonitorFromPoint**</span><span class="sxs-lookup"><span data-stu-id="e1769-113">**MonitorFromPoint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | <span data-ttu-id="e1769-114">Recupera un handle per il monitor di visualizzazione che contiene un punto specificato.</span><span class="sxs-lookup"><span data-stu-id="e1769-114">Retrieves a handle to the display monitor that contains a specified point.</span></span>                                                                                   |
| [<span data-ttu-id="e1769-115">**MonitorFromRect**</span><span class="sxs-lookup"><span data-stu-id="e1769-115">**MonitorFromRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | <span data-ttu-id="e1769-116">Recupera un handle per il monitor di visualizzazione con l'area di intersezione più ampia con un rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="e1769-116">Retrieves a handle to the display monitor that has the largest area of intersection with a specified rectangle.</span></span>                                              |
| [<span data-ttu-id="e1769-117">**MonitorFromWindow**</span><span class="sxs-lookup"><span data-stu-id="e1769-117">**MonitorFromWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | <span data-ttu-id="e1769-118">Recupera un handle per il monitor di visualizzazione con l'area di intersezione più ampia con il rettangolo di delimitazione di una finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="e1769-118">Retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.</span></span>                       |



 

 

 



