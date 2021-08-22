---
title: Win32_RDSHServer classe
description: Gestisce un Desktop remoto host sessione Desktop remoto.
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer classe Servizi Desktop remoto
- Win32_RDSHServer classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: 066cea4044330ab79122e9346f6f32999202f854245e5508448e40aea3521fe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422601"
---
# <a name="win32_rdshserver-class"></a>Classe RDSHServer Win32 \_

Gestisce un Desktop remoto host sessione Desktop remoto.

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

La **classe \_ RDSHServer Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ RDSHServer Win32** include questi metodi.



| Metodo                                                                          | Descrizione                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshserver.md)                   | Recupera un valore della proprietà Integer di un **oggetto \_ RDSHServer Win32.**<br/>                                                                                                 |
| [**GetPendingStartServerList**](win32-rdshserver-getpendingstartserverlist.md) | Recupera un elenco di server in attesa di avvio.<br/>                                                                                                                           |
| [**GetStringProperty**](getstringproperty-win32-rdshserver.md)                 | Recupera il valore di una proprietà stringa di un **oggetto \_ RDSHServer Win32.**<br/>                                                                                                   |
| [**SetInt32Property**](setint32property-win32-rdshserver.md)                   | Aggiorna un valore della proprietà Integer di **un oggetto \_ RDSHServer Win32.**<br/>                                                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdshserver.md)                 | Aggiorna il valore di una proprietà stringa di **un oggetto \_ RDSHServer Win32.**<br/>                                                                                                     |
| [**TestAndSetState**](win32-rdshserver-testandsetstate.md)                     | Confronta lo stato corrente con il confronto specificato. Se i due valori corrispondono, lo stato viene impostato su un nuovo valore. Indipendentemente dalla corrispondenza, viene restituito anche lo stato corrente.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ RDSHServer Win32** ha queste proprietà.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ottiene e imposta l'alias per la raccolta di Host sessione Desktop remoto a cui è assegnato il server Host sessione Desktop remoto.

</dd> <dt>

**ConnectionBroker**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Ottiene e imposta il nome del gestore Connessione Desktop remoto (RDCB) che gestisce l'accesso utente al server Host sessione Desktop remoto.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene e imposta il nome del server Host sessione Desktop remoto.

</dd> <dt>

**Stato server**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Descrive lo stato del server. Qualsiasi valore diverso da **TARGET \_ RUNNING** (3) è riservato e deve essere in considerazione uno stato non valido.

I valori possibili sono .

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**DESTINAZIONE \_ UNKNOWN** (1)


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**DESTINAZIONE \_ RUNNING** (3)


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**DESTINAZIONE \_ INVALID** (8)


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**DESTINAZIONE \_ STARTING** (9)


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**DESTINAZIONE \_ STOPPING** (10)


</dt> <dd></dd> </dl>

**Windows Server 2012 R2 e Windows Server 2012:** Questa proprietà non è disponibile prima Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[provider Desktop remoto Management Services](rdms-api-reference.md)
</dt> </dl>

 

