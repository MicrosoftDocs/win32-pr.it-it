---
description: Per modificare un'immagine archiviata in un metafile avanzato, è necessario che un'applicazione esegua le attività descritte nella procedura seguente.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Modifica di un metafile avanzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130783"
---
# <a name="editing-an-enhanced-metafile"></a><span data-ttu-id="69d5e-103">Modifica di un metafile avanzato</span><span class="sxs-lookup"><span data-stu-id="69d5e-103">Editing an Enhanced Metafile</span></span>

<span data-ttu-id="69d5e-104">Per modificare un'immagine archiviata in un metafile avanzato, è necessario che un'applicazione esegua le attività descritte nella procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="69d5e-104">To edit a picture stored in an enhanced metafile, an application must perform the tasks described in the following procedure.</span></span>

<span data-ttu-id="69d5e-105">**Per modificare un'immagine archiviata in un metafile avanzato**</span><span class="sxs-lookup"><span data-stu-id="69d5e-105">**To edit a picture stored in an enhanced metafile**</span></span>

1.  <span data-ttu-id="69d5e-106">Usare hit testing per acquisire le coordinate del cursore e recuperare la posizione dell'oggetto (riga, arco, rettangolo, ellisse, poligono o forma irregolare) che l'utente vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="69d5e-106">Use hit-testing to capture the cursor coordinates and retrieve the position of the object (line, arc, rectangle, ellipse, polygon, or irregular shape) that the user wants to alter.</span></span>
2.  <span data-ttu-id="69d5e-107">Convertire queste coordinate in unità logiche (o internazionali).</span><span class="sxs-lookup"><span data-stu-id="69d5e-107">Convert these coordinates to logical (or world) units.</span></span>
3.  <span data-ttu-id="69d5e-108">Chiamare la funzione [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) ed esaminare ogni record del metafile.</span><span class="sxs-lookup"><span data-stu-id="69d5e-108">Call the [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) function and examine each metafile record.</span></span>
4.  <span data-ttu-id="69d5e-109">Determinare se un record specificato corrisponde a una funzione di disegno GDI.</span><span class="sxs-lookup"><span data-stu-id="69d5e-109">Determine whether a given record corresponds to a GDI drawing function.</span></span>
5.  <span data-ttu-id="69d5e-110">In caso contrario, determinare se le coordinate archiviate nel record corrispondono alla riga, all'arco, all'ellisse o ad altro elemento grafico che interseca le coordinate specificate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="69d5e-110">If it does, determine whether the coordinates stored in the record correspond to the line, arc, ellipse, or other graphics element that intersects the coordinates specified by the user.</span></span>
6.  <span data-ttu-id="69d5e-111">Quando si trova il record che corrisponde all'output che l'utente vuole modificare, cancellare l'oggetto sullo schermo che corrisponde al record originale.</span><span class="sxs-lookup"><span data-stu-id="69d5e-111">Upon finding the record that corresponds to the output that the user wants to alter, erase the object on the screen that corresponds to the original record.</span></span>
7.  <span data-ttu-id="69d5e-112">Eliminare il record corrispondente dal metafile, salvando un puntatore nella relativa posizione.</span><span class="sxs-lookup"><span data-stu-id="69d5e-112">Delete the corresponding record from the metafile, saving a pointer to its location.</span></span>
8.  <span data-ttu-id="69d5e-113">Consente all'utente di ricreare o sostituire l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="69d5e-113">Permit the user to redraw or replace the object.</span></span>
9.  <span data-ttu-id="69d5e-114">Converte le funzioni GDI utilizzate per creare il nuovo oggetto in uno o più record di metafile avanzati.</span><span class="sxs-lookup"><span data-stu-id="69d5e-114">Convert the GDI functions used to draw the new object into one or more enhanced-metafile records.</span></span>
10. <span data-ttu-id="69d5e-115">Archiviare questi record nel metafile avanzato.</span><span class="sxs-lookup"><span data-stu-id="69d5e-115">Store these records in the enhanced metafile.</span></span>

 

 



