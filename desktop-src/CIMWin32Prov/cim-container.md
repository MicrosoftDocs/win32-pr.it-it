---
description: La classe CIM \_ Container rappresenta un'associazione tra un elemento contenuto e un elemento fisico contenitore. Un oggetto contenitore deve essere un pacchetto fisico.
ms.assetid: 9b119163-3c56-44e2-ba66-d8add3c375fa
ms.tgt_platform: multiple
title: CIM_Container classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Container
- CIM_Container.PartComponent
- CIM_Container.GroupComponent
- CIM_Container.LocationWithinContainer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c0e4177fd70a79b1029d14ddb866eb533ce4c4e6183d88c61873bb9f8072a261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700761"
---
# <a name="cim_container-class"></a>Classe \_ contenitore CIM

La **classe CIM \_ Container** rappresenta un'associazione tra un elemento contenuto e un elemento fisico contenitore. Un oggetto contenitore deve essere un pacchetto fisico.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B6F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Container : CIM_Component
{
  CIM_PhysicalElement REF PartComponent;
  CIM_PhysicalPackage REF GroupComponent;
  string                  LocationWithinContainer;
};
```

## <a name="members"></a>Members

La **classe CIM \_ Container** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ Container** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**CiM \_ PhysicalPackage che**](cim-physicalpackage.md) rappresenta il pacchetto fisico che contiene altri elementi fisici, inclusi altri pacchetti.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico. In questa proprietà è possibile registrare informazioni relative agli elementi stazionari nel contenitore ,ad esempio "second drive bay from the top", angolazioni, altitudini e altri dati. Questa stringa può integrare o essere usata al posto della creazione di un'istanza [**dell'oggetto \_ Location CIM.**](cim-location.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Elemento [**CIM \_ PhysicalElement**](cim-physicalelement.md) che descrive l'elemento fisico contenuto nel pacchetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per altre informazioni sulle classi derivate dal **contenitore CIM, \_** vedere [Classi Win32](win32-provider.md).

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

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

