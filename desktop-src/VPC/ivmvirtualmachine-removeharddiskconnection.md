---
title: Metodo IVMVirtualMachine RemoveHardDiskConnection (VPCCOMInterfaces. h)
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
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400666"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a>Metodo IVMVirtualMachine:: RemoveHardDiskConnection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Rimuove la connessione al disco rigido specificata dalla macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hardDiskConnection* \[ in\]
</dt> <dd>

Oggetto [**IVMHardDiskConnection**](ivmharddiskconnection.md) che rappresenta la connessione al disco rigido da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                              |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                    | Il parametro è **null**.<br/>                                 |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>            | La configurazione è sconosciuta.<br/>                              |
| <dl> <dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt> </dl> | Lo stato della macchina virtuale è in esecuzione o salvato.<br/>        |
| <dl> <dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt> </dl>         | L'unità specificata non è connessa a questo percorso del bus.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>            | Si è verificato un errore imprevisto.<br/>                          |



 

## <a name="remarks"></a>Commenti

È possibile rimuovere una connessione a un disco rigido esistente solo da una macchina virtuale arrestata. Un elenco di connessioni attualmente collegate alla macchina virtuale viene ottenuto enumerando la proprietà [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

