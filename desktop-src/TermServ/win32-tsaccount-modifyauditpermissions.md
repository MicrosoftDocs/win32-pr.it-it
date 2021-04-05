---
title: Metodo ModifyAuditPermissions della classe Win32_TSAccount
description: Prepara l'impostazione di un set di autorizzazioni di controllo più granulare per l'account specificato.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ModifyAuditPermissions
- Metodo ModifyAuditPermissions Servizi Desktop remoto, classe Win32_TSAccount
- Classe Win32_TSAccount Servizi Desktop remoto, metodo ModifyAuditPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874441"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a>Metodo ModifyAuditPermissions della \_ classe TSAccount Win32

Il metodo **ModifyAuditPermissions** prepara a impostare un set di autorizzazioni di controllo più granulare per l'account specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PermissionMask* \[ in\]
</dt> <dd>

Set di [host sessione Desktop remoto autorizzazioni](terminal-services-permissions.md) da associare all'account specificato. Il valore di questo parametro è una bitmap ed è possibile selezionare uno o tutti i valori seguenti.

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

*Operazione riuscita* \[ in\]
</dt> <dd>

Specifica se il set di autorizzazioni specificato dal valore del parametro *PermissionMask* è consentito o negato.

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

 

