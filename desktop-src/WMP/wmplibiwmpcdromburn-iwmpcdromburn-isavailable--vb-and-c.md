---
title: Metodo IWMPCdromBurn non disponibile
description: Il metodo disavailable fornisce informazioni sull'unità CD e sui supporti.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- Metodo di Windows Media Player disponibile
- Metodo di Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo disavailable
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329658"
---
# <a name="iwmpcdromburnisavailable-method"></a>Metodo IWMPCdromBurn:: unavailable

Il metodo **disavailable** fornisce informazioni sull'unità CD e sui supporti.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrItem* \[ in\]
</dt> <dd>

**System. String** che contiene uno dei valori seguenti.



| Valore | Descrizione                 |
|-------|-----------------------------|
| Bruciare  | L'unità è un masterizzatore CD.   |
| Disco  | Nell'unità è presente un CD. |
| Cancellazione | È possibile cancellare il CD.       |
| Scrittura | È possibile scrivere in un CD.   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Boolean** che indica il risultato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





