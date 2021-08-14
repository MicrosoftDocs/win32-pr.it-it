---
title: Metodo IVMVirtualMachine DetachUSBDevice (VPCCOMInterfaces.h)
description: Rilascia un dispositivo USB da una macchina virtuale.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- Metodo DetachUSBDevice Virtual PC
- Metodo DetachUSBDevice Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo DetachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5b45821f56a9533ed851f6c73342fbd15801223832cf9bad9a380b3f97f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344675"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a>Metodo IVMVirtualMachine::D etachUSBDevice

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Rilascia un dispositivo USB da una macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inUSBDevice* \[ Pollici\]
</dt> <dd>

Puntatore [**IVMUSBDevice**](ivmusbdevice.md) che rappresenta il dispositivo USB da scollegare dalla macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                          | Descrizione                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | L'operazione è stata completata.<br/>       |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                  | Il parametro è **NULL.**<br/>          |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt> </dl>     | La macchina virtuale non è in esecuzione.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ SCOLLEGAMENTO USB \_ NON**</dt> <dt>riuscito 0xA00400927</dt> </dl> | Operazione di scollegamento non riuscita.<br/>        |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>          | Si è verificato un errore imprevisto.<br/>   |



 

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

 

