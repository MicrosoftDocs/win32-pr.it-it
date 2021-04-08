---
description: La \_ classe CIM BootServiceAccessBySAP associa un servizio di avvio e i relativi punti di accesso.
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: Classe CIM_BootServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootServiceAccessBySAP
- CIM_BootServiceAccessBySAP.Dependent
- CIM_BootServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90548be52defbcf3419d6c7defc21395da5cfbfe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748618"
---
# <a name="cim_bootserviceaccessbysap-class"></a>CIM \_ BootServiceAccessBySAP (classe)

La classe **CIM \_ BootServiceAccessBySAP** associa un servizio di avvio e i relativi punti di accesso.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{6EDF1DD2-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_BootSAP     REF Dependent;
  CIM_BootService REF Antecedent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ BootServiceAccessBySAP** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ BootServiceAccessBySAP** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ BOOTSERVICE**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ BOOTSERVICE CIM**](cim-bootservice.md) che descrive il servizio di avvio.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ BootSAP**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Un [**\_ BootSAP CIM**](cim-bootsap.md) che descrive un punto di accesso per il servizio di avvio.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ BootServiceAccessBySAP** è derivata da [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md).

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

 

