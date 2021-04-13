---
title: Classe Win32_RDMSCollectionProperties
description: Gestisce le proprietà di un insieme di desktop virtuali.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSCollectionProperties Servizi Desktop remoto
- Classe Win32_RDMSCollectionProperties Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400519"
---
# <a name="win32_rdmscollectionproperties-class"></a>Win32 \_ RDMSCollectionProperties (classe)

Gestisce le proprietà di un insieme di desktop virtuali.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDMSCollectionProperties** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](/windows)

### <a name="methods"></a>Metodi

La classe **Win32 \_ RDMSCollectionProperties** presenta questi metodi.



| Metodo                                                                                        | Descrizione                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**GetProvisioningProperties**](getprovisioningproperties-win32-rdmscollectionproperties.md) | Recupera le proprietà di provisioning dell'insieme di desktop virtuali.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ RDMSCollectionProperties** dispone di queste proprietà.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene l'alias della raccolta.

</dd> <dt>

**ReferenceVirtualDesktopAdapters**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta i nomi delle schede di rete virtuali della macchina virtuale master.

</dd> <dt>

**ReferenceVirtualDesktopArchitecture**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta l'architettura del processore della macchina virtuale master.

</dd> <dt>

**ReferenceVirtualDesktopGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il GUID della macchina virtuale master.

</dd> <dt>

**ReferenceVirtualDesktopHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il nome del server host della macchina virtuale master.

</dd> <dt>

**ReferenceVirtualDesktopMachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il nome del computer della macchina virtuale master.

</dd> <dt>

**ReferenceVirtualDesktopName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta il nome della macchina virtuale master.

</dd> <dt>

**ReferenceVirtualDesktopOsversion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta la versione del sistema operativo della macchina virtuale master.

</dd> <dt>

**ReferenceVirtualDesktopRamsizeMB**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta le dimensioni della memoria della macchina virtuale master.

</dd> <dt>

**ReferenceVirtualDesktopRemoteFX**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene e imposta un valore che indica se RemoteFX è abilitato per la macchina virtuale master. **True** se RemoteFX è abilitato; in caso contrario, **false**. Il valore predefinito per questa proprietà è **false**.

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

 

