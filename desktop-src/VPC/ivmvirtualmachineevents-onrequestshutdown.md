---
title: Metodo IVMVirtualMachineEvents OnRequestShutdown (VPCCOMInterfaces. h)
description: Riceve la notifica che è stata effettuata una richiesta di arresto.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- Metodo OnRequestShutdown Virtual PC
- Metodo OnRequestShutdown Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnRequestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477404"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a>Metodo IVMVirtualMachineEvents:: OnRequestShutdown

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve la notifica che è stata effettuata una richiesta di arresto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato ogni volta che la sessione della macchina virtuale sta per essere arrestata. Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell'evento **vmVirtualMachineEvent \_ RequestShutdown** originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).

Questa notifica degli eventi viene inviata solo quando la sessione delle macchine virtuali sta per essere arrestata. Le routine di arresto del sistema operativo, ad esempio [**IVMGuestOS:: Shutdown**](ivmguestos-shutdown.md), non generano direttamente questo evento, a meno che non tenti anche di eseguire un'alimentazione software dell'hardware virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

