---
description: Quando si usa un'interfaccia Windows Image Acquisition (WIA) in più thread all'interno di un singolo processo, un'applicazione deve fornire il marshalling per tale interfaccia.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Uso di più thread in un'applicazione WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129390"
---
# <a name="using-multiple-threads-in-a-wia-application"></a><span data-ttu-id="1e374-103">Uso di più thread in un'applicazione WIA</span><span class="sxs-lookup"><span data-stu-id="1e374-103">Using Multiple Threads in a WIA Application</span></span>

<span data-ttu-id="1e374-104">Quando si usa un'interfaccia Windows Image Acquisition (WIA) in più thread all'interno di un singolo processo, un'applicazione deve fornire il marshalling per tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1e374-104">When using a Windows Image Acquisition (WIA) interface in more than one thread within a single process, an application must provide marshalling for that interface.</span></span> <span data-ttu-id="1e374-105">Se un thread crea un puntatore a interfaccia, non è possibile utilizzare tale puntatore in un thread diverso senza eseguire il marshalling.</span><span class="sxs-lookup"><span data-stu-id="1e374-105">If one thread creates an interface pointer, you cannot use that pointer in a different thread without marshalling.</span></span>

<span data-ttu-id="1e374-106">Se, ad esempio, un thread in un'applicazione ottiene un puntatore all'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) , un thread separato non può utilizzare tale puntatore di interfaccia senza marshalling.</span><span class="sxs-lookup"><span data-stu-id="1e374-106">For example, if one thread in an application obtains a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface, a separate thread cannot use that interface pointer without marshalling.</span></span>

<span data-ttu-id="1e374-107">Una tecnica comune utilizzata per eseguire questo marshalling consiste nell'utilizzare la tabella dell'interfaccia globale.</span><span class="sxs-lookup"><span data-stu-id="1e374-107">A common technique used to accomplish this marshalling is to use the global interface table.</span></span> <span data-ttu-id="1e374-108">La tabella dell'interfaccia globale è una tabella mantenuta in tutti i thread all'interno di un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="1e374-108">The global interface table is a table maintained across all threads within a single process.</span></span> <span data-ttu-id="1e374-109">Tutti i thread in esecuzione nel processo possono recuperare le interfacce registrate nella tabella dell'interfaccia globale.</span><span class="sxs-lookup"><span data-stu-id="1e374-109">All threads running within the process can retrieve interfaces that are registered to the global interface table.</span></span> <span data-ttu-id="1e374-110">Questa tecnica evita la necessità di creare flussi per il passaggio di interfacce tra thread.</span><span class="sxs-lookup"><span data-stu-id="1e374-110">This technique avoids the need to create streams for passing interfaces between threads.</span></span>

<span data-ttu-id="1e374-111">Per informazioni sull'uso della tabella dell'interfaccia globale, vedere [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="1e374-111">For information on how to use the global interface table, see [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="1e374-112">Anche se non si prevede di usare più thread in un'applicazione WIA, è necessario presupporre che tutte le funzioni di callback degli eventi di trasferimento dati o del dispositivo vengano eseguite in thread distinti.</span><span class="sxs-lookup"><span data-stu-id="1e374-112">Even if you do not intend to use multiple threads in a WIA application, you must assume that all data transfer or device event callback functions run in separate threads.</span></span>

 

 
