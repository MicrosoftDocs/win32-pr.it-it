---
title: Metodo IWMPMedia3 getAttributeCountByType
description: Il metodo getAttributeCountByType restituisce il numero di attributi associati al tipo di attributo specificato.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player, interfaccia IWMPMedia3
- Interfaccia IWMPMedia3 Windows Media Player metodo , getAttributeCountByType
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
ms.openlocfilehash: 2c8e3fc681ea5471457bd9a80ac3e26dabc08b2112387dd8c5f785bf5f055dfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000111"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>Metodo IWMPMedia3::getAttributeCountByType

Il **metodo getAttributeCountByType** restituisce il numero di attributi associati al tipo di attributo specificato.

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

*bstrType* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il tipo di attributo.

</dd> <dt>

*bstrLanguage* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta la lingua. Se il valore è impostato su Null o su una stringa di lunghezza zero (""), viene usata la stringa delle impostazioni locali corrente. In caso contrario, il valore deve essere una stringa di lingua RFC 1766 valida, ad esempio "en-us".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto **System.Int32** che rappresenta il numero di attributi associati al tipo.

## <a name="remarks"></a>Commenti

Questo metodo viene usato per individuare il numero di attributi corrispondenti a un nome di attributo specifico per un determinato elemento multimediale. I numeri di indice possono quindi essere passati al **metodo getItemInfoByType.** Ciò è utile, ad esempio, quando un elemento multimediale è stato categorizzato in più generi.

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





