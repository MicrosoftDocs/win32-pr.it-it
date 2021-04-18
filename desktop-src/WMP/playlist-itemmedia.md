---
title: PLAYLIST. itemMedia
description: L'attributo itemMedia recupera l'oggetto multimediale corrispondente all'indice specificato nell'elemento PLAYLIST.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- PLAYLIST. itemMedia Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327622"
---
# <a name="playlistitemmedia"></a>PLAYLIST. itemMedia

L'attributo **itemMedia** recupera l'oggetto **multimediale** corrispondente all'indice specificato nell'elemento **playlist** .

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un oggetto **multimediale** di sola lettura.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero**(**Long**) che contiene l'indice di un elemento della playlist.

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **itemMedia** restituirà oggetti multimediali espansi nell'elemento **playlist** . Se, ad esempio, è presente una playlist che contiene tre clip multimediali non espanse nell'elemento **playlist** , **itemMedia**(0) restituirà la playlist come oggetto multimediale. Se la playlist è espansa, **itemMedia**(0) restituirà il primo clip multimediale nella playlist.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> </dl>

 

 





