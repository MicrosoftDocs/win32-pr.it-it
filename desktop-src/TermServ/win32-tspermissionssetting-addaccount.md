---
title: Metodo AddAccount della classe Win32_TSPermissionsSetting (Faxcomex.h)
description: Il metodo AddAccount prepara l'aggiunta di un account al terminale con il set di autorizzazioni specificato. È possibile aggiungere utenti, gruppi o computer.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Metodo AddAccount Servizi Desktop remoto
- Metodo AddAccount Servizi Desktop remoto , Win32_TSPermissionsSetting classe
- Win32_TSPermissionsSetting classe Servizi Desktop remoto , metodo AddAccount
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3bd1862dfde955d782527ca60fc0fb43ca31431ccb307574e875fe84a640655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348556"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Metodo AddAccount della classe \_ TSPermissionsSetting Win32

Il **metodo AddAccount** prepara l'aggiunta di un account al terminale con il set di autorizzazioni specificato. È possibile aggiungere utenti, gruppi o computer.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AccountName* \[ Pollici\]
</dt> <dd>

Nome dell'account da aggiungere al terminale.

</dd> <dt>

*PermissionPreSet* \[ Pollici\]
</dt> <dd>

Set di autorizzazioni da associare all'account specificato. Questo parametro può essere uno o tutti i valori seguenti. Per altre informazioni, vedere [Servizi Desktop remoto autorizzazioni](terminal-services-permissions.md).

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_ ACCESSO \_ GUEST** (0)


</dt> <dd>

L'account dispone dell'autorizzazione di accesso.

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_ ACCESSO \_ UTENTE** (1)


</dt> <dd>

L'account dispone delle autorizzazioni seguenti: Accesso, Informazioni query, Invia messaggio e Connessione.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_ ALL \_ ACCESS** (2)


</dt> <dd>

L'account dispone di tutte Servizi Desktop remoto autorizzazioni.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto di questi valori,](terminal-services-wmi-provider-error-codes.md) fare riferimento Servizi Desktop remoto di errore del provider WMI.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Faxcomex.h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

