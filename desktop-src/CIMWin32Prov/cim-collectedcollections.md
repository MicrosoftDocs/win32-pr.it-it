---
description: La classe CIM CollectedCollections è un'associazione di aggregazione che rappresenta una raccolta di elementi del sistema \_ gestito (MSE) contenuti in una raccolta di mse.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: CIM_CollectedCollections classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cecac67d96aba6b8ad8c5937f098eaef312af89b80c28febaa8073c5f7be26f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322291"
---
# <a name="cim_collectedcollections-class"></a>Classe CIM \_ CollectedCollections

La **classe CIM \_ CollectedCollections** è un'associazione di aggregazione che rappresenta una raccolta di elementi del sistema gestito (MSE) contenuti in una raccolta di mse.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a>Members

La **classe CIM \_ CollectedCollections** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ CollectedCollections** ha queste proprietà.

<dl> <dt>

**Raccolta**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'elemento padre o di "livello superiore" nell'aggregazione.

</dd> <dt>

**CollectionInCollection**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'insieme **"collected".**

</dd> </dl>

## <a name="remarks"></a>Commenti

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



 

 




