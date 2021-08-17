---
title: Metodo ModifyPermissions della Win32_TSAccount classe
description: Imposta un'autorizzazione per l'account specificato.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- Metodo ModifyPermissions Servizi Desktop remoto
- Metodo ModifyPermissions Servizi Desktop remoto , Win32_TSAccount classe
- Win32_TSAccount classe Servizi Desktop remoto, metodo ModifyPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6265290fa3604c426609f51d0518f1f6762ea02718757d86ff9ed69b10bd018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119421671"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a>Metodo ModifyPermissions della classe TSAccount Win32 \_

Imposta un'autorizzazione per l'account specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PermissionMask* \[ Pollici\]
</dt> <dd>

Autorizzazione [Desktop remoto host sessione da](terminal-services-permissions.md) impostare.

I valori possibili sono:

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_ QUERY** (0)


</dt> <dd>

Autorizzazione per eseguire query sulle informazioni su una sessione.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ SET** (1)


</dt> <dd>

Autorizzazione per la modifica dei parametri di connessione.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ RESET** (6)


</dt> <dd>

Autorizzazione per reimpostare o terminare una sessione o una connessione.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ DIRITTI \| STANDARD \_ VIRTUALI \_ RICHIESTI** (3)


</dt> <dd>

Autorizzazione per l'uso di canali virtuali. I canali virtuali forniscono l'accesso da un programma server ai dispositivi client.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ SHADOW** (4)


</dt> <dd>

Autorizzazione per lo shadow o il controllo remoto della sessione di un altro utente.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ LOGON** (5)


</dt> <dd>

Autorizzazione per accedere a una sessione nel server.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ LOGOFF** (2)


</dt> <dd>

Autorizzazione per disconnettere un utente da una sessione.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MSG** (7)


</dt> <dd>

Autorizzazione per inviare un messaggio a una sessione di un altro utente.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ CONNECT** (8)


</dt> <dd>

Autorizzazione per la connessione a un'altra sessione.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ DISCONNECT** (9)


</dt> <dd>

Autorizzazione per disconnettere una sessione.

</dd> </dl> </dd> <dt>

*Consenti* \[ Pollici\]
</dt> <dd>

Specifica se l'autorizzazione nel *parametro PermissionMask* è consentita o negata.

I valori possibili sono:

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Il set di autorizzazioni specificato è consentito.

</dd> <dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Il set di autorizzazioni specificato è negato.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Account \_ TS Win32**](win32-tsaccount.md)
</dt> </dl>

 

