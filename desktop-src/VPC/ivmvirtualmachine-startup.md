---
title: Metodo di avvio IVMVirtualMachine (VPCCOMInterfaces.h)
description: Avvia la macchina virtuale dallo stato non inizializzato o salvato.
ms.assetid: 82f9b6f1-99b1-4402-93f5-b4aa3520a505
keywords:
- Metodo di avvio Virtual PC
- Metodo di avvio Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, Metodo di avvio
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d7e63ea8944cf65a66e6f09dd8c0efa531d9e4cadf5390c116678a6f9804e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652911"
---
# <a name="ivmvirtualmachinestartup-method"></a>Metodo IVMVirtualMachine::Startup

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Avvia la macchina virtuale dallo stato non inizializzato o salvato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Startup(
  [out, retval] IVMTask **startupTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*startupTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia dello stato di avanzamento del completamento della sequenza di avvio della macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'operazione è stata completata.<br/>                                                  |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                  | Il parametro è **NULL.**<br/>                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0x80070005</dt> </dl> | Il chiamante deve disporre delle autorizzazioni di accesso di esecuzione per avviare questa macchina virtuale.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ TIMEOUT \_ 0xA0040202**</dt> <dt></dt> </dl>                           | L'operazione non è stata completata in modo corretto.<br/>                             |
| <dl> <dt>**Macchina virtuale \_ E \_ OUT \_ OF \_ RESOURCE**</dt> <dt>0xA0040203</dt> </dl>                    | Le risorse host non sono sufficienti.<br/>                                           |
| <dl> <dt>**Macchina virtuale \_ E \_ TROPPE MACCHINE VIRTUALI \_ \_ 0xA0040204**</dt> <dt></dt> </dl>                       | Sono presenti troppe macchine virtuali attive.<br/>                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ VM \_ RUNNING**</dt> <dt>0xA0040500</dt> </dl>                          | La macchina virtuale è già in esecuzione.<br/>                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ PARENT \_ MODIFIED**</dt> <dt>0xA00400687</dt> </dl>                    | Impossibile avviare la macchina virtuale poiché il disco rigido virtuale padre è stato modificato.<br/>     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Si è verificato un errore imprevisto.<br/>                                              |



 

## <a name="remarks"></a>Commenti

Se la macchina virtuale viene salvata, verrà ripristinata dallo stato salvato.

I valori seguenti possono essere restituiti tramite la [**proprietà Error**](ivmtask-error.md) dell'oggetto [**IVMTask**](ivmtask.md) restituito.



| [**Codice**](ivmtask-error.md) di errore/Valore                                                                                                                                                                                                                                      | Descrizione                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)<br/>                                                 | L'hardware non supporta la virtualizzazione.<br/>              |
| <span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)<br/> | La virtualizzazione hardware è disabilitata.<br/>                       |
| <span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)<br/>                             | Sono installati sia Virtual PC 2007 che Windows Virtual PC.<br/> |
| <span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)<br/>             | È installato un altro software di virtualizzazione.<br/>                |
| <span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)<br/>                                                                 | Le risorse host non sono sufficienti.<br/>                       |



 

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

 

