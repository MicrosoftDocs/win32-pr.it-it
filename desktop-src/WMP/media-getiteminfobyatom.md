---
title: Metodo Media.getItemInfoByAtom
description: Il metodo getItemInfoByAtom recupera il valore dell'attributo con il numero di indice specificato.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- Metodo getItemInfoByAtom Windows Media Player
- Metodo getItemInfoByAtom Windows Media Player , classe Media
- Classe media Windows Media Player metodo , getItemInfoByAtom
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26db8e87a52c0d8c8236b5e4b8b5e7325fb3bb0a995dcbd81da668ea760df660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135134"
---
# <a name="mediagetiteminfobyatom-method"></a>Metodo Media.getItemInfoByAtom

Il **metodo getItemInfoByAtom** recupera il valore dell'attributo con il numero di indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice in corrispondenza del quale risiede un determinato attributo all'interno del set di attributi disponibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore String** che rappresenta il valore dell'attributo specificato. Per gli attributi il cui valore sottostante **è booleano,** restituisce la stringa "true" o "false".

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato per recuperare i metadati per un elemento multimediale digitale specifico usando un numero di indice dell'attributo. La **proprietà attributeCount** può essere usata per determinare il numero di attributi disponibili per l'elemento multimediale.

Il **metodo getMediaAtom** dell'oggetto **MediaCollection** può essere usato anche per recuperare l'indice di un attributo specifico. Questa tecnica è in genere più efficiente dei **metodi getItemInfo** o **getItemInfoByType** quando si lavora con playlist di grandi dimensioni.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

Per informazioni sugli attributi supportati da Windows Media Player, vedere Windows Media Player [riferimento agli attributi.](attribute-reference.md)

**Windows Media Player 10 Mobile:** Gli attributi per un elemento multimediale sono disponibili solo durante la riproduzione, a meno che non vengano recuperati dall'elemento tramite la raccolta multimediale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MediaCollection.getMediaAtom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**Lettura dei valori degli attributi**](reading-attribute-values.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





