---
title: Proprietà MultipleUserSessionsAllowed di IVMGuestOS
description: Determina se nel sistema operativo guest sono consentite più sessioni utente simultanee.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- Proprietà MultipleUserSessionsAllowed Virtual PC
- Proprietà MultipleUserSessionsAllowed Virtual PC, interfaccia IVMGuestOS
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
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119963"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a>Proprietà IVMGuestOS:: MultipleUserSessionsAllowed

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se nel sistema operativo guest sono consentite più sessioni utente simultanee.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a>Valore proprietà

**Variante \_ TRUE** se nel sistema operativo guest sono consentite più sessioni utente simultanee. in caso contrario, **Variant \_ false** .

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                                                       |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Servizi Desktop remoto (precedentemente noto come servizi Terminal) non è ancora inizializzato nel sistema operativo guest.<br/> |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                            | Il parametro *sessionStatus* è **null**.<br/>                                                                          |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>                                                                                 |
| <dl> <dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt> </dl> | I componenti di integrazione non sono installati in questa macchina virtuale.<br/>                                                   |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                                                   |



## <a name="remarks"></a>Commenti

Il valore di questa proprietà non è valido a meno che la proprietà [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) non sia **Variant \_ true**.

Per i sistemi operativi client Windows, **MultipleUserSessionsAllowed** è una **variante \_ true** se il cambio rapido utente è supportato. Per i sistemi operativi Windows Server, **MultipleUserSessionsAllowed** è una **variante \_ true** se Servizi Desktop remoto (denominato in precedenza Terminal Services) viene installata e abilitata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                      |
| IDL<br/>                      | <dl> <dt>IVMGuestOS. idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

