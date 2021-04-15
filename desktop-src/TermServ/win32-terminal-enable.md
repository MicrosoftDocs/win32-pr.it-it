---
title: Metodo Enable della classe Win32_Terminal
description: Il metodo Enable Disabilita o Abilita il terminale.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Abilita Servizi Desktop remoto metodo
- Enable Servizi Desktop remoto metodo, classe Win32_Terminal
- Classe Win32_Terminal Servizi Desktop remoto, metodo Enable
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400368"
---
# <a name="enable-method-of-the-win32_terminal-class"></a>Metodo Enable della \_ classe terminale Win32

Il metodo **Enable** Disabilita o Abilita il terminale.

## <a name="syntax"></a>Sintassi


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fEnableTerminal* \[ in\]
</dt> <dd>

Flag che disabilita o Abilita il terminale.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Il terminale è disabilitato.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Il terminale è abilitato.

</dd> </dl> </dd> </dl>

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

[**\_Terminale Win32**](win32-terminal.md)
</dt> </dl>

 

