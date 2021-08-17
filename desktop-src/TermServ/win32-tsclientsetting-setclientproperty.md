---
title: Metodo SetClientProperty della Win32_TSClientSetting classe
description: Il metodo SetClientProperty imposta la proprietà LPTPortMapping, COMPortMapping, AudioMapping, ClipboardMapping, DriveMapping o WindowsPrinterMapping per la classe.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- Metodo SetClientProperty Servizi Desktop remoto
- Metodo SetClientProperty Servizi Desktop remoto , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Servizi Desktop remoto, metodo SetClientProperty
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017a771022e0f5edc7d4abe22501fc8dfadc006e01ed2642f95f9c39f101eef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127017"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a>Metodo SetClientProperty della classe \_ Win32 TSClientSetting

Il **metodo SetClientProperty** imposta la proprietà **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** o **WindowsPrinterMapping** per la classe .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PropertyName* \[ Pollici\]
</dt> <dd>

Specifica la proprietà client impostata dal metodo .

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**Mapping audio**


</dt> <dd>

Il metodo imposta la **proprietà AudioMapping.**

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**


</dt> <dd>

Il metodo imposta la **proprietà ClipboardMapping.**

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**ComPortMapping**


</dt> <dd>

Il metodo imposta la **proprietà COMPortMapping.**

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**Mapping di unità**


</dt> <dd>

Il metodo imposta la **proprietà DriveMapping.**

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**


</dt> <dd>

Il metodo imposta la **proprietà LPTPortMapping.**

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**


</dt> <dd>

Il metodo imposta la **proprietà PNPRedirection.**

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**


</dt> <dd>

Il metodo imposta la **proprietà WindowsPrinterMapping.**

</dd> </dl> </dd> <dt>

*Valore* \[ Pollici\]
</dt> <dd>

Valore che indica se abilitare o disabilitare la proprietà specificata dal *parametro PropertyName.*

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Disabilitare la proprietà .

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Abilitare la proprietà .

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se la proprietà client specificata non è sotto il controllo di Criteri di gruppo o se l'impostazione della proprietà non è idonea per l'override da parte del server.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

