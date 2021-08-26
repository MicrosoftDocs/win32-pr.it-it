---
description: La classe CIM \_ HostedService rappresenta un'associazione tra un servizio e il sistema in cui si trova la funzionalità.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: CIM_HostedService classe (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7e70f7dea8fe6f5be0da7d76b37cf99ba4dcc7397c09cf27b542129232212286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921601"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a>CIM_HostedService classe (provider WMI CIMWin32)

La **classe CIM \_ HostedService** rappresenta un'associazione tra un servizio e il sistema in cui si trova la funzionalità. Un sistema può ospitare molti servizi, che rimandano al sistema di hosting. Il modello non rappresenta i servizi ospitati in più sistemi.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ HostedService** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ HostedService** ha queste proprietà.

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

Tipo di dati: **servizio \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Servizio [**CIM \_**](cim-service.md) che descrive il servizio ospitato nel sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

**CIM \_ HostedService** deriva dalla [**dipendenza CIM. \_**](cim-dependency.md)

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

 

