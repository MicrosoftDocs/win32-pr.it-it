---
title: Metodo ModifyPermissions della classe Win32_TSAccount
description: Imposta un'autorizzazione per l'account specificato.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ModifyPermissions
- Metodo ModifyPermissions Servizi Desktop remoto, classe Win32_TSAccount
- Classe Win32_TSAccount Servizi Desktop remoto, metodo ModifyPermissions
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
ms.openlocfilehash: c4bf6147c215475314f65bb8fa426442884bc82e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301509"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a>Metodo ModifyPermissions della \_ classe TSAccount Win32

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

*PermissionMask* \[ in\]
</dt> <dd>

[Autorizzazione host sessione Desktop remoto](terminal-services-permissions.md) da impostare.

I valori possibili sono:

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_ QUERY** (0)


</dt> <dd>

Autorizzazione per eseguire query sulle informazioni relative a una sessione.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ IMPOSTA** (1)


</dt> <dd>

Autorizzazione per la modifica dei parametri di connessione.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ Reimposta** (6)


</dt> <dd>

Autorizzazione per reimpostare o terminare una sessione o una connessione.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ \| Diritti standard \_ virtuali \_ richiesti** (3)


</dt> <dd>

Autorizzazione per l'utilizzo di canali virtuali. I canali virtuali forniscono l'accesso da un programma server ai dispositivi client.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ OMBREGGIAtura** (4)


</dt> <dd>

Autorizzazione per nascondere o controllare in modalità remota la sessione di un altro utente.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ ACCESSO** (5)


</dt> <dd>

Autorizzazione per accedere a una sessione nel server.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ Disconnessione** (2)


</dt> <dd>

Autorizzazione per disconnettere un utente da una sessione.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MESSAGGIO** (7)


</dt> <dd>

Autorizzazione per l'invio di un messaggio alla sessione di un altro utente.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ Connetti** (8)


</dt> <dd>

Autorizzazione per la connessione a un'altra sessione.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ Disconnetti** (9)


</dt> <dd>

Autorizzazione per disconnettere una sessione.

</dd> </dl> </dd> <dt>

*Consenti* \[ in\]
</dt> <dd>

Specifica se l'autorizzazione nel parametro *PermissionMask* è consentita o negata.

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

Il set di autorizzazioni specificato è stato negato.

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
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSAccount Win32**](win32-tsaccount.md)
</dt> </dl>

 

