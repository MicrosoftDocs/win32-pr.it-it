---
description: 'Altre informazioni su: esplorazione di un albero di oggetti elemento'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Esplorazione di un albero di oggetti Item
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307344"
---
# <a name="navigating-a-tree-of-item-objects"></a><span data-ttu-id="00fae-103">Esplorazione di un albero di oggetti Item</span><span class="sxs-lookup"><span data-stu-id="00fae-103">Navigating a Tree of Item Objects</span></span>

> [!Note]  
> <span data-ttu-id="00fae-104">Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="00fae-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="00fae-105">Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="00fae-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="00fae-106">Un'applicazione o uno script consente di spostarsi in un albero degli elementi del dispositivo Windows Image Acquisition (WIA) per individuare e selezionare le immagini nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00fae-106">An application or script navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="00fae-107">Utilizzando questa tecnica, un'applicazione seleziona e acquisisce un'immagine senza utilizzare una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="00fae-107">Using this technique, an application selects and acquires an image without the use of a dialog box.</span></span>

<span data-ttu-id="00fae-108">Un dispositivo WIA viene rappresentato come elemento radice in una struttura ad albero di oggetti [**elemento**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="00fae-108">A WIA device is represented as the root item in a tree of [**Item**](-wia-item.md) objects.</span></span> <span data-ttu-id="00fae-109">Gli elementi figlio nell'albero rappresentano cartelle e immagini per una fotocamera o i letti digitalizzazione per uno scanner.</span><span class="sxs-lookup"><span data-stu-id="00fae-109">The child items in the tree represent folders and images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="00fae-110">Dopo la connessione a un dispositivo, chiamare la proprietà [**Children**](-wia-iwiadispatchitem-children.md) dell'oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo (l'elemento radice dell'albero) per ottenere una raccolta degli elementi figlio (le immagini o i letti di analisi) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00fae-110">After connecting to a device, call the [**Children**](-wia-iwiadispatchitem-children.md) property of the [**Item**](-wia-item.md) object that represents the device (the root item of the tree) to obtain a collection of the child items (the images or scan beds) of the device.</span></span>

<span data-ttu-id="00fae-111">Enumerare la raccolta in modo ricorsivo, se necessario, per esplorare l'albero degli elementi.</span><span class="sxs-lookup"><span data-stu-id="00fae-111">Enumerate this collection (recursively, if necessary) to navigate item tree.</span></span>

 

 
