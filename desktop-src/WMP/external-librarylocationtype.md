---
title: External.libraryLocationType
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. | External.libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- External.libraryLocationType Windows Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e254ce6258cf667884e2815508b413ed1455b1b6924bfebb4edc900da048c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736201"
---
# <a name="externallibrarylocationtype"></a>External.libraryLocationType

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

La **proprietà libraryLocationType** recupera una costante [di posizione](library-location-constants.md) della libreria che indica il tipo della vista corrente in Windows Media Player.

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura** che contiene una delle costanti di percorso della libreria.

## <a name="remarks"></a>Commenti

Questa proprietà funziona in combinazione con [la proprietà External.libraryLocationID.](external-librarylocationid.md) Si supponga, ad esempio, **che libraryLocationType** sia uguale a CPAlbumID e **libraryLocationID** sia uguale a 3. Ciò significa che la visualizzazione corrente Windows Media Player mostra l'album con ID 3. Per altre informazioni su come Windows Media Player caratterizza le visualizzazioni del contenuto dello store online, vedere [Posizione e elemento selezionato.](location-and-selected-item.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**Posizione ed elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 





