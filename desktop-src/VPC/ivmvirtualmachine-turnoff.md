---
title: Metodo IVMVirtualMachine TurnOff (VPCCOMInterfaces.h)
description: Spegnimento della macchina virtuale.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- Metodo TurnOff Virtual PC
- Metodo TurnOff Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo TurnOff
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5351aacc3e21cd620aa31798314fd7f6728cf98653cb83cbaa2f19439d530c44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864161"
---
# <a name="ivmvirtualmachineturnoff-method"></a>Metodo IVMVirtualMachine::TurnOff

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Spegnimento della macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*turnOffTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia dello stato di avanzamento del completamento della sequenza di turnoff della macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'operazione è stata completata.<br/>                                                     |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                  | Il parametro è **NULL.**<br/>                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0x80070005</dt> </dl> | Il chiamante deve disporre delle autorizzazioni di accesso di esecuzione per disattivare la macchina virtuale.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt> </dl>                     | La macchina virtuale non è in esecuzione.<br/>                                               |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                          | La configurazione è sconosciuta.<br/>                                                     |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                          | Si è verificato un errore imprevisto.<br/>                                                 |



 

## <a name="remarks"></a>Commenti

Questo metodo consente di spegnere la macchina virtuale nello stesso modo in cui si spegne l'alimentazione di una macchina fisica.

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

 

