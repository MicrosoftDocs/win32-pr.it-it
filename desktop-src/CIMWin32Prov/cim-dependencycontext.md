---
description: La relazione DependencyContext CIM \_ associa una classe Dependency CIM \_ a uno o più oggetti di configurazione \_ CIM. Ad esempio, le dipendenze di un sistema di computer possono cambiare in base alla rete a cui è collegato il sistema.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: CIM_DependencyContext classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 845086b7d41eb03227d6b5b47240ef4bf9e1a2c35f8049c96d5c665800b327e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924641"
---
# <a name="cim_dependencycontext-class"></a>Classe \_ DependencyContext CIM

La **relazione \_ DependencyContext CIM** associa una classe [**\_ Dependency CIM**](cim-dependency.md) a uno o più oggetti di configurazione [**CIM. \_**](cim-configuration.md) Ad esempio, le dipendenze di un sistema di computer possono cambiare in base alla rete a cui è collegato il sistema.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a>Members

La **classe \_ DependencyContext CIM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CiM DependencyContext** ha queste proprietà.

<dl> <dt>

**Contesto**
</dt> <dd> <dl> <dt>

Tipo di dati: **Configurazione \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento all'oggetto di configurazione che aggrega la dipendenza.

</dd> <dt>

**Dipendenza**
</dt> <dd> <dl> <dt>

Tipo di dati: **dipendenza \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a una dipendenza aggregata.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

