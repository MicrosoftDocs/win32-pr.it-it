---
title: Classe Win32_RDSHServer
description: Gestisce un server host sessione Desktop remoto (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDSHServer Servizi Desktop remoto
- Classe Win32_RDSHServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340722"
---
# <a name="win32_rdshserver-class"></a>Win32 \_ RDSHServer (classe)

Gestisce un server host sessione Desktop remoto (RDSH).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDSHServer** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ RDSHServer** presenta questi metodi.



| Metodo                                                                          | Descrizione                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshserver.md)                   | Recupera un valore di proprietà Integer di un oggetto **Win32 \_ RDSHServer** .<br/>                                                                                                 |
| [**GetPendingStartServerList**](win32-rdshserver-getpendingstartserverlist.md) | Recupera un elenco di server in attesa di avvio.<br/>                                                                                                                           |
| [**GetStringProperty**](getstringproperty-win32-rdshserver.md)                 | Recupera un valore della proprietà di stringa di un oggetto **Win32 \_ RDSHServer** .<br/>                                                                                                   |
| [**SetInt32Property**](setint32property-win32-rdshserver.md)                   | Aggiorna un valore della proprietà Integer di un oggetto **Win32 \_ RDSHServer** .<br/>                                                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdshserver.md)                 | Aggiorna il valore di una proprietà di stringa di un oggetto **Win32 \_ RDSHServer** .<br/>                                                                                                     |
| [**TestAndSetState**](win32-rdshserver-testandsetstate.md)                     | Confronta lo stato corrente con il comparand specificato. Se le due corrispondenze, lo stato viene impostato su un nuovo valore. Indipendentemente dalla corrispondenza, viene restituito anche lo stato corrente.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ RDSHServer** dispone di queste proprietà.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ottiene e imposta l'alias della raccolta RDSH a cui è assegnato il server RDSH.

</dd> <dt>

**ConnectionBroker**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il nome del broker di Connessione Desktop remoto (RDCB) che gestisce l'accesso degli utenti al server RDSH.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene e imposta il nome del server RDSH.

</dd> <dt>

**ServerState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Descrive lo stato del server. Qualsiasi valore diverso da **target \_ Running** (3) è riservato e deve essere considerato uno stato non valido.

I valori possibili sono.

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**Destinazione \_ SCONOSCIUTO** (1)


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**Destinazione \_ IN esecuzione** (3)


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**Destinazione \_ NON valido** (8)


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**Destinazione \_ INIZIO** (9)


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**Destinazione \_ ARRESTO** in corso (10)


</dt> <dd></dd> </dl>

**Windows server 2012 R2 e Windows server 2012:** Questa proprietà non è disponibile prima di Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider di Desktop remoto Management Services](rdms-api-reference.md)
</dt> </dl>

 

