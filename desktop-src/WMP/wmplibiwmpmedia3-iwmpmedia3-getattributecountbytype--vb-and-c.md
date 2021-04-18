---
title: Metodo IWMPMedia3 getAttributeCountByType
description: Il metodo getAttributeCountByType restituisce il numero di attributi associati al tipo di attributo specificato.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player, interfaccia IWMPMedia3
- Interfaccia IWMPMedia3 Windows Media Player, metodo getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324369"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>Metodo IWMPMedia3:: getAttributeCountByType

Il metodo **getAttributeCountByType** restituisce il numero di attributi associati al tipo di attributo specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrType* \[ in\]
</dt> <dd>

**System. String** che rappresenta il tipo di attributo.

</dd> <dt>

*bstrLanguage* \[ in\]
</dt> <dd>

**System. String** che rappresenta il linguaggio. Se il valore è impostato su null o su una stringa di lunghezza zero (""), viene utilizzata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Int32** che rappresenta il numero di attributi associati al tipo.

## <a name="remarks"></a>Commenti

Questo metodo viene utilizzato per individuare il numero di attributi corrispondente a un nome di attributo specifico per un determinato elemento multimediale. I numeri di indice possono quindi essere passati al metodo **getItemInfoByType** . Questa operazione è utile, ad esempio, quando un elemento multimediale è stato categorizzato in più generi.

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





