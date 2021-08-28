---
title: Metodo Media.getAttributeCountByType
description: Il metodo getAttributeCountByType recupera il numero di attributi associati al nome e alla lingua dell'attributo specificati.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player classe Media
- Classe media Windows Media Player metodo , getAttributeCountByType
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
ms.openlocfilehash: 222f92a57ba9fbcd9971a5536be5f31078e2e09373fb1d168a7074911b027d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123450"
---
# <a name="mediagetattributecountbytype-method"></a>Metodo Media.getAttributeCountByType

Il **metodo getAttributeCountByType** recupera il numero di attributi associati al nome e alla lingua dell'attributo specificati.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di Windows Media Player [sugli attributi](attribute-reference.md).

</dd> <dt>

*language* \[ Pollici\]
</dt> <dd>

**Stringa** che rappresenta la lingua. Se il valore è impostato su Null o "" (stringa vuota), viene usata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di lingua RFC 1766 valida, ad esempio "en-us".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**) contenente il numero di attributi.

## <a name="remarks"></a>Commenti

Questo metodo viene usato per determinare il numero di attributi corrispondenti a un nome di attributo specifico per un **determinato oggetto Media.** I numeri di indice possono quindi essere passati al **metodo getItemInfoByType.** Ciò è utile, ad esempio, quando un elemento multimediale è stato categorizzato in più generi.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MediaObject**](media-object.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





