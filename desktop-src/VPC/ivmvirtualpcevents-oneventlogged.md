---
title: Metodo IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces.h)
description: Riceve una notifica che Windows un evento viene logato da Virtual PC.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Metodo OnEventLogged Virtual PC
- Metodo OnEventLogged Virtual PC , interfaccia IVMVirtualPCEvents
- Interfaccia IVMVirtualPCEvents Virtual PC, metodo OnEventLogged
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4994f37cd0e6f83162171fbbdacbf2247a8d472cd49b5750aa2d1b735e4b554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998521"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>Metodo IVMVirtualPCEvents::OnEventLogged

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riceve una notifica che Windows un evento viene logato da Virtual PC.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*logMessageID* \[ Pollici\]
</dt> <dd>

Identificatore del messaggio del registro eventi registrato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando Windows virtual PC registra un messaggio nel Windows eventi. Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica **dell'evento vmVirtualPCEvent \_ EventLogged** originato da [**IVMVirtualPC.**](ivmvirtualpc.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents è definito come efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

