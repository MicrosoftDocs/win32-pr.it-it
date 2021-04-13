---
title: Metodo IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces. h)
description: Unisce i file modifiche disco virtuali.
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
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341063"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a>Metodo IVMVirtualMachine:: MergeUndoDisks

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Unisce i file modifiche disco virtuali.

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

Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia della creazione dell'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                            |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **null**.<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt> </dl> | Il sistema non è in grado di trovare il percorso specificato dal parametro *convertedDiskImagePath* o uno dei dischi padre non è valido.<br/> |
| <dl> <dt>**E \_**</dt> <dt>0x80070005</dt> AccessDenied </dl>                               | L'utente corrente non dispone di accesso sufficiente al file padre.<br/>                                                                 |
| <dl> <dt>**E \_ GESTISCi**</dt> <dt>0x80070006</dt> </dl>                                     | Uno dei dischi padre è in uso.<br/>                                                                                           |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                            | La configurazione è sconosciuta.<br/>                                                                                                |
| <dl> <dt>**Macchina virtuale \_ E \_ macchina virtuale \_ che esegue**</dt> <dt>0xA0040500</dt> </dl>                            | La macchina virtuale è in esecuzione.<br/>                                                                                              |
| <dl> <dt>**Macchina virtuale \_ E \_ file \_ \_**</dt> di sola lettura <dt>0xA004067A</dt> </dl>                       | L'elemento padre di file modifiche disco virtuali è contrassegnato come di sola lettura.<br/>                                                                     |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                            |



 

## <a name="remarks"></a>Commenti

Non è possibile chiamare **MergeUndoDisks** mentre la macchina virtuale è ancora in esecuzione. Usare [**IVMVirtualMachine:: Save**](ivmvirtualmachine-save.md) per salvare lo stato della macchina virtuale prima di chiamare **MergeUndoDisks** o [**IVMVirtualMachine:: bivio**](ivmvirtualmachine-turnoff.md) per spegnere la macchina virtuale senza salvare lo stato corrente in anticipo.

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

 

