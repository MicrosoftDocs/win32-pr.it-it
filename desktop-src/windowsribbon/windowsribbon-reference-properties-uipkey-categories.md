---
title: UI_PKEY_Categories
description: Identifica la proprietà \_ UI PKEY \_ Categories.
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4aa812673f289b80b000710dd48a449656368f00d0beb51dcb489e60328e6a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086549"
---
# <a name="ui_pkey_categories"></a>Categorie \_ DI CHIAVI \_ dell'interfaccia utente

Identifica la proprietà \_ UI PKEY \_ Categories.

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Commenti

Le categorie PKEY dell'interfaccia utente vengono usate da un'applicazione per \_ eseguire query nelle categorie usate per \_ raggruppare gli elementi correlati in un controllo raccolta.

Il valore della proprietà è [**un oggetto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) in cui ogni elemento della raccolta rappresenta una categoria.

Ogni elemento in [**questo oggetto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementare [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) per esporre le proprietà di sola lettura associate all'elemento, ad esempio l'etichetta o l'immagine.

Per aggiungere o eliminare elementi in un controllo raccolta in fase di esecuzione, usare i vari metodi di [**IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

Lo screenshot seguente illustra l'uso di due categorie, **Forme di** selezione e Opzioni **di selezione**, in un menu [**SplitButton.**](windowsribbon-element-splitbutton.md)

![Screenshot che mostra due categorie, forme di selezione e opzioni di selezione, in un controllo splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà della raccolta](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 