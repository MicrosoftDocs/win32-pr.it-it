---
title: Metodo IVMVirtualMachine DetachUSBDevice (VPCCOMInterfaces. h)
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
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302093"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a>IVMVirtualMachine::D Metodo etachUSBDevice

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Rilascia un dispositivo USB da una macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inUSBDevice* \[ in\]
</dt> <dd>

Puntatore [**IVMUSBDevice**](ivmusbdevice.md) che rappresenta il dispositivo USB da scollegare dalla macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                          | Descrizione                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | L'operazione è stata completata.<br/>       |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                  | Il parametro è **null**.<br/>          |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>     | La macchina virtuale non è in esecuzione.<br/> |
| <dl> <dt>**Macchina virtuale \_ \_Scollegamento USB E 0xA00400927 \_ \_ non riuscito**</dt> <dt></dt> </dl> | Operazione di scollegamento non riuscita.<br/>        |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>          | Si è verificato un errore imprevisto.<br/>   |



 

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

 

