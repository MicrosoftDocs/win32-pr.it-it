---
description: La \_ classe CIM CompatibleProduct rappresenta un'associazione tra i prodotti che indica se due prodotti a cui viene fatto riferimento sono interoperativi, ad esempio se possono essere installati insieme o se uno può essere il contenitore fisico per l'altro e così via.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: Classe CIM_CompatibleProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94969b1f2e45a27e402e132a0b9593de413a653b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877982"
---
# <a name="cim_compatibleproduct-class"></a>CIM \_ CompatibleProduct (classe)

La classe **CIM \_ CompatibleProduct** rappresenta un'associazione tra i prodotti che indica se due prodotti a cui viene fatto riferimento sono interoperativi, ad esempio se possono essere installati insieme o se uno può essere il contenitore fisico per l'altro e così via.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a>Members

La classe **CIM \_ CompatibleProduct** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ CompatibleProduct** dispone di queste proprietà.

<dl> <dt>

**CompatibilityDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che definisce la modalità di interoperabilità e compatibilità dei due prodotti a cui viene fatto riferimento e se sono presenti limitazioni di compatibilità.

</dd> <dt>

**CompatibleProduct**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ prodotto CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al prodotto compatibile.

</dd> <dt>

**Prodotto**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ prodotto CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al prodotto per il quale sono definite offerte compatibili.

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



 

 




