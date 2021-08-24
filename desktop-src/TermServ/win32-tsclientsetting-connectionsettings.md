---
title: Metodo ConnectionSettings della classe Win32_TSClientSetting
description: Il metodo ConnectionSettings imposta le impostazioni di sessione applicabili al processo di connessione e accesso.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Metodo ConnectionSettings Servizi Desktop remoto
- Metodo ConnectionSettings Servizi Desktop remoto , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Servizi Desktop remoto , metodo ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f48a93959b1e86eb77f6ab0fbfab444444ca1c077835e1c28330d34ed66c87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656171"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Metodo ConnectionSettings della classe \_ TSClientSetting Win32

Il **metodo ConnectionSettings** imposta le impostazioni di sessione applicabili al processo di connessione e accesso.

## <a name="syntax"></a>Sintassi


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ConnectClientDrivesAtLogon* \[ Pollici\]
</dt> <dd>

Contrassegna l'abilitazione o la disabilitazione della proprietà **ConnectClientDrivesAtLogon** che specifica se le unità del client vengono connesse automaticamente durante la procedura di accesso.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Le unità del client non vengono connesse automaticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Le unità del client vengono connesse automaticamente.

</dd> </dl> </dd> <dt>

*ConnectPrinterAtLogon* \[ Pollici\]
</dt> <dd>

Flag che abilita o disabilita la **proprietà ConnectPrinterAtLogon,** che specifica se tutte le stampanti client locali mappate vengono connesse automaticamente durante la procedura di accesso.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Tutte le stampanti locali mappate non vengono connesse automaticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Tutte le stampanti locali mappate vengono connesse automaticamente.

</dd> </dl> </dd> <dt>

*DefaultToClientPrinter* \[ Pollici\]
</dt> <dd>

Flag che abilita o disabilita la **proprietà DefaultToClientPrinter** che specifica se i processi di stampa vengono inviati automaticamente alla stampante locale del client.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

I processi di stampa non vengono inviati automaticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

I processi di stampa vengono inviati automaticamente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

