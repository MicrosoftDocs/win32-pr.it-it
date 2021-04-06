---
title: Metodo Save IVMVirtualMachine (VPCCOMInterfaces. h)
description: Salva lo stato della macchina virtuale (VM).
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Salva il metodo Virtual PC
- Salva metodo Virtual PC, interfaccia IVMVirtualMachine
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
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742882"
---
# <a name="ivmvirtualmachinesave-method"></a>Metodo IVMVirtualMachine:: Save

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Salva lo stato della macchina virtuale (VM).

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
| <dl> <dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt> </dl>                                     | Non è stato possibile salvare la macchina virtuale perché i file modifiche disco sono stati contrassegnati per l'eliminazione.<br/>    |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                  | Il parametro è **null**.<br/>                                                    |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt> </dl> | Il chiamante deve disporre delle autorizzazioni di accesso Execute per salvare lo stato della macchina virtuale.<br/> |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>                     | La macchina virtuale non è in esecuzione.<br/>                                                        |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                          | Si è verificato un errore imprevisto.<br/>                                             |



 

## <a name="remarks"></a>Commenti

La macchina virtuale viene spenta al completamento dell'attività di **salvataggio** . La proprietà [**IVMVirtualMachine:: state**](ivmvirtualmachine-state.md) conterrà **vmVMState \_ Saving** mentre è in corso il salvataggio, seguito da **vmVMState \_ salvato** al termine del salvataggio e la macchina virtuale è disattivata.

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

 

