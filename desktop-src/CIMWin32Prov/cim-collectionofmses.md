---
description: L' \_ oggetto CIM CollectionOfMSEs consente il raggruppamento di oggetti CIM \_ ManagedSystemElement allo scopo di associare le impostazioni e le configurazioni. È astratto per richiedere ulteriori definizioni e perfezionamento semantico nelle sottoclassi.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: Classe CIM_CollectionOfMSEs (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127110"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>Classe CIM_CollectionOfMSEs (provider WMI CIMWin32)

L'oggetto **CIM \_ CollectionOfMSEs** consente il raggruppamento di oggetti [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) allo scopo di associare le impostazioni e le configurazioni. È astratto per richiedere ulteriori definizioni e perfezionamento semantico nelle sottoclassi.

L' **oggetto \_ CollectionOfMSEs CIM** non porta informazioni sullo stato o sullo stato, ma rappresenta solo un raggruppamento di elementi. Per questo motivo, non è corretto per i gruppi di sottoclassi con stato/stato da **CIM \_ CollectionOfMSEs**, ad esempio [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (che è correttamente sottoclassato da [**CIM \_ LogicalElement**](cim-logicalelement.md)). Le raccolte in genere aggregano gli oggetti ' like ' e rappresentano un'ottimizzazione. Senza raccolte, è necessario definire singole associazioni CIM [**\_ ElementSetting**](cim-elementsetting.md) e [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) per collegare le impostazioni e gli oggetti di configurazione a singoli [**CIM \_ ManagedSystemElements**](cim-managedsystemelement.md). È possibile che si verifichino molte duplicazioni nell'assegnazione della stessa impostazione a più oggetti. Inoltre, l'utilizzo dell'oggetto Collection consente di determinare che l'impostazione e le associazioni di configurazione sono effettivamente le stesse per i membri della raccolta. Queste informazioni verrebbero altrimenti ottenute definendo la raccolta in modo proprietario, quindi eseguendo una query sulle associazioni **CIM \_ ElementSetting** e **CIM \_ ElementConfiguration** per determinare se il set di raccolta è completamente coperto.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a>Members

La classe **CIM \_ CollectionOfMSEs** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ CollectionOfMSEs** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione testuale dell'oggetto CollectionOfMSEs.

</dd> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificazione dell'oggetto raccolta. Quando è sottoclassata, è possibile eseguire l'override della proprietà CollectionID in modo che sia una proprietà chiave.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto CollectionOfMSEs.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Vedere [le classi Win32](win32-provider.md) per le classi WMI derivate da **CIM \_ CollectionOfMSEs**.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




