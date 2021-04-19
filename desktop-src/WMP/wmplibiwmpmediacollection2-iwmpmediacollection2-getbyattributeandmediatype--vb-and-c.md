---
title: Metodo IWMPMediaCollection2 getByAttributeAndMediaType
description: Il metodo getByAttributeAndMediaType restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali con un attributo e un tipo di supporto specificati.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- Metodo getByAttributeAndMediaType Windows Media Player
- Metodo getByAttributeAndMediaType Windows Media Player, interfaccia IWMPMediaCollection2
- Interfaccia IWMPMediaCollection2 Windows Media Player, metodo getByAttributeAndMediaType
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
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333394"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a>Metodo IWMPMediaCollection2:: getByAttributeAndMediaType

Il `getByAttributeAndMediaType` metodo restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali con un attributo e un tipo di supporto specificati.

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

*bstrAttribute* \[ in\]
</dt> <dd>

**System. String** che rappresenta l'attributo specificato.

</dd> <dt>

*bstrValue* \[ in\]
</dt> <dd>

**System. String** che corrisponde al valore specificato per l'attributo specificato in *bstrAttribute*.

</dd> <dt>

*bstrMediaType* \[ in\]
</dt> <dd>

**System. String** che rappresenta il tipo di supporto specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPPlaylist** per la playlist recuperata.

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

 

 





