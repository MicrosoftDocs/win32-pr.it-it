---
title: Metodo Save IVMVirtualMachine (VPCCOMInterfaces.h)
description: Salva lo stato della macchina virtuale .
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Metodo Di salvataggio Virtual PC
- Metodo Save Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo Save
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 609125ed9ae8deab897163d6a841e9cb665659c2c5af76baff3a1d96fb235e92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124791"
---
# <a name="ivmvirtualmachinesave-method"></a>Metodo IVMVirtualMachine::Save

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Salva lo stato della macchina virtuale .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*saveTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia dello stato di avanzamento della sequenza di salvataggio dello stato della macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'operazione è stata completata.<br/>                                                 |
| <dl> <dt>**E \_ FAIL**</dt> <dt>0x80004005</dt> </dl>                                     | Impossibile salvare la macchina virtuale perché i dischi di annullamento sono stati contrassegnati per l'eliminazione.<br/>    |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                  | Il parametro è **NULL.**<br/>                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0x80070005</dt> </dl> | Il chiamante deve disporre delle autorizzazioni di accesso di esecuzione per salvare lo stato di questa macchina virtuale.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>                     | La macchina virtuale non è in esecuzione.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Si è verificato un errore imprevisto.<br/>                                             |



 

## <a name="remarks"></a>Commenti

La macchina virtuale viene disattivata quando **l'attività Salva** raggiunge il completamento. La [**proprietà IVMVirtualMachine::State**](ivmvirtualmachine-state.md) conterrà **vmVMState \_ Saving** mentre è in corso il salvataggio, seguita da **vmVMState \_ Saved** al termine del salvataggio e alla spenta della macchina virtuale.

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

 

