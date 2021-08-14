---
description: La classe CIM ProductSupport rappresenta un'associazione tra il prodotto e l'accesso al supporto che indica come viene ottenuto \_ il supporto per il prodotto.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: CIM_ProductSupport classe
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
ms.openlocfilehash: a33efc39481ebe94b6aa8802d469e218d026aba34ab8da6cddf3f136b45a6d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118421448"
---
# <a name="cim_productsupport-class"></a>Classe CIM \_ ProductSupport

La **classe CIM \_ ProductSupport** rappresenta un'associazione tra il prodotto e l'accesso al supporto che indica come viene ottenuto il supporto per il prodotto. Per un prodotto sono disponibili vari tipi di supporto. lo stesso oggetto di supporto può fornire assistenza per più prodotti.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe CIM \_ ProductSupport** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ProductSupport** ha queste proprietà.

<dl> <dt>

**Prodotto**
</dt> <dd> <dl> <dt>

Tipo di dati: **PRODOTTO CIM \_**
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

Riferimento al supporto tecnico del prodotto.

</dd> </dl>

## <a name="remarks"></a>Commenti

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



 

 




