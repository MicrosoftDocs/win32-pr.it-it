---
description: Rappresenta un'associazione tra due punti di accesso al servizio (SAP), in cui un SAP dipende dall'altro per utilizzare o connettersi a un servizio.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: CIM_SAPSAPDependency classe (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae8b1e45d1685204b15cf359f36cfced321fb75c099b7be76e0ece2ce3f836de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980861"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a>CIM_SAPSAPDependency classe (gestione Hyper-V)

Rappresenta un'associazione tra due punti di accesso al servizio (SAP), in cui un SAP dipende dall'altro per utilizzare o connettersi a un servizio. Ad esempio, per stampare su una stampante di rete, i punti di accesso alla stampa locale devono utilizzare i punti di accesso di rete sottostanti per inviare la richiesta di stampa.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ SAPSAPDependency** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ SAPSAPDependency** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Riferimento all'oggetto SAP richiesto.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Riferimento all'oggetto SAP dipendente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> </dl>

 

