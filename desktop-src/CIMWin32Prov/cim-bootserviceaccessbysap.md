---
description: La classe CIM \_ BootServiceAccessBySAP associa un servizio di avvio e i relativi punti di accesso.
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: CIM_BootServiceAccessBySAP classe
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
ms.openlocfilehash: 78ea24cb3140d50552884887d66fa2607c00b51635ea38af2150295b0c516ef1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959090"
---
# <a name="cim_bootserviceaccessbysap-class"></a>Classe CIM \_ BootServiceAccessBySAP

La **classe CIM \_ BootServiceAccessBySAP** associa un servizio di avvio e i relativi punti di accesso.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe CIM \_ BootServiceAccessBySAP** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ BootServiceAccessBySAP** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ BootService**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**BootService \_ CIM**](cim-bootservice.md) che descrive il servizio di avvio.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ BootSAP**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Oggetto [**CIM \_ BootSAP**](cim-bootsap.md) che descrive un punto di accesso per il servizio di avvio.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ BootServiceAccessBySAP** è derivata da [**CIM \_ ServiceAccessBySAP.**](cim-serviceaccessbysap.md)

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md)
</dt> </dl>

 

