---
description: La \_ classe CIM LogicalIdentity è un'associazione astratta e generica che indica che due elementi logici rappresentano aspetti diversi della stessa entità sottostante.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: Classe CIM_LogicalIdentity (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965999"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a>Classe CIM_LogicalIdentity (provider WMI CIMWin32)

La classe **CIM \_ LogicalIdentity** è un'associazione astratta e generica che indica che due elementi logici rappresentano aspetti diversi della stessa entità sottostante. L'associazione trasmette ciò che può essere definito con ereditarietà multipla ed è limitato agli aspetti logici di un elemento di sistema gestito. Nella maggior parte degli scenari la relazione di identità è determinata dall'equivalenza delle chiavi o da altre proprietà di identificazione degli elementi correlati.

L'associazione deve essere utilizzata solo in scenari ben noti, consentendo una definizione e un chiarimento più concreti nelle sottoclassi. Uno scenario in cui la relazione è ragionevole, ad esempio, rappresenta un dispositivo che è sia un'entità bus che un'entità funzionale, in cui il dispositivo è un'entità USB (bus) e una tastiera (funzionale).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Members

La classe **CIM \_ LogicalIdentity** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ LogicalIdentity** dispone di queste proprietà.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ LogicalElement CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un aspetto alternativo dell'entità di sistema.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ LogicalElement CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un aspetto dell'elemento logico.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per le classi derivate da **CIM \_ LogicalIdentity**, vedere [Win32 Classes](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




