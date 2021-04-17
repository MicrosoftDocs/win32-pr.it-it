---
description: Un'applicazione consente di spostarsi in un albero degli elementi del dispositivo Windows Image Acquisition (WIA) per individuare e selezionare le immagini nel dispositivo. Utilizzando questa tecnica, un'applicazione seleziona e acquisisce un'immagine senza presentare una finestra di dialogo all'utente.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Esplorazione di un albero di elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526431"
---
# <a name="navigating-an-item-tree"></a><span data-ttu-id="3c463-104">Esplorazione di un albero di elementi</span><span class="sxs-lookup"><span data-stu-id="3c463-104">Navigating an Item Tree</span></span>

<span data-ttu-id="3c463-105">Un'applicazione consente di spostarsi in un albero degli elementi del dispositivo Windows Image Acquisition (WIA) per individuare e selezionare le immagini nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c463-105">An application navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="3c463-106">Utilizzando questa tecnica, un'applicazione seleziona e acquisisce un'immagine senza presentare una finestra di dialogo all'utente.</span><span class="sxs-lookup"><span data-stu-id="3c463-106">Using this technique, an application selects and acquires an image without presenting a dialog box to the user.</span></span>

<span data-ttu-id="3c463-107">Un dispositivo WIA viene rappresentato come elemento radice in una struttura ad albero di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3c463-107">A WIA device is represented as the root item in a tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="3c463-108">Gli elementi figlio nell'albero rappresentano le immagini per una fotocamera o i letti digitalizzazione per uno scanner.</span><span class="sxs-lookup"><span data-stu-id="3c463-108">The child items in the tree represent images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="3c463-109">Dopo aver selezionato un dispositivo WIA, un'applicazione chiama il metodo [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) dell'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) del dispositivo per enumerare gli elementi figlio (le immagini o i letti di analisi) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c463-109">After a WIA device is selected, an application calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method of the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface of the device to enumerate the child items (the images or scan beds) of the device.</span></span> <span data-ttu-id="3c463-110">Per istruzioni, vedere [selezione di un dispositivo](-wia-selecting-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="3c463-110">For instructions, see [Selecting a Device](-wia-selecting-a-device.md).</span></span>

<span data-ttu-id="3c463-111">Il metodo [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) crea un oggetto di enumerazione per gli elementi figlio del dispositivo e restituisce un puntatore all'interfaccia [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3c463-111">The [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method creates an enumeration object for the child items of the device, and returns a pointer to that object's [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) interface.</span></span> <span data-ttu-id="3c463-112">L'applicazione può quindi usare i metodi dell'interfaccia **IEnumWiaItem** per ottenere i puntatori agli elementi nell'albero degli elementi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c463-112">The application can then use the methods of the **IEnumWiaItem** interface to obtain pointers to the items in the device's item tree.</span></span>

 

 



