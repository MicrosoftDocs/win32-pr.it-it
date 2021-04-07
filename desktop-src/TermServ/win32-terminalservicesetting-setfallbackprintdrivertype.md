---
title: Metodo SetFallbackPrintDriverType della classe Win32_TerminalServiceSetting
description: Il metodo SetFallbackPrintDriverType imposta la proprietà FallbackPrintDriverType per la classe.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetFallbackPrintDriverType
- Metodo SetFallbackPrintDriverType Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetFallbackPrintDriverType
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048686"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Metodo SetFallbackPrintDriverType della \_ classe TerminalServiceSetting Win32

Il metodo **SetFallbackPrintDriverType** imposta la proprietà **FallbackPrintDriverType** per la classe.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FallbackPrintDriverType* \[ in\]
</dt> <dd>

Imposta la proprietà **FallbackPrintDriverType** che consente o nega nuove connessioni di Servizi Desktop remoto.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Nessun driver di fallback.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Migliore ipotesi.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Migliore ipotesi. Se non viene trovata alcuna corrispondenza, eseguire il fallback a Hewlett-Packard PCL (Printer Control Language).

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Migliore ipotesi. Se non viene trovata alcuna corrispondenza, eseguire il fallback a PostScript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Migliore ipotesi. Se non viene trovata alcuna corrispondenza, visualizzare i driver PS e PCL.

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

 

