---
title: Informazioni sull'I/O dei file multimediali
description: Informazioni sull'I/O dei file multimediali
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Multimedia di Windows, I/O file
- Multimedia, I/O file
- input multimediale, I/O file
- I/O file multimediale, informazioni
- I/O di file, informazioni
- input e output (I/O), informazioni
- I/O (input e output), informazioni
- I/O di base
- formato file di interscambio risorse (RIFF)
- RIFF (formato file di interscambio risorse)
- I/O RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298261"
---
# <a name="about-multimedia-file-io"></a><span data-ttu-id="ac133-114">Informazioni sull'I/O dei file multimediali</span><span class="sxs-lookup"><span data-stu-id="ac133-114">About Multimedia File I/O</span></span>

<span data-ttu-id="ac133-115">Per la maggior parte delle applicazioni multimediali è necessario l'input e l'output (I/O) del file, ovvero la possibilità di creare, leggere e scrivere file su disco.</span><span class="sxs-lookup"><span data-stu-id="ac133-115">Most multimedia applications require file input and output (I/O) — that is, the ability to create, read, and write disk files.</span></span> <span data-ttu-id="ac133-116">I servizi di I/O dei file multimediali forniscono I/O di file memorizzati nel buffer e non memorizzati nel buffer e supportano i file RIFF.</span><span class="sxs-lookup"><span data-stu-id="ac133-116">Multimedia file I/O services provide buffered and unbuffered file I/O and support for RIFF files.</span></span> <span data-ttu-id="ac133-117">I servizi sono estendibili con procedure di I/O personalizzate che possono essere condivise tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ac133-117">The services are extensible with custom I/O procedures that can be shared among applications.</span></span>

<span data-ttu-id="ac133-118">Per la maggior parte delle applicazioni sono necessari solo i servizi di I/O dei file di base e i servizi di I/O file di RIFF.</span><span class="sxs-lookup"><span data-stu-id="ac133-118">Most applications need only the basic file I/O services and the RIFF file I/O services.</span></span> <span data-ttu-id="ac133-119">Le applicazioni sensibili alle prestazioni di I/O dei file, ad esempio le applicazioni che trasmettono i dati da Compact Disk in tempo reale, possono ottimizzare le prestazioni usando i servizi per accedere direttamente al buffer di I/O dei file.</span><span class="sxs-lookup"><span data-stu-id="ac133-119">Applications sensitive to file I/O performance, such as applications that stream data from compact disc in real time, can optimize performance by using services to directly access the file I/O buffer.</span></span> <span data-ttu-id="ac133-120">Le applicazioni che accedono a sistemi di archiviazione personalizzati, ad esempio archivi di file e database, possono fornire una propria procedura di I/O che legge e scrive elementi del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ac133-120">Applications that access custom storage systems, such as file archives and databases, can provide their own I/O procedure that reads and writes elements of the storage system.</span></span>

 

 




