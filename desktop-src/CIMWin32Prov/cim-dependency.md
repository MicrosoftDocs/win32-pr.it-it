---
description: La classe Dependency CIM \_ rappresenta un'associazione che stabilisce relazioni di dipendenza tra oggetti.
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: CIM_Dependency classe (provider WMI CIMWin32)
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
ms.openlocfilehash: 1a2c1c568eeb8a3d753479c8663cc04293e76d38c5efb9919ab494b198657efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921941"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a>CIM_Dependency classe (provider WMI CIMWin32)

La **classe \_ Dependency CIM** rappresenta un'associazione che stabilisce relazioni di dipendenza tra oggetti.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe \_ dependency CIM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Dependency CIM** ha queste proprietà.

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

Riferimento all'oggetto dipendente dalla **proprietà Antecedent.**

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per altre informazioni sulle classi derivate **dalla dipendenza \_ CIM,** vedere [Classi Win32.](win32-provider.md)

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




