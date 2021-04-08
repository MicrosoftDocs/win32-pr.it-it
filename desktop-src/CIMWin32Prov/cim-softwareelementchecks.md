---
description: La \_ classe di associazione CIM SoftwareElementChecks mette in correlazione un elemento software con informazioni sulla condizione o sulla posizione che possono essere richieste da una funzionalità.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementChecks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877485"
---
# <a name="cim_softwareelementchecks-class"></a>CIM \_ SoftwareElementChecks (classe)

La classe di associazione **CIM \_ SoftwareElementChecks** mette in correlazione un elemento software con informazioni sulla condizione o sulla posizione che possono essere richieste da una funzionalità.

Poiché gli elementi software in uno stato pronto per l'esecuzione non possono passare a un altro stato, il valore della proprietà **fase** è limitato allo stato per gli oggetti [**CIM \_ SoftwareElement**](cim-softwareelement.md) in uno stato pronto per l'esecuzione.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a>Members

La classe **CIM \_ SoftwareElementChecks** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ SoftwareElementChecks** dispone di queste proprietà.

<dl> <dt>

**Controllo**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ controllo CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento al controllo.

</dd> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SoftwareElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento all'elemento.

</dd> <dt>

**Fase**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controllo a cui si fa riferimento è un controllo in stato o un controllo di stato successivo.

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

**In-state** (0)


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

**Stato successivo** (1)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per le classi WMI derivate da **CIM \_ SoftwareElementChecks**, vedere [Win32 Classes](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

