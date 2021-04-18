---
title: Classe Win32_SessionBrokerServiceProperties
description: Definisce la query per un servizio di gestore sessioni.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518981"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>Win32 \_ SessionBrokerServiceProperties (classe)

Definisce la query per un servizio di gestore sessioni.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SessionBrokerServiceProperties** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](/windows)

### <a name="methods"></a>Metodi

La classe **Win32 \_ SessionBrokerServiceProperties** presenta questi metodi.



| Metodo                                                                                                | Descrizione                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteSBDbConnectionString**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | Elimina le stringhe di connessione del database (primaria e secondaria) dal registro di sistema.<br/> **Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Questo metodo non è disponibile prima di Windows Server 2016<br/> |
| [**InstallBrokerDatabase**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | Installa il database gestore connessione Desktop remoto nella SQL Server centrale<br/>                                                                                                                                                                    |
| [**IsDbReachable**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | Controlla se il database è raggiungibile<br/>                                                                                                                                                                                                 |
| [**SetBrokerHAMode**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | Esegue la migrazione dei dati dal database WID locale al nuovo database basato su SQL Server. Configura inoltre il server Broker per l'utilizzo della SQL Server centrale<br/>                                                                                        |
| [**SetBrokerNonHAMode**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | Esegue la migrazione dei dati dal SQL Server centrale al database locale. Configura inoltre il server Broker per l'utilizzo del database locale.<br/>                                                                                                              |
| [**SetSBDbConnectionStrings**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | Salva le stringhe di connessione del database (primaria e secondaria) nel registro di sistema.<br/> **Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Questo metodo non è disponibile prima di Windows Server 2016<br/>     |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SessionBrokerServiceProperties** dispone di queste proprietà.

<dl> <dt>

**SBDbConnectionString**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Stringa di connessione del database utilizzata dal servizio Gestore sessioni.

**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012

</dd> <dt>

**SBDbSecondaryConnectionString**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

facoltativo. Stringa di connessione al database secondario, usata dal servizio Broker di sessione per supportare la scadenza della password.

**Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2016

</dd> <dt>

**SBNetworkName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di rete utilizzato dal servizio Broker di sessione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

