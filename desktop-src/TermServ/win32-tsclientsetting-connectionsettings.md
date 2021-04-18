---
title: Metodo ConnectionSettings della classe Win32_TSClientSetting
description: Il Metodo ConnectionSettings imposta le impostazioni di sessione che si applicano al processo di connessione e accesso.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo ConnectionSettings
- Metodo ConnectionSettings Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, Metodo ConnectionSettings
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
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517674"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Metodo ConnectionSettings della \_ classe TSClientSetting Win32

Il metodo **ConnectionSettings** imposta le impostazioni di sessione che si applicano al processo di connessione e accesso.

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

*ConnectClientDrivesAtLogon* \[ in\]
</dt> <dd>

Flag che Abilita o Disabilita la proprietà **ConnectClientDrivesAtLogon** che specifica se le unità del client vengono connesse automaticamente durante la procedura di accesso.

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

*ConnectPrinterAtLogon* \[ in\]
</dt> <dd>

Flag che Abilita o Disabilita la proprietà **ConnectPrinterAtLogon** , che specifica se tutte le stampanti client locali mappate vengono connesse automaticamente durante la procedura di accesso.

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

*DefaultToClientPrinter* \[ in\]
</dt> <dd>

Flag che Abilita o Disabilita la proprietà **DefaultToClientPrinter** che specifica se i processi di stampa vengono inviati automaticamente alla stampante locale del client.

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

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.

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

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

