---
title: Win32_SessionBrokerServiceProperties classe
description: Definisce la query per un servizio broker di sessione.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties classe Servizi Desktop remoto
- Win32_SessionBrokerServiceProperties classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: 3f095272ee0d836e77542e20badbe5bb1169206cc6b0e87d742e3fbd235acd52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656181"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>Classe \_ SessionBrokerServiceProperties Win32

Definisce la query per un servizio broker di sessione.

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

La **classe Win32 \_ SessionBrokerServiceProperties** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](/windows)

### <a name="methods"></a>Metodi

La **classe Win32 \_ SessionBrokerServiceProperties** include questi metodi.



| Metodo                                                                                                | Descrizione                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteSBDbConnectionString**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | Elimina le stringhe di connessione del database (primarie e secondarie) dal Registro di sistema.<br/> **Windows Server 2012 R2, Windows Server 2012 e Windows Server 2008 R2:** Questo metodo non è disponibile prima di Windows Server 2016<br/> |
| [**InstallBrokerDatabase**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | Installa il database di Gestore connessione Desktop remoto nel server SQL Server<br/>                                                                                                                                                                    |
| [**IsDbReachable**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | Verifica se il database è raggiungibile<br/>                                                                                                                                                                                                 |
| [**SetBrokerHAMode**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | Esegue la migrazione dei dati dal database WID locale al nuovo database SQL Server database basato su . Configura anche il server broker per l'uso dell'SQL Server<br/>                                                                                        |
| [**SetBrokerNonHAMode**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | Esegue la migrazione dei dati dalla SQL Server centrale al database locale. Configura anche il server broker per l'uso del database locale.<br/>                                                                                                              |
| [**SetSBDbConnectionStrings**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | Salva le stringhe di connessione del database (primaria e secondaria) nel Registro di sistema.<br/> **Windows Server 2012 R2, Windows Server 2012 e Windows Server 2008 R2:** Questo metodo non è disponibile prima di Windows Server 2016<br/>     |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ SessionBrokerServiceProperties** ha queste proprietà.

<dl> <dt>

**SBDbConnectionString**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Stringa di connessione del database utilizzata dal servizio Session Broker.

**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012

</dd> <dt>

**SBDbSecondaryConnectionString**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

facoltativo. Stringa di connessione del database secondario, usata dal servizio Session Broker per supportare la scadenza della password.

**Windows Server 2012 R2, Windows Server 2012 e Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2016

</dd> <dt>

**SBNetworkName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di rete utilizzato dal servizio di broker di sessione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

