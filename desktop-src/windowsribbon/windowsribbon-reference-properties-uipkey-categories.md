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
# <a name="ui_pkey_categories"></a>\_Categorie pkey dell'interfaccia utente \_

Identifica la \_ proprietà delle categorie pkey dell'interfaccia utente \_ .

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

\_Le categorie pkey dell'interfaccia utente \_ vengono utilizzate da un'applicazione per eseguire una query sulle categorie utilizzate per raggruppare gli elementi correlati in un controllo raccolta.

Il valore della proprietà è un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) in cui ogni elemento della raccolta rappresenta una categoria.

Ogni elemento in questo [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementare [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) per esporre le proprietà di sola lettura associate all'elemento, ad esempio l'etichetta o l'immagine.

Per aggiungere o eliminare elementi in un controllo raccolta in fase di esecuzione, usare i vari metodi di [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).

Lo screenshot seguente illustra l'uso di due categorie, forme di **selezione** e **Opzioni di selezione**, in un menu [**SplitButton**](windowsribbon-element-splitbutton.md) .

![screenshot che mostra due categorie, le forme di selezione e le opzioni di selezione in un controllo splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà della raccolta](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[PKEY dell'interfaccia utente \_ \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 