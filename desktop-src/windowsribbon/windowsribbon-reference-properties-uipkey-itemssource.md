---
title: UI_PKEY_ItemsSource
description: Identifica la proprietà \_ ItemsSource PKEY \_ dell'interfaccia utente.
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017a3fc8f05c24c8d1996202b1db08a459f1a3747e3f787b521a70e6e3a25df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201572"
---
# <a name="ui_pkey_itemssource"></a>UI \_ PKEY \_ ItemsSource

Identifica la proprietà \_ ItemsSource PKEY \_ dell'interfaccia utente.

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

Ui PKEY ItemsSource viene usato da un'applicazione per eseguire query sulla raccolta di elementi in un controllo raccolta, ad esempio la barra \_ \_ di accesso rapido.

Il valore della proprietà è un [**oggetto IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

Ogni elemento in [**questo oggetto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementare [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) per esporre le proprietà di sola lettura associate all'elemento, ad esempio l'etichetta o l'immagine.

Per aggiungere o eliminare elementi in un controllo raccolta in fase di esecuzione, usare i [**metodi IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

Lo screenshot seguente illustra una raccolta di elementi in un menu [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

![Screenshot che mostra le categorie in una raccolta della barra multifunzione.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà della raccolta](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 