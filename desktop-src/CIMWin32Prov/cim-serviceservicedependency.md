---
description: La \_ classe CIM ServiceServiceDependency rappresenta un'associazione tra due servizi.
ms.assetid: 0fb43fb3-2c05-4762-b339-2dcc090ed38d
ms.tgt_platform: multiple
title: Classe CIM_ServiceServiceDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceServiceDependency
- CIM_ServiceServiceDependency.Dependent
- CIM_ServiceServiceDependency.Antecedent
- CIM_ServiceServiceDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fdc8ea1a3324395e5230ca6d47487b61c8c02ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304765"
---
# <a name="cim_serviceservicedependency-class"></a>CIM \_ ServiceServiceDependency (classe)

La classe **CIM \_ ServiceServiceDependency** rappresenta un'associazione tra due servizi. Il servizio associato deve essere presente, deve essere stato completato oppure deve essere assente affinché l'altro servizio funzioni. È ad esempio possibile che i servizi di avvio dipendano da servizi BIOS, dischi e inizializzazione sottostanti. Per i servizi di inizializzazione, il servizio di avvio dipende dal completamento dei servizi di inizializzazione. Per i servizi disco, i servizi di avvio possono effettivamente utilizzare i succhi di questo servizio. Questa dipendenza di utilizzo è modellata sull'associazione [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) .

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8502C53B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ServiceServiceDependency : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_Service REF Antecedent;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ServiceServiceDependency** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ServiceServiceDependency** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ servizio CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

[**\_ Servizio CIM**](cim-service.md) che descrive il servizio richiesto.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ servizio CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

[**\_ Servizio CIM**](cim-service.md) che descrive il servizio che dipende da un servizio sottostante.

</dd> <dt>

**TypeOfDependency**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Natura della dipendenza da servizio a servizio. Questa proprietà indica che il servizio associato deve essere stato completato, deve essere avviato o non deve essere avviato per il funzionamento del servizio.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>Il **servizio deve essere stato completato** (2)


</dt> <dd>

Il servizio deve essere stato completato.

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>Il **servizio deve essere avviato** (3)


</dt> <dd>

Il servizio deve essere avviato.

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>Il **servizio non deve essere avviato** (4)


</dt> <dd>

Il servizio non deve essere avviato.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per le classi WMI derivate da **CIM \_ ServiceServiceDependency**, vedere [Win32 Classes](win32-provider.md).

La classe **CIM \_ ServiceServiceDependency** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

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

 

