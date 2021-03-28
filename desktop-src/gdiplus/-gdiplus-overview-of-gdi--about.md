---
description: Windows GDI+ è il sottosistema del sistema operativo Windows XP o Windows Server 2003 responsabile della visualizzazione di informazioni su schermate e stampanti. GDI+ è un'API esposta tramite un set di classi C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Panoramica di GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994189"
---
# <a name="overview-of-gdi"></a><span data-ttu-id="612a6-104">Panoramica di GDI+</span><span class="sxs-lookup"><span data-stu-id="612a6-104">Overview of GDI+</span></span>

<span data-ttu-id="612a6-105">Windows GDI+ è il sottosistema del sistema operativo Windows XP o Windows Server 2003 responsabile della visualizzazione di informazioni su schermate e stampanti.</span><span class="sxs-lookup"><span data-stu-id="612a6-105">Windows GDI+ is the subsystem of the Windows XP operating system or Windows Server 2003 that is responsible for displaying information on screens and printers.</span></span> <span data-ttu-id="612a6-106">GDI+ è un'API esposta tramite un set di classi C++.</span><span class="sxs-lookup"><span data-stu-id="612a6-106">GDI+ is an API that is exposed through a set of C++ classes.</span></span>

<span data-ttu-id="612a6-107">Come suggerisce il nome, GDI+ è il successore di Windows Graphics Device Interface (GDI), l'interfaccia del dispositivo di grafica inclusa nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="612a6-107">As its name suggests, GDI+ is the successor to Windows Graphics Device Interface (GDI), the graphics device interface included with earlier versions of Windows.</span></span> <span data-ttu-id="612a6-108">Windows XP o Windows Server 2003 supporta GDI per la compatibilità con le applicazioni esistenti, ma i programmatori delle nuove applicazioni devono usare GDI+ per tutte le proprie esigenze grafiche, perché GDI+ ottimizza molte delle funzionalità di GDI e fornisce anche funzionalità aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="612a6-108">Windows XP or Windows Server 2003 supports GDI for compatibility with existing applications, but programmers of new applications should use GDI+ for all their graphics needs because GDI+ optimizes many of the capabilities of GDI and also provides additional features.</span></span>

<span data-ttu-id="612a6-109">Un'interfaccia del dispositivo grafica, ad esempio GDI+, consente ai programmatori di applicazioni di visualizzare informazioni su uno schermo o una stampante senza doversi preoccupare dei dettagli di un particolare dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="612a6-109">A graphics device interface, such as GDI+, allows application programmers to display information on a screen or printer without having to be concerned about the details of a particular display device.</span></span> <span data-ttu-id="612a6-110">Il programmatore di applicazioni effettua chiamate ai metodi forniti dalle classi GDI+ e tali metodi a loro volta effettuano chiamate appropriate a driver di dispositivo specifici.</span><span class="sxs-lookup"><span data-stu-id="612a6-110">The application programmer makes calls to methods provided by GDI+ classes and those methods in turn make the appropriate calls to specific device drivers.</span></span> <span data-ttu-id="612a6-111">GDI+ isola l'applicazione dall'hardware grafico ed è questo isolamento che consente agli sviluppatori di creare applicazioni indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="612a6-111">GDI+ insulates the application from the graphics hardware, and it is this insulation that allows developers to create device-independent applications.</span></span>

 

 



