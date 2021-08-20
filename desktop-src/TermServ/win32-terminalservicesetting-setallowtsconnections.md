---
title: Metodo SetAllowTSConnections della Win32_TerminalServiceSetting classe
description: Il metodo SetAllowTSConnections consente o nega nuove connessioni Desktop remoto. Questo metodo modificherà di conseguenza la proprietà AllowTSConnections per la classe .
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Metodo SetAllowTSConnections Servizi Desktop remoto
- Metodo SetAllowTSConnections Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto, metodo SetAllowTSConnections
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
ms.openlocfilehash: 63f8e9be06a19599f578089fa979d7fd93a7bf457fcadf033ed0ab56fea4947f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127027"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetAllowTSConnections della classe TerminalServiceSetting Win32 \_

Il **metodo SetAllowTSConnections** consente o nega nuove connessioni Desktop remoto. Questo metodo modificherà di conseguenza la proprietà **AllowTSConnections** per la classe .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AllowTSConnections* \[ Pollici\]
</dt> <dd>

Specifica se sono consentite nuove connessioni Desktop remoto. Deve essere uno dei valori seguenti.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Non sono consentite nuove connessioni. Se il *parametro ModifyFirewallException* è 1, l'eccezione Desktop remoto firewall è disabilitata.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Sono consentite nuove connessioni. Se il *parametro ModifyFirewallException* è 1, l'eccezione Desktop remoto firewall è abilitata.

</dd> </dl> </dd> <dt>

*ModifyFirewallException* \[ Pollici\]
</dt> <dd>

Specifica se l'impostazione dell'eccezione del firewall Desktop remoto verrà modificata nello stato specificato dal *parametro AllowTSConnections.* Deve essere uno dei valori seguenti.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Non modificare l'impostazione dell'eccezione del firewall.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Modificare l'impostazione dell'eccezione del firewall.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce Success in esito positivo; In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_Terminale Win32ServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

