---
title: Win32_SessionDirectoryCluster classe
description: Fornisce le proprietà per la visualizzazione delle proprietà di una farm in Connessione Desktop remoto Broker (Gestore connessione Desktop remoto).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster classe Servizi Desktop remoto
- Win32_SessionDirectoryCluster classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1dba262ddb332f03c7f398c4f205e73a9c9e94054d4164fb94c8c01dc8b505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127081"
---
# <a name="win32_sessiondirectorycluster-class"></a>Classe \_ SessionDirectoryCluster Win32

Fornisce le proprietà per la visualizzazione delle proprietà di una farm in Connessione Desktop remoto Broker (Gestore connessione Desktop remoto).

> [!Note]  
> In Windows Server 2008 R2 il nome di Gestore sessione Servizi terminal è stato modificato in Gestore connessione Desktop remoto. Queste proprietà si applicano a tutti i sistemi operativi supportati, se non diversamente specificato.

 

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 SessionDirectoryCluster** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Win32 SessionDirectoryCluster** ha queste proprietà.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome della farm in Gestore connessione Desktop remoto.

</dd> <dt>

**NumberOfServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di server nella farm in Gestore connessione Desktop remoto.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modalità sessione singola della farm in Gestore connessione Desktop remoto.

<dt>

0
</dt> <dd>

La farm in Gestore connessione Desktop remoto non è in modalità sessione singola.

</dd> <dt>

1
</dt> <dd>

La farm in Gestore connessione Desktop remoto è in modalità sessione singola.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ SessionDirectoryServer**](win32-sessiondirectoryserver.md)
</dt> <dt>

[**Win32 \_ SessionDirectorySession**](win32-sessiondirectorysession.md)
</dt> </dl>

 

