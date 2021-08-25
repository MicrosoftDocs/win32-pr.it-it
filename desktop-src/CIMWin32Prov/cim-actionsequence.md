---
description: L'associazione CIM ActionSequence definisce una serie di operazioni che passano l'elemento software (a cui fa riferimento l'associazione \_ CIM SoftwareElementActions) allo stato successivo o rimuove l'elemento software dallo stato \_ corrente.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: CIM_ActionSequence classe
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
ms.openlocfilehash: a199671dd9f88cd81be50af537e156892e8cab653c70677de27c6e5df02f1d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801081"
---
# <a name="cim_actionsequence-class"></a>Classe CIM \_ ActionSequence

L'associazione **CIM \_ ActionSequence** definisce una serie di operazioni che passano l'elemento software (a cui fa riferimento l'associazione [**\_ CIM SoftwareElementActions)**](cim-softwareelementactions.md) allo stato successivo o rimuove l'elemento software dallo stato corrente.

Le azioni di stato successivo e le azioni di disinstallazione associate a un particolare elemento software devono essere una sequenza continua. Poiché **CIM \_ ActionSequence** è un'associazione, i cicli nella classe [**\_ Action CIM,**](cim-action.md) con i ruoli per l'azione "prior" e l'azione "next", formano una sequenza.

La necessità di una sequenza continua implica:

-   All'interno del set di azioni di stato successivo o di disinstallazione è presente una sola azione che non dispone di un'istanza dell'associazione **CIM \_ ActionSequence** che vi fa riferimento nel ruolo "next". Si tratta della prima azione nella sequenza.
-   Nel set di azioni di stato successivo o di disinstallazione è presente una sola azione che non dispone di un'istanza dell'associazione **CIM \_ ActionSequence** che vi fa riferimento nel ruolo "precedente". Si tratta dell'ultima azione nella sequenza.
-   Tutte le altre azioni all'interno del set di azioni next-state e uninstall devono partecipare a due istanze dell'associazione **CIM \_ ActionSequence,** una in un ruolo "prior" e una nel ruolo "next".

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe CIM \_ ActionSequence** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ActionSequence** ha queste proprietà.

<dl> <dt>

**Avanti**
</dt> <dd> <dl> <dt>

Tipo di dati: **Azione CIM \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento all'azione successiva.

</dd> <dt>

**Precedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Azione CIM \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento all'azione precedente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le [**classi action CIM \_**](cim-action.md) che partecipano a questa associazione devono avere lo stesso valore per la proprietà **Direction.**

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

