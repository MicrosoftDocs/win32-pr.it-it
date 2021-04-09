---
description: La \_ classe CIM ClusterServiceAccessBySAP rappresenta la relazione tra un servizio di clustering e i relativi punti di accesso.
ms.assetid: b1e03ef1-909c-4836-a75f-c8d88a4d0087
ms.tgt_platform: multiple
title: Classe CIM_ClusterServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusterServiceAccessBySAP
- CIM_ClusterServiceAccessBySAP.Dependent
- CIM_ClusterServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b6e6f0df20f182be392de3fbb0cb13068cbeffc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966206"
---
# <a name="cim_clusterserviceaccessbysap-class"></a>CIM \_ ClusterServiceAccessBySAP (classe)

La classe **CIM \_ ClusterServiceAccessBySAP** rappresenta la relazione tra un servizio di clustering e i relativi punti di accesso.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{88F073D8-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ClusterServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_ClusteringSAP     REF Dependent;
  CIM_ClusteringService REF Antecedent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ClusterServiceAccessBySAP** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ClusterServiceAccessBySAP** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ClusteringService**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ ClusteringService CIM**](cim-clusteringservice.md) che descrive il servizio di clustering.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ClusteringSAP**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Un [**\_ ClusteringSAP CIM**](cim-clusteringsap.md) che descrive un punto di accesso per il servizio di clustering.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ ClusterServiceAccessBySAP** è derivata da [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md).

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

[**\_SERVICEACCESSBYSAP CIM**](cim-serviceaccessbysap.md)
</dt> </dl>

 

