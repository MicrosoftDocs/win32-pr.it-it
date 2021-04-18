---
title: Metodo IWMPStringCollection2 getAttributeCountByType
description: Il metodo getAttributeCountByType restituisce il numero di attributi associati all'indice della raccolta di stringhe, al nome dell'attributo e alla lingua specificati.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player, interfaccia IWMPStringCollection2
- Interfaccia IWMPStringCollection2 Windows Media Player, metodo getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331730"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a>Metodo IWMPStringCollection2:: getAttributeCountByType

Il metodo **getAttributeCountByType** restituisce il numero di attributi associati all'indice della raccolta di stringhe, al nome dell'attributo e alla lingua specificati.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lCollectionIndex* \[ in\]
</dt> <dd>

**System. Int32** che specifica l'indice in base zero dell'elemento della raccolta di stringhe da cui ottenere l'attributo.

</dd> <dt>

*bstrType* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'attributo.

</dd> <dt>

*bstrLanguage* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome della lingua. Se il valore è impostato su null o su una stringa di lunghezza zero (""), viene utilizzata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Int32** che rappresenta il conteggio.

## <a name="remarks"></a>Commenti

Questo metodo viene utilizzato per individuare il numero di attributi corrispondente a un nome di attributo specifico per un determinato elemento **StringCollection** . I numeri di indice possono quindi essere passati al quarto parametro del metodo **getItemInfoByType** .

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPStringCollection2 (VB e C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfoByType (VB e C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





