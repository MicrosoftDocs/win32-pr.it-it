---
title: Metodo GetTStoLSConnectivityStatus della classe Win32_TerminalServiceSetting
description: Determina lo stato di connettività tra Servizi Desktop remoto e un server licenze.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetTStoLSConnectivityStatus
- Metodo GetTStoLSConnectivityStatus Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo GetTStoLSConnectivityStatus
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477447"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>Metodo GetTStoLSConnectivityStatus della \_ classe TerminalServiceSetting Win32

Determina lo stato di connettività tra Servizi Desktop remoto e un server licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nomeserver* \[ in\]
</dt> <dd>

Nome del server licenze di cui verificare lo stato di connettività.

</dd> <dt>

*TStoLSConnectivityStatus* \[ out\]
</dt> <dd>

Valore che indica lo stato di connettività del server licenze. Può corrispondere a uno dei valori seguenti.

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Ls \_ Con connessione \_ sconosciuta** (0)


</dt> <dd>

Impossibile determinare lo stato di connettività.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Ls \_ \_ \_ WS08R2 valido collegabile** (1)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze Windows Server 2008 R2.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Ls \_ \_ \_ WS08 valido collegabile** (2)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze Windows Server 2008.

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Ls \_ \_ \_ \_ Mancata corrispondenza RTM della versione beta** (3)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze, ma uno dei server esegue una versione beta del sistema operativo.

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Ls \_ \_ \_ Versione precedente collegabile** (4)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze, ma esiste un'incompatibilità tra il server licenze e il server host Servizi Desktop remoto.

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Ls \_ CONNESSIONE \_ non \_ in \_ TSCGROUP** (5)


</dt> <dd>

I criteri del gruppo di sicurezza sono abilitati nel server licenze, ma Servizi Desktop remoto non fa parte dei criteri di gruppo.

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Ls \_ NON \_ collegabile** (6)


</dt> <dd>

Servizi Desktop remoto non è in grado di connettersi al server licenze.

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Ls \_ \_ \_ Validità di connessione sconosciuta** (7)


</dt> <dd>

Il server licenze può essere connesso a, ma non è possibile determinare la validità della connessione.

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Ls \_ CONNETTIbile \_ ma \_ accesso \_ negato** (8)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze, ma l'account utente non dispone dei privilegi di amministratore per il server licenze.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Ls \_ WS08R2 valido per la connessione \_ \_ \_ VDI** (9)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server Virtual Desktop Infrastructure (VDI) di Windows Server 2008 R2.

**Windows Server 2008 R2:** Questo valore non è supportato prima di Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Ls \_ \_Funzionalità connettibile \_ non \_ supportata** (10)


</dt> <dd>

La funzionalità non è supportata.

**Windows server 2008 R2 e Windows server 2008 R2 con SP1:** Questo valore non è supportato prima di Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Ls \_ \_ \_ Ls valido collegabile** (11)


</dt> <dd>

Il server licenze è valido.

**Windows server 2008 R2 e Windows server 2008 R2 con SP1:** Questo valore non è supportato prima di Windows Server 2012.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





