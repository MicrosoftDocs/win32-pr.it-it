---
description: La \_ classe di esportazione CIM rappresenta un'associazione tra un file system locale e le relative directory, che indicano che le directory specificate sono disponibili per il montaggio.
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: Classe CIM_Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966162"
---
# <a name="cim_export-class"></a>\_Classe di esportazione CIM

La classe di **\_ esportazione CIM** rappresenta un'associazione tra un file system locale e le relative directory, che indicano che le directory specificate sono disponibili per il montaggio. Quando si esporta un intero file system, la directory deve fare riferimento alla directory più in alto della file system.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a>Members

La classe di **\_ esportazione CIM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe di **\_ esportazione CIM** dispone di queste proprietà.

<dl> <dt>

**Directory**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ directory CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla directory esportata per il montaggio di network file system (NFS).

</dd> <dt>

**ExportedDirectoryName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome con cui viene esportata la directory.

</dd> <dt>

**LocalFS**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LocalFileSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Riferimento al file system locale.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

