---
title: Metodo SetSingleSession della classe Win32_TerminalServiceSetting
description: Il metodo SetSingleSession imposta la proprietà SingleSession per la classe.
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSingleSession
- Metodo SetSingleSession Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetSingleSession
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302437"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetSingleSession della \_ classe TerminalServiceSetting Win32

Il metodo **SetSingleSession** imposta la proprietà **SingleSession** per la classe.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SingleSession* \[ in\]
</dt> <dd>

Flag che disabilita o Abilita la proprietà **SingleSession** , che determina se gli utenti sono limitati a una o più sessioni di Servizi Desktop remoto.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Disabilitare la proprietà.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Abilitare la proprietà.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

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

 

