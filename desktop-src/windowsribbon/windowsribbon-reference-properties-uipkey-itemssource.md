---
title: UI_PKEY_ItemsSource
description: Identifica la proprietà ItemsSource dell'interfaccia utente \_ pkey \_ .
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bdc52a7688648f59be74c22516ee790d109dd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729471"
---
# <a name="ui_pkey_itemssource"></a><span data-ttu-id="cb5d2-103">Interfaccia utente \_ pkey \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="cb5d2-103">UI\_PKEY\_ItemsSource</span></span>

<span data-ttu-id="cb5d2-104">Identifica la proprietà ItemsSource dell'interfaccia utente \_ pkey \_ .</span><span class="sxs-lookup"><span data-stu-id="cb5d2-104">Identifies the UI\_PKEY\_ItemsSource property.</span></span>

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="cb5d2-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb5d2-105">Remarks</span></span>

<span data-ttu-id="cb5d2-106">L'interfaccia utente \_ pkey \_ ItemsSource viene utilizzata da un'applicazione per eseguire una query sulla raccolta di elementi in un controllo raccolta, ad esempio la barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="cb5d2-106">UI\_PKEY\_ItemsSource is used by an application to query the collection of items in a gallery control, such as the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="cb5d2-107">Il valore della proprietà è un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="cb5d2-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="cb5d2-108">Ogni elemento in questo [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementare [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) per esporre le proprietà di sola lettura associate all'elemento, ad esempio l'etichetta o l'immagine.</span><span class="sxs-lookup"><span data-stu-id="cb5d2-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="cb5d2-109">Per aggiungere o eliminare elementi in un controllo raccolta in fase di esecuzione, usare i metodi [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="cb5d2-109">To add or delete items in a gallery control at run time, use the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) methods.</span></span>

<span data-ttu-id="cb5d2-110">Lo screenshot seguente illustra una raccolta di elementi in un menu [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="cb5d2-110">The following screen shot illustrates a collection of items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) menu.</span></span>

![screenshot che mostra le categorie in una raccolta della barra multifunzione.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a><span data-ttu-id="cb5d2-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb5d2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb5d2-113">Proprietà della raccolta</span><span class="sxs-lookup"><span data-stu-id="cb5d2-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 