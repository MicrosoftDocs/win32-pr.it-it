---
title: Metodo IVMVirtualMachine RemoveHardDiskConnection (VPCCOMInterfaces.h)
description: Rimuove la connessione al disco rigido specificata dalla macchina virtuale.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- Metodo RemoveHardDiskConnection Virtual PC
- Metodo RemoveHardDiskConnection Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo RemoveHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdcf09118e8fd9911937a7ab8323266ed33c7e974e0b98579fb30a75dae7f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998661"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a>Metodo IVMVirtualMachine::RemoveHardDiskConnection

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Rimuove la connessione al disco rigido specificata dalla macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hardDiskConnection* \[ Pollici\]
</dt> <dd>

Oggetto [**IVMHardDiskConnection**](ivmharddiskconnection.md) che rappresenta la connessione al disco rigido da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                              |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                    | Il parametro è **NULL.**<br/>                                 |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>            | La configurazione è sconosciuta.<br/>                              |
| <dl> <dt>**Macchina virtuale \_ E \_ VM RUNNING OR \_ \_ \_ SAVED**</dt> <dt>0xA004020B</dt> </dl> | La macchina virtuale è in esecuzione o salvata.<br/>        |
| <dl> <dt>**Macchina virtuale \_ E \_ UNITÀ \_ NON VALIDA**</dt> <dt>0xA0040502</dt> </dl>         | L'unità specificata non è connessa a questa posizione del bus.<br/> |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>            | Si è verificato un errore imprevisto.<br/>                          |



 

## <a name="remarks"></a>Commenti

È possibile rimuovere una connessione al disco rigido esistente solo da una macchina virtuale arrestata. Un elenco di connessioni attualmente collegate alla macchina virtuale viene ottenuto enumerando la [**proprietà HardDiskConnections.**](ivmvirtualmachine-harddiskconnections.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

