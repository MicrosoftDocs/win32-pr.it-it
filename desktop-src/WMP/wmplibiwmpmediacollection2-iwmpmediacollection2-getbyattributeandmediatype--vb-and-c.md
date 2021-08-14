---
title: Metodo IWMPMediaCollection2 getByAttributeAndMediaType
description: Il metodo getByAttributeAndMediaType restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali con un attributo e un tipo di supporto specificati.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- Metodo getByAttributeAndMediaType Windows Media Player
- Metodo getByAttributeAndMediaType Windows Media Player, interfaccia IWMPMediaCollection2
- Interfaccia IWMPMediaCollection2 Windows Media Player metodo , getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e08d38954dd24246b4d35b7842f890caba6eea94868901a528396e9a22b38c1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246433"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a>Metodo IWMPMediaCollection2::getByAttributeAndMediaType

Il `getByAttributeAndMediaType` metodo restituisce **un'interfaccia IWMPPlaylist** che fornisce l'accesso agli elementi multimediali con un attributo e un tipo di supporto specificati.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAttribute* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta l'attributo specificato.

</dd> <dt>

*bstrValue* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il valore specificato per l'attributo specificato in *bstrAttribute*.

</dd> <dt>

*bstrMediaType* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il tipo di supporto specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPPlaylist** per la playlist recuperata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMediaCollection2 (VB e C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





