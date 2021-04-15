---
title: Metodo GetTSLanaIds della classe Win32_TerminalServiceSetting
description: Ottiene gli ID della scheda di rete locale NetBIOS (LANA) e le descrizioni delle schede di rete Servizi Desktop remoto.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetTSLanaIds
- Metodo GetTSLanaIds Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo GetTSLanaIds
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d2b2357df7e6d7ccc2cb8a774ba34c50cb46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479307"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a>Metodo GetTSLanaIds della \_ classe TerminalServiceSetting Win32

Il metodo **GetTSLanaIds** ottiene gli ID della scheda di rete locale (lana) NetBIOS e le descrizioni delle schede di rete Servizi Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LanaIdList* \[ out\]
</dt> <dd>

Matrice di numeri di LANA.

</dd> <dt>

*LanaIdDescriptions* \[ out\]
</dt> <dd>

Matrice di descrizioni di LANA corrispondenti alla matrice *LanaIdList* .

</dd> </dl>

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

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

