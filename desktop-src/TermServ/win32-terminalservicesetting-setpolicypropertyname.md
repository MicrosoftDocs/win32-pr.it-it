---
title: Metodo SetPolicyPropertyName della classe Win32_TerminalServiceSetting
description: Il metodo SetPolicyPropertyName imposta la proprietà DeleteTempFolders, UseTempFolders o help per la classe.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetPolicyPropertyName
- Metodo SetPolicyPropertyName Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetPolicyPropertyName
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478832"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetPolicyPropertyName della \_ classe TerminalServiceSetting Win32

Il metodo **SetPolicyPropertyName** imposta la proprietà **DeleteTempFolders**, **UseTempFolders** o **Help** per la classe.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PropertyName* \[ in\]
</dt> <dd>

Specifica la proprietà dei criteri che il metodo sta impostando.

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**


</dt> <dd>

Il metodo sta impostando la proprietà **DeleteTempFolders** .

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**


</dt> <dd>

Il metodo sta impostando la proprietà **UseTempFolders** .

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>**Guida**


</dt> <dd>

Il metodo sta impostando la proprietà della **Guida** .

**Nota** la **Guida** non è supportata  

</dd> </dl> </dd> <dt>

*Valore* \[ di in\]
</dt> <dd>

Valore che indica se abilitare o disabilitare la proprietà specificata dal parametro *PropertyName* .

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

Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

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

 

