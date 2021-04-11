---
description: La \_ classe WMI dell'associazione DependentService Win32 mette in relazione due servizi di base interdipendenti.
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Classe Win32_DependentService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 047ec3411186f09f3d0e76da27158aa8ee91d4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127723"
---
# <a name="win32_dependentservice-class"></a>Win32 \_ DependentService (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ DependentService Win32** mette in relazione due servizi di base interdipendenti.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ DependentService** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ DependentService** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ BaseService**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 BaseService")
</dt> </dl>

[**\_ BaseService Win32**](win32-baseservice.md) che rappresenta il servizio di base basato sulla proprietà **dipendente** della classe.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ BaseService**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")
</dt> </dl>

[**\_ BaseService Win32**](win32-baseservice.md) che rappresenta il servizio di base che dipende dalla proprietà **precedente** di questa classe.

</dd> <dt>

**TypeOfDependency**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Natura della dipendenza da servizio a servizio. Questa proprietà indica che il servizio associato deve essere stato completato, deve essere avviato o non deve essere avviato per il funzionamento del servizio.

Questa proprietà viene ereditata da [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md).

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

La classe **Win32 \_ DependentService** è derivata da [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md).

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

[**\_SERVICESERVICEDEPENDENCY CIM**](cim-serviceservicedependency.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

