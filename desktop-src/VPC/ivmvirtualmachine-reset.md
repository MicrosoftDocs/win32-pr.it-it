---
title: Metodo IVMVirtualMachine Reset (VPCCOMInterfaces.h)
description: Reimposta la macchina virtuale.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Metodo reset Virtual PC
- Metodo reset Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo Reset
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d09204afba2d5c9340350a1fad256e84f8fbf8899c544c7b52d36dfb872c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056779"
---
# <a name="ivmvirtualmachinereset-method"></a>Metodo IVMVirtualMachine::Reset

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Reimposta la macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*resetTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia dello stato di avanzamento del completamento della sequenza di reimpostazione della macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'operazione è stata completata.<br/>                                     |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                  | Il parametro è **NULL.**<br/>                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0x80070005</dt> </dl> | Il chiamante deve avere le autorizzazioni di accesso di esecuzione per reimpostare la macchina virtuale.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt> </dl>                     | La macchina virtuale non è in esecuzione.<br/>                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                          | La configurazione è sconosciuta.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                          | Si è verificato un errore imprevisto.<br/>                                 |



 

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

 

