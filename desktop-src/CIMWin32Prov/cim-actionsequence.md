---
description: L' \_ associazione CIM ActionSequence definisce una serie di operazioni che consentono di eseguire la transizione dell'elemento software (a cui fa riferimento l' \_ associazione CIM SoftwareElementActions) allo stato successivo oppure di rimuovere l'elemento software dallo stato corrente.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: Classe CIM_ActionSequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304783"
---
# <a name="cim_actionsequence-class"></a>CIM \_ ActionSequence (classe)

L'associazione **CIM \_ ActionSequence** definisce una serie di operazioni che consentono di eseguire la transizione dell'elemento software (a cui fa riferimento l'associazione [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) ) allo stato successivo oppure di rimuovere l'elemento software dallo stato corrente.

Le azioni successive e le azioni di disinstallazione associate a un particolare elemento software devono essere una sequenza continua. Poiché **CIM \_ ActionSequence** è un'associazione, i cicli sulla classe [**di \_ azione CIM**](cim-action.md) , con i ruoli per l'azione "Priore" e "Next", formano una sequenza.

La necessità di una sequenza continua implica:

-   All'interno del set di azioni di disinstallazione o di stato successivo, esiste una sola azione che non ha un'istanza dell'associazione **CIM \_ ActionSequence** che fa riferimento a essa nel ruolo "Next". Si tratta della prima azione della sequenza.
-   All'interno del set di azioni di disinstallazione o di stato successivo, esiste una sola azione che non ha un'istanza dell'associazione **CIM \_ ActionSequence** che fa riferimento a essa nel ruolo "Priore". Si tratta dell'ultima azione della sequenza.
-   Tutte le altre azioni all'interno del set di azioni di stato e di disinstallazione successive devono far parte di due istanze dell'associazione **CIM \_ ActionSequence** , una in un ruolo "Priore" e una nel ruolo "Next".

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ActionSequence** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ActionSequence** dispone di queste proprietà.

<dl> <dt>

**Avanti**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ azione CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento all'azione successiva.

</dd> <dt>

**Prima**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ azione CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento all'azione precedente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le classi di [**\_ azione CIM**](cim-action.md) che partecipano a questa associazione devono avere lo stesso valore per la proprietà **Direction** .

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

