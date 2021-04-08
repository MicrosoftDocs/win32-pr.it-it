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
# <a name="ui_pkey_itemssource"></a>Interfaccia utente \_ pkey \_ ItemsSource

Identifica la proprietà ItemsSource dell'interfaccia utente \_ pkey \_ .

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Commenti

L'interfaccia utente \_ pkey \_ ItemsSource viene utilizzata da un'applicazione per eseguire una query sulla raccolta di elementi in un controllo raccolta, ad esempio la barra di accesso rapido (QAT).

Il valore della proprietà è un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Ogni elemento in questo [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementare [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) per esporre le proprietà di sola lettura associate all'elemento, ad esempio l'etichetta o l'immagine.

Per aggiungere o eliminare elementi in un controllo raccolta in fase di esecuzione, usare i metodi [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Lo screenshot seguente illustra una raccolta di elementi in un menu [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

![screenshot che mostra le categorie in una raccolta della barra multifunzione.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà della raccolta](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 