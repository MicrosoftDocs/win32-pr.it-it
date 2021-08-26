---
title: Metodo IVMGuestOS InstallIntegrationComponents (VPCCOMInterfaces.h)
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
ms.openlocfilehash: c61ade15736cec16976566f464573b30df7fd918f0f2be84f2f4ebd56e5db514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007191"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a>Metodo IVMGuestOS::InstallIntegrationComponents

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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
| <dl> <dt>**Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>                       | La macchina virtuale deve essere in esecuzione per questa operazione.<br/>                     |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                            | Impossibile trovare la macchina virtuale.<br/>                                     |
| <dl> <dt>**Macchina virtuale \_ E \_ UNITÀ \_ NON**</dt> VALIDA <dt>0xA0040502</dt> </dl>                         | La macchina virtuale non dispone di un'unità DVD vuota.<br/>                       |
| <dl> <dt>**Macchina virtuale \_ E \_ MEDIA \_ UNMOUNT FAIL \_ 0xA0040508**</dt> <dt></dt> </dl>                   | Il tentativo di smontare il supporto dall'unità DVD della macchina virtuale non è riuscito.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                           |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(FILE \_ DI ERRORE NON \_ \_ TROVATO) 0X80070002**</dt> <dt></dt> </dl> | Il sistema non riesce a trovare il file ISO per i componenti di integrazione.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS è definito come \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

