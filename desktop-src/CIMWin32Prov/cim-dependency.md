---
description: La \_ classe di dipendenza CIM rappresenta un'associazione che stabilisce relazioni di dipendenza tra oggetti.
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: Classe CIM_Dependency (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b95d45efff51128b08dc5b6395309f49e85a79e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748498"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a>Classe CIM_Dependency (provider WMI CIMWin32)

La classe di **\_ dipendenza CIM** rappresenta un'associazione che stabilisce relazioni di dipendenza tra oggetti.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a>Members

La classe di **\_ dipendenza CIM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe di **\_ dipendenza CIM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'oggetto indipendente in questa associazione.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'oggetto che dipende dalla proprietà **precedente** .

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per ulteriori informazioni sulle classi derivate dalla **\_ dipendenza CIM**, vedere [classi Win32](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




