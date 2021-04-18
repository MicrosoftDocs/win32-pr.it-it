---
description: La \_ classe CIM ProductSupport rappresenta un'associazione tra il prodotto e il supporto dell'accesso che comunica come si ottiene il supporto per il prodotto.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: Classe CIM_ProductSupport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304587"
---
# <a name="cim_productsupport-class"></a>CIM \_ ProductSupport (classe)

La classe **CIM \_ ProductSupport** rappresenta un'associazione tra il prodotto e il supporto dell'accesso che comunica come si ottiene il supporto per il prodotto. Sono disponibili vari tipi di supporto per un prodotto; lo stesso oggetto di supporto può fornire assistenza per più prodotti.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ProductSupport** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ProductSupport** dispone di queste proprietà.

<dl> <dt>

**Prodotto**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ prodotto CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al prodotto.

</dd> <dt>

**Supporto**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SupportAccess**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al supporto tecnico.

</dd> </dl>

## <a name="remarks"></a>Commenti

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



 

 




