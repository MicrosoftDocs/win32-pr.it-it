---
title: Metodo SetSessionDirectoryActive della classe Win32_TSSessionDirectory
description: Il metodo SetSessionDirectoryActive imposta la proprietà SessionDirectoryActive.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- Metodo SetSessionDirectoryActive Servizi Desktop remoto
- Metodo SetSessionDirectoryActive Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto, metodo SetSessionDirectoryActive
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ae44c471c653a3fcdfbab33ab70178b53c95715cce7cfba63defa9c96c1ab23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769351"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a>Metodo SetSessionDirectoryActive della classe \_ Win32 TSSessionDirectory

Il **metodo SetSessionDirectoryActive** imposta la **proprietà SessionDirectoryActive.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SessionDirectoryActive* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Flag che disabilita o abilita il servizio directory di sessione.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Disabilitare il servizio directory di sessione.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Abilitare il servizio directory di sessione.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

