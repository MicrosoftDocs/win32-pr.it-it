---
title: Metodo IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces. h)
description: Connette un dispositivo USB a una macchina virtuale.
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
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048494"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>Metodo IVMVirtualMachine:: AttachUSBDevice

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Connette un dispositivo USB a una macchina virtuale (VM).

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inUSBDevice* \[ in\]
</dt> <dd>

Puntatore [**IVMUSBDevice**](ivmusbdevice.md) che rappresenta il dispositivo USB connesso all'host.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                             | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                   | L'operazione è stata completata.<br/>                                           |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                     | Il parametro è **null**.<br/>                                              |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>                        | La macchina virtuale non è in esecuzione.<br/>                                                  |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                             | La configurazione è sconosciuta.<br/>                                           |
| <dl> <dt>**Macchina virtuale \_ \_Aggiunte di E \_ non \_ disponibili**</dt> <dt>0xA0040504</dt> </dl>                   | I componenti di integrazione non sono disponibili nel sistema operativo guest.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt> </dl>          | La funzionalità USB non è disponibile.<br/>                                       |
| <dl> <dt>**Macchina virtuale \_ \_ \_ \_ \_ Errore driver connettore USB E**</dt> <dt>0xA00400925</dt> </dl>          | Si è verificato un errore del driver del connettore USB.<br/>                                 |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ collegamento USB \_ non riuscito \_ più \_ dispositivi**</dt> <dt>0xA00400931</dt> </dl>     | Non è possibile aggiungere più dispositivi alla macchina virtuale.<br/>                                   |
| <dl> <dt>**Macchina virtuale \_ \_Errore del \_ GP di collegamento USB E \_ non riuscito \_ \_**</dt> <dt>0xA00400932</dt> </dl>         | Un'impostazione di criteri di gruppo impedisce il reindirizzamento USB.<br/>               |
| <dl> <dt>**Macchina virtuale \_ Il \_ \_ collegamento USB \_ non è stato \_ già \_ assegnato**</dt> <dt>0xA00400933</dt> </dl> | Un dispositivo USB è già stato collegato da un altro client.<br/>            |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ collegamento USB \_ non riuscito**</dt> <dt>0xA00400926</dt> </dl>                    | Operazione di connessione non riuscita.<br/>                                            |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                             | Si è verificato un errore imprevisto.<br/>                                       |



 

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

 

