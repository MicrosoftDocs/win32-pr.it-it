---
title: Metodo Erase IWMPCdromBurn
description: Il metodo Erase Cancella il CD corrente.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- Metodo Erase Media Player Windows
- Metodo Erase Media Player Windows, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo Erase
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e168142a6ee77081871bb7dbefa79de8031d71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329661"
---
# <a name="iwmpcdromburnerase-method"></a>Metodo IWMPCdromBurn:: erase

Il metodo **Erase** Cancella il CD corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo non funzionerà se il disco nell'unità non è riscrivibile. Utilizzare [IWMPCdromBurn. saavailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) per determinare se è possibile cancellare un CD.

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

 

 





