---
title: Metodo AddAccount della classe Win32_TSPermissionsSetting (Faxcomex. h)
description: Il metodo AddAccount prepara l'aggiunta di un account al terminale con il set di autorizzazioni specificato. È possibile aggiungere utenti, gruppi o computer.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddAccount
- Metodo AddAccount Servizi Desktop remoto, classe Win32_TSPermissionsSetting
- Classe Win32_TSPermissionsSetting Servizi Desktop remoto, metodo AddAccount
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
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477698"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Metodo AddAccount della \_ classe TSPermissionsSetting Win32

Il metodo **AddAccount** prepara l'aggiunta di un account al terminale con il set di autorizzazioni specificato. È possibile aggiungere utenti, gruppi o computer.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AccountName* \[ in\]
</dt> <dd>

Nome dell'account da aggiungere al terminale.

</dd> <dt>

*PermissionPreSet* \[ in\]
</dt> <dd>

Set di autorizzazioni da associare all'account specificato. Questo parametro può essere uno o tutti i valori seguenti. Per ulteriori informazioni, vedere [Servizi Desktop remoto autorizzazioni](terminal-services-permissions.md).

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_ \_Accesso Guest** (0)


</dt> <dd>

L'account dispone di autorizzazioni di accesso.

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_ \_Accesso utente** (1)


</dt> <dd>

L'account dispone delle autorizzazioni seguenti: accesso, informazioni sulle query, invio del messaggio e connessione.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_ Tutti gli \_ accessi** (2)


</dt> <dd>

L'account dispone di tutte le autorizzazioni Servizi Desktop remoto.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Faxcomex. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSPermissionsSetting Win32**](win32-tspermissionssetting.md)
</dt> </dl>

 

