---
description: La classe CIM ApplicationSystemSoftwareFeature rappresenta un'associazione che identifica le \_ funzionalità software che costituiscono un particolare sistema di applicazioni. Le funzionalità software possono essere incluse in prodotti diversi.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: CIM_ApplicationSystemSoftwareFeature classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d751a4564e8ed7357abd9dae5b4773e7180c66a5d0a89781a40d672715e69b11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322571"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a>Classe \_ CIM ApplicationSystemSoftwareFeature

La **classe CIM \_ ApplicationSystemSoftwareFeature rappresenta** un'associazione che identifica le funzionalità software che costituiscono un particolare sistema di applicazioni. Le funzionalità software possono essere incluse in prodotti diversi.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ ApplicationSystemSoftwareFeature** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ApplicationSystemSoftwareFeature** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ApplicationSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Oggetto [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) che contiene il sistema padre nell'associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Oggetto [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) che contiene l'elemento figlio che è un componente di un sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ ApplicationSystemSoftwareFeature** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> </dl>

 

