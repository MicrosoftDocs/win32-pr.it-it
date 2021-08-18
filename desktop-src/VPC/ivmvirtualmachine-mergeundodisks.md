---
title: Metodo IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces.h)
description: Unisce i dischi di annullamento virtuali.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- Metodo MergeUndoDisks Virtual PC
- Metodo MergeUndoDisks Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo MergeUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d30558ddb8acdd75d72955048beb34f0141206b53f3f5873e42627fb155f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998681"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a>Metodo IVMVirtualMachine::MergeUndoDisks

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Unisce i dischi di annullamento virtuali.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*undoMergeTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia della creazione dell'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                            |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **NULL.**<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND) 0X80070003**</dt> <dt></dt> </dl> | Il sistema non riesce a trovare il percorso specificato dal *parametro convertedDiskImagePath* oppure uno dei dischi padre non è valido.<br/> |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> <dt>0x80070005</dt> </dl>                               | L'utente corrente non ha accesso sufficiente al file padre.<br/>                                                                 |
| <dl> <dt>**E \_ GESTIRE**</dt> <dt>0x80070006</dt> </dl>                                     | Uno dei dischi padre è in uso.<br/>                                                                                           |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                            | La configurazione è sconosciuta.<br/>                                                                                                |
| <dl> <dt>**Macchina virtuale \_ E \_ VM \_ RUNNING**</dt> <dt>0xA0040500</dt> </dl>                            | La macchina virtuale è in esecuzione.<br/>                                                                                              |
| <dl> <dt>**Macchina virtuale \_ E \_ FILE READ ONLY \_ \_ 0xA004067A**</dt> <dt></dt> </dl>                       | L'elemento padre dei dischi di annullamento virtuali è contrassegnato come di sola lettura.<br/>                                                                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                            |



 

## <a name="remarks"></a>Commenti

**Non è possibile chiamare MergeUndoDisks** mentre la macchina virtuale è ancora in esecuzione. Usare [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md) per salvare lo stato della macchina virtuale prima di chiamare **MergeUndoDisks** o [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md) per disattivare la macchina virtuale senza salvare lo stato corrente in anticipo.

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

 

