---
title: Metodo GetTStoLSConnectivityStatus della Win32_TerminalServiceSetting classe
description: Determina lo stato di connettività tra Servizi Desktop remoto e un server licenze.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Metodo GetTStoLSConnectivityStatus Servizi Desktop remoto
- Metodo GetTStoLSConnectivityStatus Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto metodo , GetTStoLSConnectivityStatus
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
ms.openlocfilehash: ff79de8bc1740e659b8f0398c0fa84958c1bfcffda505f1a26322da442dcc19b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059569"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>Metodo GetTStoLSConnectivityStatus della classe TerminalServiceSetting Win32 \_

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

*NomeServer* \[ Pollici\]
</dt> <dd>

Nome del server licenze di cui controllare lo stato di connettività.

</dd> <dt>

*TStoLSConnectivityStatus* \[ Cambio\]
</dt> <dd>

Valore che indica lo stato di connettività del server licenze. Può essere uno dei valori seguenti.

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS \_ CONNECTABLE \_ UNKNOWN** (0)


</dt> <dd>

Non è possibile determinare lo stato della connettività.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS \_ \_ \_ WS08R2 VALIDO COLLEGABILE** (1)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze Windows Server 2008 R2.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS \_ \_ \_ WS08 VALIDO COLLEGABILE** (2)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze Windows Server 2008.

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS \_ MANCATA \_ CORRISPONDENZA \_ DI CONNECTABLE BETA RTM \_** (3)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze, ma uno dei server esegue una versione beta del sistema operativo.

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS \_ VERSIONE \_ PRECEDENTE \_ COLLEGABILE** (4)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze, ma esiste un'incompatibilità tra il server licenze e il server host Servizi Desktop remoto licenze.

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS \_ CONNECTABLE \_ NOT \_ IN \_ TSCGROUP** (5)


</dt> <dd>

I criteri di gruppo di sicurezza sono abilitati nel server licenze, Servizi Desktop remoto non fanno parte dei criteri di gruppo.

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS \_ NON \_ COLLEGABILE** (6)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze.

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS \_ VALIDITÀ \_ \_ SCONOSCIUTA COLLEGABILE** (7)


</dt> <dd>

Il server licenze può essere connesso, ma non è possibile determinare la validità della connessione.

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS \_ CONNETTIBILE \_ MA \_ ACCESSO \_ NEGATO** (8)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server licenze, ma l'account utente non dispone dei privilegi di amministratore nel server licenze.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS \_ VDI \_ \_ WS08R2 \_ VALIDO COLLEGABILE** (9)


</dt> <dd>

Servizi Desktop remoto possibile connettersi al server Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI).

**Windows Server 2008 R2:** Questo valore non è supportato prima di Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS \_ FUNZIONALITÀ \_ COLLEGABILE \_ NON \_ SUPPORTATA** (10)


</dt> <dd>

La funzionalità non è supportata.

**Windows Server 2008 R2 e Windows Server 2008 R2 con SP1:** Questo valore non è supportato prima di Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS \_ LS \_ VALIDO \_ COLLEGABILE** (11)


</dt> <dd>

Il server licenze è valido.

**Windows Server 2008 R2 e Windows Server 2008 R2 con SP1:** Questo valore non è supportato prima di Windows Server 2012.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto di questi valori,](terminal-services-wmi-provider-error-codes.md) fare riferimento Servizi Desktop remoto di errore del provider WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Terminale Win32ServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





