---
description: Per migliorare le prestazioni, non è possibile serializzare l'accesso a oggetti GDI (Graphics Device Interface), ad esempio tavolozze, contesti di dispositivo, aree e così come.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Più thread e oggetti GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311983"
---
# <a name="multiple-threads-and-gdi-objects"></a><span data-ttu-id="c10b8-103">Più thread e oggetti GDI</span><span class="sxs-lookup"><span data-stu-id="c10b8-103">Multiple Threads and GDI Objects</span></span>

<span data-ttu-id="c10b8-104">Per migliorare le prestazioni, non è possibile serializzare l'accesso a oggetti GDI (Graphics Device Interface), ad esempio tavolozze, contesti di dispositivo, aree e così come.</span><span class="sxs-lookup"><span data-stu-id="c10b8-104">To enhance performance, access to graphics device interface (GDI) objects (such as palettes, device contexts, regions, and the like) is not serialized.</span></span> <span data-ttu-id="c10b8-105">Ciò crea un rischio potenziale per i processi con più thread che condividono questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="c10b8-105">This creates a potential danger for processes that have multiple threads sharing these objects.</span></span> <span data-ttu-id="c10b8-106">Se, ad esempio, un thread elimina un oggetto GDI mentre viene utilizzato da un altro thread, i risultati sono imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="c10b8-106">For example, if one thread deletes a GDI object while another thread is using it, the results are unpredictable.</span></span> <span data-ttu-id="c10b8-107">Questo pericolo può essere evitato semplicemente non condividendo oggetti GDI.</span><span class="sxs-lookup"><span data-stu-id="c10b8-107">This danger can be avoided simply by not sharing GDI objects.</span></span> <span data-ttu-id="c10b8-108">Se la condivisione è inevitabile (o auspicabile), l'applicazione deve fornire i propri meccanismi per la sincronizzazione dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="c10b8-108">If sharing is unavoidable (or desirable), the application must provide its own mechanisms for synchronizing access.</span></span> <span data-ttu-id="c10b8-109">Per ulteriori informazioni sulla sincronizzazione dell'accesso, vedere [sincronizzazione dell'esecuzione di più thread](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="c10b8-109">For more information about synchronizing access, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

 

 



