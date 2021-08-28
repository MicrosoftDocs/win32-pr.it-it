---
title: PLAYLIST.itemMedia
description: L'attributo itemMedia recupera l'oggetto Media corrispondente all'indice specificato nell'elemento PLAYLIST.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- PLAYLIST.itemMedia Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52b3061ef83ec246878d51528e88a12b4f10dcb3085f584a2266dc64a163b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746868"
---
# <a name="playlistitemmedia"></a>PLAYLIST.itemMedia

**L'attributo itemMedia** recupera l'oggetto **Media** corrispondente all'indice specificato nell'elemento **PLAYLIST.**

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un oggetto Multimediale **di** sola lettura.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Indice*
</dt> <dd>

**Numero**(**long**) contenente l'indice di un elemento della playlist.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà itemMedia** restituirà oggetti multimediali espansi nell'elemento **PLAYLIST.** Ad esempio, se è presente una playlist che contiene tre clip multimediali non espanse nell'elemento **PLAYLIST,** **itemMedia**(0) restituirà la playlist come oggetto multimediale. Se la playlist è espansa, **itemMedia**(0) restituirà il primo clip multimediale nella playlist.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





