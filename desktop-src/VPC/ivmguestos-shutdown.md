---
title: Metodo Shutdown IVMGuestOS (VPCCOMInterfaces. h)
description: Arresta il sistema operativo guest nella macchina virtuale.
ms.assetid: a1453ad1-c4c2-47bb-a612-d203a6ee8c18
keywords:
- Metodo Shutdown Virtual PC
- Metodo Shutdown Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo Shutdown
topic_type:
- apiref
api_name:
- IVMGuestOS.Shutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63025270752af044a572cf9b6299e54b31b89ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742063"
---
# <a name="ivmguestosshutdown-method"></a>Metodo IVMGuestOS:: Shutdown

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Arresta il sistema operativo guest nella macchina virtuale (VM).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Shutdown(
  [in]          VARIANT_BOOL isForced,
  [out, retval] IVMTask      **outShutdownTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*applicazione forzata* \[ in\]
</dt> <dd>

**Variante \_ TRUE** se l'arresto deve essere forzato, **Variant \_ false** in caso contrario.

</dd> <dt>

*outShutdownTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del completamento del processo di arresto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | L'operazione è stata completata.<br/>                                   |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                  | Il parametro *outShutdownTask* è **null**.<br/>                    |
| <dl> <dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt> </dl>                           | L'operazione non è stata completata in modo tempestivo.<br/>              |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                          | Non è stato possibile trovare la macchina virtuale.<br/>                                      |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>                     | Per questa operazione è necessario che la macchina virtuale sia in esecuzione.<br/>                      |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt> </dl> | Il chiamante deve avere le autorizzazioni di accesso Execute per questa macchina virtuale.<br/>    |
| <dl> <dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt> </dl>       | La funzionalità componenti di integrazione non è installata in questa macchina virtuale.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                          | Si è verificato un errore imprevisto.<br/>                               |



 

## <a name="remarks"></a>Commenti

Quando viene richiamato questo metodo, è necessario che la macchina virtuale sia in esecuzione e che sia installata la funzionalità componenti di integrazione. Questo metodo è supportato solo per i sistemi operativi guest basati su Windows.

I valori seguenti possono essere restituiti tramite la proprietà [**Error**](ivmtask-error.md) dell'oggetto [**IVMTask**](ivmtask.md) restituito.



| Codice [**errore**](ivmtask-error.md) /valore                                                                                                                                                                                                                                                                          | Descrizione                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005<br/>                             | Il chiamante deve avere le autorizzazioni di accesso Execute per questa macchina virtuale.<br/>             |
| <span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)<br/>                         | Il computer è bloccato e non può essere arrestato senza l'opzione Force.<br/> |
| <span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)<br/>                                             | Il dispositivo non è pronto.<br/>                                                 |
| <span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)<br/> | È in corso l'arresto del sistema.<br/>                                        |



 

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

 

