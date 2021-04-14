---
title: Metodo SetAllowTSConnections della classe Win32_TerminalServiceSetting
description: Il metodo SetAllowTSConnections consente o nega nuove connessioni Desktop remoto. Questo metodo modificherà la proprietà AllowTSConnections per la classe di conseguenza.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetAllowTSConnections
- Metodo SetAllowTSConnections Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetAllowTSConnections
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478833"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetAllowTSConnections della \_ classe TerminalServiceSetting Win32

Il metodo **SetAllowTSConnections** consente o nega nuove connessioni Desktop remoto. Questo metodo modificherà la proprietà **AllowTSConnections** per la classe di conseguenza.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AllowTSConnections* \[ in\]
</dt> <dd>

Specifica se sono consentite nuove connessioni Desktop remoto. Deve essere uno dei valori seguenti.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Non sono consentite nuove connessioni. Se il parametro *ModifyFirewallException* è 1, l'eccezione desktop remoto firewall è disabilitata.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Sono consentite nuove connessioni. Se il parametro *ModifyFirewallException* è 1, l'eccezione desktop remoto firewall è abilitata.

</dd> </dl> </dd> <dt>

*ModifyFirewallException* \[ in\]
</dt> <dd>

Specifica se l'impostazione di eccezione del firewall per Desktop remoto verrà modificata nello stato specificato dal parametro *AllowTSConnections* . Deve essere uno dei valori seguenti.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Non modificare l'impostazione delle eccezioni del firewall.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Modificare l'impostazione di eccezione del firewall.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce esito positivo in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

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

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

