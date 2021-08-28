---
description: L'associazione CIM JobDestinationJobs descrive dove viene inviato un processo per l'elaborazione, ovvero a \_ quale destinazione del processo.
ms.assetid: 6f732d34-2284-4909-a966-6b4066780cb0
ms.tgt_platform: multiple
title: CIM_JobDestinationJobs classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestinationJobs
- CIM_JobDestinationJobs.Dependent
- CIM_JobDestinationJobs.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5947ac9a8539227f27dbea62aeebcfbc07b14a7626e25234e3a39ee3267d81c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438431"
---
# <a name="cim_jobdestinationjobs-class"></a>Classe CIM \_ JobDestinationJobs

**L'associazione CIM \_ JobDestinationJobs** descrive dove viene inviato un processo per l'elaborazione, ovvero a quale destinazione del processo.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8D079BEE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestinationJobs : CIM_Dependency
{
  CIM_Job            REF Dependent;
  CIM_JobDestination REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ JobDestinationJobs** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ JobDestinationJobs** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ JobDestination**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Processo [**\_ CIMDestination che descrive**](cim-jobdestination.md) la destinazione del processo, possibilmente una coda.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **processo CIM \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Processo [**CIM \_ che**](cim-job.md) descrive il processo presente nella coda/destinazione del processo.

</dd> </dl>

## <a name="remarks"></a>Commenti

**CIM \_ JobDestinationJobs** deriva dalla dipendenza [**CIM. \_**](cim-dependency.md)

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

 

