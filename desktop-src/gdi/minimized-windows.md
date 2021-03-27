---
description: Il sistema riduce la finestra principale di un'applicazione (stile sovrapposto) a una finestra ridotta a icona quando l'utente fa clic su Riduci a icona dal menu finestra o l'applicazione chiama la funzione ShowWindow e specifica un valore come SW \_ Riduci a icona.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Finestre ridotte a icona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754378"
---
# <a name="minimized-windows"></a><span data-ttu-id="fdf0a-103">Finestre ridotte a icona</span><span class="sxs-lookup"><span data-stu-id="fdf0a-103">Minimized Windows</span></span>

<span data-ttu-id="fdf0a-104">Il sistema riduce la finestra principale di un'applicazione (stile sovrapposto) a una finestra ridotta a icona quando l'utente fa clic su Riduci a icona dal menu finestra o l'applicazione chiama la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) e specifica un valore come SW \_ Riduci a icona.</span><span class="sxs-lookup"><span data-stu-id="fdf0a-104">The system reduces an application's main window (overlapping style) to a minimized window when the user clicks Minimize from the window menu or the application calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function and specifies a value such as SW\_MINIMIZE.</span></span> <span data-ttu-id="fdf0a-105">Per ridurre al minimo una finestra, è possibile velocizzare le prestazioni del sistema riducendo la quantità di lavoro che un'applicazione deve eseguire durante l'aggiornamento della finestra principale.</span><span class="sxs-lookup"><span data-stu-id="fdf0a-105">Minimizing a window speeds up system performance by reducing the amount of work an application must do when updating its main window.</span></span>

<span data-ttu-id="fdf0a-106">Per un'applicazione tipica, il sistema disegna un'icona, denominata icona della classe, quando la finestra è ridotta a icona, etichettando l'icona con il nome della finestra.</span><span class="sxs-lookup"><span data-stu-id="fdf0a-106">For a typical application, the system draws an icon, called the class icon, when the window is minimized, labeling the icon with the name of the window.</span></span> <span data-ttu-id="fdf0a-107">L'icona della classe, un'immagine statica che rappresenta l'applicazione, viene specificata dall'applicazione quando registra la classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="fdf0a-107">The class icon, a static image that represents the application, is specified by the application when it registers the window class.</span></span> <span data-ttu-id="fdf0a-108">L'applicazione assegna un handle all'icona della classe al membro **HICON** di [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) prima di chiamare [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="fdf0a-108">The application assigns a handle to the class icon to the **hIcon** member of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) before calling [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="fdf0a-109">L'applicazione può usare la funzione [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) per recuperare l'handle dell'icona.</span><span class="sxs-lookup"><span data-stu-id="fdf0a-109">The application can use the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to retrieve the icon handle.</span></span>

 

 
