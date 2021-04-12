---
title: Porting di applicazioni di sistema X Window
description: Porting di applicazioni di sistema X Window
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL per Windows, porting
- porting in OpenGL, X Window System
- Porting OpenGL, sistema X Window
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221527"
---
# <a name="porting-x-window-system-applications"></a><span data-ttu-id="3ae4f-106">Porting di applicazioni di sistema X Window</span><span class="sxs-lookup"><span data-stu-id="3ae4f-106">Porting X Window System Applications</span></span>

<span data-ttu-id="3ae4f-107">Analogamente a Windows, il sistema X Window è un sistema basato su messaggi di gestione degli eventi che usa i controlli e i menu della finestra.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-107">Like Windows, the X Window System is an event-handling, message-based system that uses window controls and menus.</span></span> <span data-ttu-id="3ae4f-108">Il codice OpenGL nell'applicazione di sistema X Window è probabilmente situato in aree che corrispondono approssimativamente al punto in cui verrà visualizzato quando lo si trasferisce a Windows.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-108">The OpenGL code in your X Window System application is probably located in areas that roughly correspond to where it will appear when you port it to Windows.</span></span> <span data-ttu-id="3ae4f-109">La maggior parte del codice OpenGL non cambia, ma è necessario riscrivere il codice specifico del sistema X Window.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-109">Most of your OpenGL code will not change, but you must rewrite any code that is specific to the X Window System.</span></span>

<span data-ttu-id="3ae4f-110">**Utilizzare la seguente procedura generale per trasferire i programmi OpenGL di sistema X Window a Windows**</span><span class="sxs-lookup"><span data-stu-id="3ae4f-110">**Use the following general procedure to port your X Window System OpenGL programs to Windows**</span></span>

1.  <span data-ttu-id="3ae4f-111">Riscrivere il codice specifico del sistema X Window usando il codice di Windows equivalente.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-111">Rewrite the X Window System specific code using equivalent Windows code.</span></span> <span data-ttu-id="3ae4f-112">Individuare il codice per la creazione e la gestione degli eventi della finestra.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-112">Locate window-creation and event-handling code.</span></span> <span data-ttu-id="3ae4f-113">Il sistema della finestra X e le finestre sono sistemi di gestione degli eventi, basati su messaggi, che semplificano la determinazione del punto in cui apportare le modifiche appropriate.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-113">The X Window System and Windows are event-handling, message-based windowing systems, which makes it easier to determine where to make the appropriate changes.</span></span> <span data-ttu-id="3ae4f-114">Tuttavia, in particolare per le applicazioni di grandi dimensioni, la riscrittura di un'applicazione da un sistema operativo a un altro può essere un'impresa complessa e difficile.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-114">(However, especially for large applications, rewriting an application from one operating system to another can be a complex and difficult undertaking.)</span></span>
2.  <span data-ttu-id="3ae4f-115">Individuare il codice che utilizza le funzioni GLX.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-115">Locate any code that uses GLX functions.</span></span> <span data-ttu-id="3ae4f-116">Queste sono le funzioni che verranno convertite nelle funzioni Windows equivalenti.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-116">These are the functions you'll translate to their equivalent Windows functions.</span></span>
3.  <span data-ttu-id="3ae4f-117">Trasla le funzioni di formato pixel GLX e funzioni visive/ridotte nel formato Windows/OpenGL pixel appropriato e nelle funzioni di contesto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-117">Translate GLX pixel format functions and Visual/Drawable functions to appropriate Windows/OpenGL pixel format and device context functions.</span></span>
4.  <span data-ttu-id="3ae4f-118">Tradurre le funzioni del contesto di rendering GLX in funzioni di contesto di rendering Windows/OpenGL.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-118">Translate GLX rendering context functions to Windows/OpenGL rendering context functions.</span></span>
5.  <span data-ttu-id="3ae4f-119">Trasla le funzioni GLX pixmap in funzioni Windows equivalenti.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-119">Translate GLX Pixmap functions to equivalent Windows functions.</span></span>
6.  <span data-ttu-id="3ae4f-120">Tradurre il framebuffer GLX e altre funzioni GLX nelle funzioni di Windows appropriate.</span><span class="sxs-lookup"><span data-stu-id="3ae4f-120">Translate GLX framebuffer and other GLX functions to the appropriate Windows functions.</span></span>

 

 




