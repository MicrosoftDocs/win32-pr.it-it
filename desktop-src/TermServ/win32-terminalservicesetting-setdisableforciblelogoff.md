---
title: Metodo SetDisableForcibleLogoff della classe Win32_TerminalServiceSetting
description: Questo metodo non è supportato.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetDisableForcibleLogoff
- Metodo SetDisableForcibleLogoff Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetDisableForcibleLogoff
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ae62db188d0e3aa31ffd8e3993e793e9bb2bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476403"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetDisableForcibleLogoff della \_ classe TerminalServiceSetting Win32

Questo metodo non è supportato.

**Windows Vista e Windows Server 2008:** Abilita o Disabilita se un amministratore connesso alla console di può essere disconnesso forzatamente.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DisableForcibleLogoff* \[ in\]
</dt> <dd>

Contrassegnare la disabilitazione o l'abilitazione della proprietà **DisableForcibleLogoff** , che determina se un amministratore che è connesso alla console può essere disconnesso in modo forzato.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Disabilitare la proprietà. L'amministratore connesso può essere disconnesso in modo forzato.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Abilitare la proprietà. Non è possibile disconnettere forzatamente l'amministratore connesso.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce esito positivo in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Fine del supporto client<br/>    | Windows Vista<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





