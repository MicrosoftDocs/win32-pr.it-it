---
title: Proprietà IVMGuestOS MultipleUserSessionsAllowed
description: Determina se nel sistema operativo guest sono consentite più sessioni utente simultanee.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- MultipleUserSessionsAllowed - proprietà Virtual PC
- MultipleUserSessionsAllowed - proprietà Virtual PC , interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà MultipleUserSessionsAllowed
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68075c13cfc65b79d992b849b310bd3c88b09f7901567baf249bff15496ede05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594074"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a>Proprietà IVMGuestOS::MultipleUserSessionsAllowed

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Determina se nel sistema operativo guest sono consentite più sessioni utente simultanee.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a>Valore proprietà

**VARIANT \_ TRUE** se nel sistema operativo guest sono consentite più sessioni utente simultanee, VARIANT FALSE in **\_ caso** contrario.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                                                       |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Servizi Desktop remoto (precedentemente noto come Servizi terminal) non è ancora inizializzato nel sistema operativo guest.<br/> |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                            | Il *parametro sessionStatus* è **NULL.**<br/>                                                                          |
| <dl> <dt>Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>                                                                                 |
| <dl> <dt>Macchina virtuale \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0xA0040505</dt> </dl> | I componenti di integrazione non vengono installati in questa macchina virtuale.<br/>                                                   |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                                                   |



## <a name="remarks"></a>Commenti

Il valore di questa proprietà non è valido a meno che la [**proprietà TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) non **sia VARIANT \_ TRUE.**

Per Windows sistemi operativi client, **MultipleUserSessionsAllowed** è **VARIANT \_ TRUE** se è supportato il cambio rapido utente. Per Windows server, **MultipleUserSessionsAllowed** è **VARIANT \_ TRUE** se Servizi Desktop remoto (in precedenza denominato Servizi terminal) è installato e abilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                      |
| Idl<br/>                      | <dl> <dt>IVMGuestOS.idl</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS è definito come \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

