---
description: La \_ relazione CIM DependencyContext associa una \_ classe di dipendenza CIM a uno o più \_ oggetti di configurazione CIM. Le dipendenze di un sistema di computer, ad esempio, possono variare in base alla rete a cui è collegato il sistema.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: Classe CIM_DependencyContext
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
ms.openlocfilehash: 69319a4f4d228d484da62411060ae3fead90bb79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877914"
---
# <a name="cim_dependencycontext-class"></a>CIM \_ DependencyContext (classe)

La relazione **CIM \_ DependencyContext** associa una classe di [**\_ dipendenza CIM**](cim-dependency.md) a uno o più oggetti di [**\_ configurazione CIM**](cim-configuration.md) . Le dipendenze di un sistema di computer, ad esempio, possono variare in base alla rete a cui è collegato il sistema.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

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

La classe **CIM \_ DependencyContext** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ DependencyContext** dispone di queste proprietà.

<dl> <dt>

**Contesto**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ configurazione CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento all'oggetto di configurazione che aggrega la dipendenza.

</dd> <dt>

**Dipendenza**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ dipendenza CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a una dipendenza aggregata.

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



 

