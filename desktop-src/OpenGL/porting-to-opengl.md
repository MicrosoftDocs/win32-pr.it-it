---
title: Porting in OpenGL
description: Porting in OpenGL
ms.assetid: 6799e10b-2f7c-4516-92ea-43667784f8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8efd2a34ac5d7fb6fc52aef3f24a556712b2c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396319"
---
# <a name="porting-to-opengl"></a><span data-ttu-id="9a81b-103">Porting in OpenGL</span><span class="sxs-lookup"><span data-stu-id="9a81b-103">Porting to OpenGL</span></span>

<span data-ttu-id="9a81b-104">OpenGL è progettato per la compatibilità tra l'hardware e i sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="9a81b-104">OpenGL is designed for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="9a81b-105">Questa progettazione rende più semplice per i programmatori trasferire i programmi OpenGL da un sistema a un altro.</span><span class="sxs-lookup"><span data-stu-id="9a81b-105">This design makes it easier for programmers to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="9a81b-106">Sebbene ogni sistema operativo abbia requisiti specifici, la maggior parte del codice OpenGL nei programmi correnti può essere usata così com'è.</span><span class="sxs-lookup"><span data-stu-id="9a81b-106">While each operating system has unique requirements, much of the OpenGL code in your current programs can be used as is.</span></span> <span data-ttu-id="9a81b-107">Per trasferire l'applicazione OpenGL in Microsoft Windows, è necessario modificare i programmi per l'uso con i sistemi Windows windowing.</span><span class="sxs-lookup"><span data-stu-id="9a81b-107">To port your OpenGL application to Microsoft Windows, you'll have to modify your programs to work with the Windows windowing systems.</span></span>

<span data-ttu-id="9a81b-108">In generale, le applicazioni vengono trasferite in OpenGL per Windows da una delle due piattaforme seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a81b-108">In general applications are ported to OpenGL for Windows from one of two platforms:</span></span>

-   <span data-ttu-id="9a81b-109">Applicazioni OpenGL sviluppate per il sistema X Window e la libreria X (Xlib)</span><span class="sxs-lookup"><span data-stu-id="9a81b-109">OpenGL applications developed for the X Window System and the X library (Xlib)</span></span>
-   <span data-ttu-id="9a81b-110">Applicazioni IRIS GL</span><span class="sxs-lookup"><span data-stu-id="9a81b-110">IRIS GL applications</span></span>

<span data-ttu-id="9a81b-111">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="9a81b-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9a81b-112">Introduzione al porting in OpenGL per Windows</span><span class="sxs-lookup"><span data-stu-id="9a81b-112">Introduction to Porting to OpenGL for Windows</span></span>](introduction-to-porting-to-opengl-for-windows-nt--windows-2000--and-windows-95-98.md)
-   [<span data-ttu-id="9a81b-113">Funzioni OpenGL e rispettivi equivalenti IRIS GL</span><span class="sxs-lookup"><span data-stu-id="9a81b-113">OpenGL Functions and Their IRIS GL Equivalents</span></span>](opengl-functions-and-their-iris-gl-equivalents.md)
-   [<span data-ttu-id="9a81b-114">Differenze tra IRIS GL e OpenGL</span><span class="sxs-lookup"><span data-stu-id="9a81b-114">IRIS GL and OpenGL Differences</span></span>](iris-gl-and-opengl-differences.md)

 

 




