---
title: Metodo Restart di IVMGuestOS (VPCCOMInterfaces.h)
description: Riavvia il sistema operativo guest.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Metodo di riavvio Virtual PC
- Metodo di riavvio Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo Restart
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b25d5fc2bec8c8a0a10425f63b6abc7c6363e8562b84376af4d053ec710e709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594009"
---
# <a name="ivmguestosrestart-method"></a>Metodo IVMGuestOS::Restart

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Riavvia il sistema operativo guest.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inForced* \[ Pollici\]
</dt> <dd>

**VARIANT \_ TRUE se** è necessario un riavvio forzato e **VARIANT FALSE in \_ caso** contrario.

</dd> <dt>

*outRestartTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia dello stato di avanzamento del completamento della sequenza di riavvio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                    | Descrizione                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                   |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                            | Il *parametro outRestartTask* è **NULL.**<br/>                     |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                               |
| <dl> <dt>**Macchina virtuale \_ E \_ TIMEOUT \_ 0xA0040202**</dt> <dt></dt> </dl>                     | L'operazione non è stata completata in modo corretto.<br/>              |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale (VM) deve essere in esecuzione per questa operazione.<br/>    |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                    | La configurazione è sconosciuta.<br/>                                   |
| <dl> <dt>**Macchina virtuale \_ FUNZIONALITÀ \_ DELLE AGGIUNTE E NON \_ \_ \_ 0XA0040505**</dt> <dt></dt> </dl> | La funzionalità dei componenti di integrazione non è installata in questa macchina virtuale.<br/> |



 

## <a name="remarks"></a>Commenti

I valori seguenti possono essere restituiti tramite la [**proprietà Error**](ivmtask-error.md) dell'oggetto [**IVMTask**](ivmtask.md) restituito.



| [**Codice**](ivmtask-error.md) di errore/Valore                                                                                                                                                                                                                                                                          | Descrizione                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)<br/>                             | Il chiamante deve avere le autorizzazioni di accesso di esecuzione per questa macchina virtuale.<br/>             |
| <span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)<br/>                         | Il computer è bloccato e non può essere arrestato senza l'opzione forza.<br/> |
| <span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)<br/>                                             | Il dispositivo non è pronto.<br/>                                                 |
| <span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)<br/> | È in corso un arresto del sistema.<br/>                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

