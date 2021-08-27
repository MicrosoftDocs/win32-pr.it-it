---
title: Metodo IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces.h)
description: Collega un dispositivo USB a una macchina virtuale.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Metodo AttachUSBDevice Virtual PC
- Metodo AttachUSBDevice Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo AttachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c62f3e6862e14a7faa70719d1238500ab5dfe1de10801e7aea390e24a07210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006901"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>Metodo IVMVirtualMachine::AttachUSBDevice

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Collega un dispositivo USB a una macchina virtuale (VM).

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inUSBDevice* \[ Pollici\]
</dt> <dd>

Puntatore [**IVMUSBDevice**](ivmusbdevice.md) che rappresenta il dispositivo USB connesso all'host.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                             | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                   | L'operazione è stata completata.<br/>                                           |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                     | Il parametro è **NULL.**<br/>                                              |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt> </dl>                        | La macchina virtuale non è in esecuzione.<br/>                                                  |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                             | La configurazione è sconosciuta.<br/>                                           |
| <dl> <dt>**Macchina virtuale \_ E \_ ADDITIONS \_ NOT \_ AVAIL**</dt> <dt>0xA0040504</dt> </dl>                   | I componenti di integrazione non sono disponibili nel sistema operativo guest.<br/> |
| <dl> <dt>**Macchina virtuale \_ FUNZIONALITÀ \_ DELLE AGGIUNTE E NON \_ \_ \_ 0XA0040505**</dt> <dt></dt> </dl>          | La funzionalità USB non è disponibile.<br/>                                       |
| <dl> <dt>**Macchina virtuale \_ ERRORE \_ DEL DRIVER DEL \_ \_ \_ CONNETTORE USB**</dt> <dt>0XA00400925</dt> </dl>          | Si è verificato un errore del driver del connettore USB.<br/>                                 |
| <dl> <dt>**Macchina virtuale \_ E \_ USB ATTACH FAILED MORE DEVICES \_ \_ \_ \_ 0XA00400931**</dt> <dt></dt> </dl>     | Non è possibile collegare altri dispositivi alla macchina virtuale.<br/>                                   |
| <dl> <dt>**Macchina virtuale \_ Errore E \_ USB ATTACH FAILED GP \_ \_ \_ \_ 0XA00400932**</dt> <dt></dt> </dl>         | Un'impostazione di Criteri di gruppo impedisce il reindirizzamento USB.<br/>               |
| <dl> <dt>**Macchina virtuale \_ E \_ USB ATTACH FAILED ALREADY \_ \_ \_ \_ ASSIGNED**</dt> <dt>0xA00400933</dt> </dl> | Un dispositivo USB è già stato collegato da un altro client.<br/>            |
| <dl> <dt>**Macchina virtuale \_ E \_ USB ATTACH FAILED \_ \_ 0xA00400926**</dt> <dt></dt> </dl>                    | L'operazione di collegamento non è riuscita.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                             | Si è verificato un errore imprevisto.<br/>                                       |



 

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

 

