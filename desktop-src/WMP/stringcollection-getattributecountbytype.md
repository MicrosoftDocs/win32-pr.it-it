---
title: StringCollection. getAttributeCountByType, metodo
description: Il metodo getAttributeCountByType Recupera il numero di attributi associati all'indice dell'elemento StringCollection, al nome dell'attributo e alla lingua specificati.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player, classe StringCollection
- StringCollection (classe) Windows Media Player, metodo getAttributeCountByType
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
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328711"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>StringCollection. getAttributeCountByType, metodo

Il metodo **getAttributeCountByType** Recupera il numero di attributi associati all'indice dell'elemento **StringCollection** , al nome dell'attributo e alla lingua specificati.

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

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice in base zero dell'elemento **StringCollection** da cui ottenere l'attributo.

</dd> <dt>

*nome* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo.

</dd> <dt>

*lingua* \[ di in\]
</dt> <dd>

**Stringa** contenente il linguaggio. Se il valore è impostato su null o su una stringa vuota (""), viene utilizzata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**).

## <a name="remarks"></a>Commenti

Questo metodo viene utilizzato per determinare il numero di attributi corrispondenti a un nome di attributo specifico per un particolare elemento **StringCollection** . I numeri di indice possono quindi essere passati al quarto parametro del metodo **StringCollection. getItemInfoByType** .

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**StringCollection (oggetto)**](stringcollection-object.md)
</dt> </dl>

 

 





