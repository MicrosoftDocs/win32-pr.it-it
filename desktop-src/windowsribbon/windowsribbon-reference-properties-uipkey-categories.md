---
title: UI_PKEY_Categories
description: Identifica la \_ proprietà delle categorie pkey dell'interfaccia utente \_ .
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7666ee9eba6639f1f39b96f012b464854191ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300117"
---
# <a name="ui_pkey_categories"></a><span data-ttu-id="8a873-103">\_Categorie pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="8a873-103">UI\_PKEY\_Categories</span></span>

<span data-ttu-id="8a873-104">Identifica la \_ proprietà delle categorie pkey dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="8a873-104">Identifies the UI\_PKEY\_Categories property.</span></span>

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="8a873-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a873-105">Remarks</span></span>

<span data-ttu-id="8a873-106">\_Le categorie pkey dell'interfaccia utente \_ vengono utilizzate da un'applicazione per eseguire una query sulle categorie utilizzate per raggruppare gli elementi correlati in un controllo raccolta.</span><span class="sxs-lookup"><span data-stu-id="8a873-106">UI\_PKEY\_Categories is used by an application to query the categories that are used to group related items in a gallery control.</span></span>

<span data-ttu-id="8a873-107">Il valore della proprietà è un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) in cui ogni elemento della raccolta rappresenta una categoria.</span><span class="sxs-lookup"><span data-stu-id="8a873-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object where each item in the collection represents a category.</span></span>

<span data-ttu-id="8a873-108">Ogni elemento in questo [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementare [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) per esporre le proprietà di sola lettura associate all'elemento, ad esempio l'etichetta o l'immagine.</span><span class="sxs-lookup"><span data-stu-id="8a873-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="8a873-109">Per aggiungere o eliminare elementi in un controllo raccolta in fase di esecuzione, usare i vari metodi di [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span><span class="sxs-lookup"><span data-stu-id="8a873-109">To add or delete items in a gallery control at run time, use the various methods of [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span></span>

<span data-ttu-id="8a873-110">Lo screenshot seguente illustra l'uso di due categorie, forme di **selezione** e **Opzioni di selezione**, in un menu [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="8a873-110">The following screen shot illustrates the use of two categories, **Selection shapes** and **Selection options**, in a [**SplitButton**](windowsribbon-element-splitbutton.md) menu.</span></span>

![screenshot che mostra due categorie, le forme di selezione e le opzioni di selezione in un controllo splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a><span data-ttu-id="8a873-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a873-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a873-113">Proprietà della raccolta</span><span class="sxs-lookup"><span data-stu-id="8a873-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="8a873-114">PKEY dell'interfaccia utente \_ \_ CategoryID</span><span class="sxs-lookup"><span data-stu-id="8a873-114">UI\_PKEY\_CategoryId</span></span>](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 