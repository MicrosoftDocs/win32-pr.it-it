---
description: La \_ classe CIM SoftwareFeatureSAPImplementation rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato nel software.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877285"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a>CIM \_ SoftwareFeatureSAPImplementation (classe)

La classe **CIM \_ SoftwareFeatureSAPImplementation** rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato nel software. Un SAP può essere fornito da più di una funzionalità software per operare insieme tra loro. Inoltre, una funzionalità software può fornire più di un SAP. Quando molte funzionalità software sono associate a un singolo SAP, si presuppone che gli elementi funzionino insieme per fornire il punto di accesso. Se sono presenti implementazioni diverse di un SAP, ogni implementazione comporterebbe la creazione di istanze singole dell'oggetto SAP. Le singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ SoftwareFeatureSAPImplementation** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ SoftwareFeatureSAPImplementation** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) che descrive la funzionalità del software precedente.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ serviceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive il punto di accesso al servizio dipendente.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ SoftwareFeatureSAPImplementation** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

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

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 

