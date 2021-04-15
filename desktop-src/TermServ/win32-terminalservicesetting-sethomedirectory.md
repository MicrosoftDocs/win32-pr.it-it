---
title: Metodo SetHomeDirectory della classe Win32_TerminalServiceSetting
description: Imposta la proprietà TerminalServicesHomeDirectory per la classe.
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetHomeDirectory
- Metodo SetHomeDirectory Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetHomeDirectory
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517679"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetHomeDirectory della \_ classe TerminalServiceSetting Win32

Il metodo **SetHomeDirectory** imposta la proprietà **TerminalServicesHomeDirectory** per la classe.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HomeDirectory* \[ in\]
</dt> <dd>

Nuovo valore per la proprietà **TerminalServicesHomeDirectory** , che specifica la directory radice del computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce esito positivo in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI. Per un elenco di codici di errore WMI, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

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

 

