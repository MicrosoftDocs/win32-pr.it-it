---
title: Metodo IVMGuestOS InstallIntegrationComponents (VPCCOMInterfaces. h)
description: Individua e installa i componenti di integrazione più recenti nel sistema operativo guest.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- Metodo InstallIntegrationComponents Virtual PC
- Metodo InstallIntegrationComponents Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo InstallIntegrationComponents
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879ded1464ebd310e1d1da4e3a952dc086600350
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400268"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a>Metodo IVMGuestOS:: InstallIntegrationComponents

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Individua e installa i componenti di integrazione più recenti nel sistema operativo guest.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                               |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>                       | Per questa operazione è necessario che la macchina virtuale sia in esecuzione.<br/>                     |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                            | Impossibile trovare la macchina virtuale.<br/>                                     |
| <dl> <dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt> </dl>                         | La macchina virtuale non dispone di un'unità DVD vuota.<br/>                       |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ smontaggio supporto \_ 0xA0040508 non riuscito**</dt> <dt></dt> </dl>                   | Il tentativo di smontare il supporto dall'unità DVD della macchina virtuale non è riuscito.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                           |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt> </dl> | Il sistema non è in grado di trovare il file ISO per i componenti di integrazione.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

