---
title: Metodo IWMPLibraryServices getCountByType
description: Il metodo getCountByType restituisce il conteggio delle librerie disponibili di un tipo specificato.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- Metodo getCountByType Windows Media Player
- Metodo getCountByType Windows Media Player, interfaccia IWMPLibraryServices
- Interfaccia IWMPLibraryServices Windows Media Player, metodo getCountByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332413"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a>Metodo IWMPLibraryServices:: getCountByType

Il metodo **getCountByType** restituisce il conteggio delle librerie disponibili di un tipo specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*wmplt* \[ in\]
</dt> <dd>

Valore dell'enumerazione **wmplib. WMPLibraryType** che specifica il tipo di libreria da contare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Int32** che rappresenta il conteggio delle librerie.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





