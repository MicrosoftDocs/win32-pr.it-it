---
title: Metodo IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces. h)
description: Riceve la notifica che Windows Virtual PC registra un evento.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Metodo OnEventLogged Virtual PC
- Metodo OnEventLogged Virtual PC, interfaccia IVMVirtualPCEvents
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
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518004"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>Metodo IVMVirtualPCEvents:: OnEventLogged

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve la notifica che Windows Virtual PC registra un evento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*logMessageID* \[ in\]
</dt> <dd>

Identificatore del messaggio del registro eventi registrato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando Windows Virtual PC registra un messaggio nel registro eventi di Windows. Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell'evento **vmVirtualPCEvent \_ EventLogged** originato da [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents è definito come efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

