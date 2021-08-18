---
title: Metodo StringCollection.getAttributeCountByType
description: Il metodo getAttributeCountByType recupera il numero di attributi associati all'indice dell'elemento StringCollection, al nome dell'attributo e alla lingua specificati.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player , classe StringCollection
- Classe StringCollection Windows Media Player metodo , getAttributeCountByType
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10f88a3b8e4847588ff8f7f924333c6649e59c362b3296b54ef8b83368b7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832428"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>Metodo StringCollection.getAttributeCountByType

Il **metodo getAttributeCountByType** recupera il numero di attributi associati all'indice dell'elemento **StringCollection,** al nome dell'attributo e alla lingua specificati.

## <a name="syntax"></a>Sintassi


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice in base zero dell'elemento **StringCollection** da cui ottenere l'attributo.

</dd> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo.

</dd> <dt>

*lingua* \[ Pollici\]
</dt> <dd>

**Stringa** contenente la lingua. Se il valore è impostato su Null o sulla stringa vuota (""), viene usata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di lingua RFC 1766 valida, ad esempio "en-us".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**).

## <a name="remarks"></a>Commenti

Questo metodo viene usato per determinare il numero di attributi corrispondenti a un nome di attributo specifico per un particolare **elemento StringCollection.** I numeri di indice possono quindi essere passati al quarto parametro del **metodo StringCollection.getItemInfoByType.**

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





