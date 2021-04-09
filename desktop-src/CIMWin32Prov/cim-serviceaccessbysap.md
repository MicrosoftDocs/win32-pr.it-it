---
description: La \_ classe di associazione CIM ServiceAccessBySAP rappresenta i punti di accesso per un servizio. Ad esempio, è possibile accedere a una stampante mediante i punti di accesso (SAP) di NetWare, Macintosh o Windows, che sono potenzialmente ospitati in sistemi diversi.
ms.assetid: 68311a56-b034-4a30-a885-74a745a738d8
ms.tgt_platform: multiple
title: Classe CIM_ServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessBySAP
- CIM_ServiceAccessBySAP.Dependent
- CIM_ServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e34b2af50a6475461ae4d39d156d26143fcb75f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966094"
---
# <a name="cim_serviceaccessbysap-class"></a>CIM \_ ServiceAccessBySAP (classe)

La classe di associazione **CIM \_ ServiceAccessBySAP** rappresenta i punti di accesso per un servizio. Ad esempio, è possibile accedere a una stampante mediante i punti di accesso (SAP) di NetWare, Macintosh o Windows, che sono potenzialmente ospitati in sistemi diversi.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{714C00BA-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessBySAP : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_Service            REF Antecedent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ServiceAccessBySAP** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ServiceAccessBySAP** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ servizio CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

[**\_ Servizio CIM**](cim-service.md) che descrive il servizio.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ serviceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive un punto di accesso per un servizio. I punti di accesso dipendono da questa relazione poiché non dispongono di funzioni senza un servizio corrispondente.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ ServiceAccessBySAP** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

WMI non implementa questa classe. Per le classi WMI derivate da **CIM \_ ServiceAccessBySAP**, vedere [Win32 Classes](win32-provider.md).

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

 

