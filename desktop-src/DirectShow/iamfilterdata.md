---
description: Informazioni sull'interfaccia IAMFilterData, che converte le informazioni di filtro in dati binari imballati. Questa interfaccia è stata deprecata.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interfaccia IAMFilterData (Fil \_ data.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 9174549c93a76f94ccb7f039343a8eab5e75ece252871d11d60221df03aabe87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823601"
---
# <a name="iamfilterdata-interface"></a>Interfaccia IAMFilterData

> [!Note]  
> Questa interfaccia è stata deprecata. Le nuove applicazioni devono usare invece [**l'interfaccia IFilterMapper2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)

 

`IAMFilterData`L'interfaccia converte le informazioni di filtro in dati binari imballati, che possono essere archiviati nel Registro di sistema. L'oggetto Filter Mapper espone questa interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IAMFilterData** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMFilterData** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IAMFilterData.**



| Metodo                                                     | Descrizione                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**CreateFilterData**](iamfilterdata-createfilterdata.md) | Crea dati binari del Registro di sistema per un filtro.<br/>     |
| [**ParseFilterData**](iamfilterdata-parsefilterdata.md)   | Decomprime i dati binari del Registro di sistema per un filtro.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> L'intestazione Fil \_ data.h si trova nella directory [Mapper Sample](mapper-sample.md) in Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Fil \_ data.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce deprecate](deprecated-interfaces.md)
</dt> </dl>

 

 
