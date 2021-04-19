---
title: Media. getAttributeCountByType, metodo
description: Il metodo getAttributeCountByType Recupera il numero di attributi associati al nome dell'attributo e alla lingua specificati.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player, classe media
- Media class Media Player Windows, metodo getAttributeCountByType
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332554"
---
# <a name="mediagetattributecountbytype-method"></a>Media. getAttributeCountByType, metodo

Il metodo **getAttributeCountByType** Recupera il numero di attributi associati al nome dell'attributo e alla lingua specificati.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.

</dd> <dt>

*lingua* \[ di in\]
</dt> <dd>

**Stringa** che rappresenta la lingua. Se il valore è impostato su null o su "" (stringa vuota), viene utilizzata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**) che contiene il numero di attributi.

## <a name="remarks"></a>Commenti

Questo metodo viene utilizzato per determinare il numero di attributi corrispondenti a un nome di attributo specifico per un determinato oggetto **multimediale** . I numeri di indice possono quindi essere passati al metodo **getItemInfoByType** . Questa operazione è utile, ad esempio, quando un elemento multimediale è stato categorizzato in più generi.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MediaObject**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





