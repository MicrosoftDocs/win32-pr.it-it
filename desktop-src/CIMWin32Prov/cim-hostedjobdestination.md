---
description: La classe CIM HostedJobDestination rappresenta un'associazione tra una destinazione del processo e \_ il sistema in cui risiede. Un sistema può ospitare molte code di processi. Le destinazioni dei processi rimandano al sistema di hosting.
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: CIM_HostedJobDestination classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 072e911471fe6220a7135f45787f5ea8bf9c79279212ed6215a971ff8c1d95cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923531"
---
# <a name="cim_hostedjobdestination-class"></a>Classe CIM \_ HostedJobDestination

La **classe CIM \_ HostedJobDestination** rappresenta un'associazione tra una destinazione del processo e il sistema in cui risiede. Un sistema può ospitare molte code di processi. Le destinazioni dei processi rimandano al sistema di hosting.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ HostedJobDestination** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ HostedJobDestination** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **SISTEMA CIM \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Un [**sistema CIM \_**](cim-system.md) che descrive il sistema di hosting.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ JobDestination**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Oggetto [**CIM \_ JobDestination**](cim-jobdestination.md) che descrive la destinazione del processo ospitata nel sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

**CIM \_ HostedJobDestination** deriva dalla [**dipendenza CIM. \_**](cim-dependency.md)

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

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> </dl>

 

