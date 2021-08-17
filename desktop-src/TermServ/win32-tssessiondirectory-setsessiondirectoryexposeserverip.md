---
title: Metodo SetSessionDirectoryExposeServerIP della classe Win32_TSSessionDirectory
description: Imposta la proprietà SessionDirectoryExposeServerIP.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- Metodo SetSessionDirectoryExposeServerIP Servizi Desktop remoto
- Metodo SetSessionDirectoryExposeServerIP Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto metodo SetSessionDirectoryExposeServerIP
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7267a8462e89bdd995896a97fad82cb84ae4e8a36037e39767eca1239611af29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137604"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a>Metodo SetSessionDirectoryExposeServerIP della classe \_ Win32 TSSessionDirectory

Imposta la **proprietà SessionDirectoryExposeServerIP.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SessionDirectoryExposeServerIP* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Contrassegna la disabilitazione o l'abilitazione della proprietà **SessionDirectoryExposeServerIP** che consente o nega il recupero dell'indirizzo IP per la directory di sessione.

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

Tipo: **uint32**

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

