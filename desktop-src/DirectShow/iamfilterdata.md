---
description: Nota Questa interfaccia è stata deprecata.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interfaccia IAMFilterData (Fil \_ Data. h)
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
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326816"
---
# <a name="iamfilterdata-interface"></a>Interfaccia IAMFilterData

> [!Note]  
> Questa interfaccia è stata deprecata. Le nuove applicazioni devono invece usare l'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

 

L' `IAMFilterData` interfaccia converte le informazioni di filtro in dati binari compressi, che possono essere archiviati nel registro di sistema. L'oggetto filtro Mapper espone questa interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IAMFilterData** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMFilterData** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMFilterData** dispone di questi metodi.



| Metodo                                                     | Descrizione                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**CreateFilterData**](iamfilterdata-createfilterdata.md) | Crea dati di registro binari per un filtro.<br/>     |
| [**ParseFilterData**](iamfilterdata-parsefilterdata.md)   | Decomprime i dati del registro di sistema binario per un filtro.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> L'intestazione fil \_ Data. h si trova nella directory degli [esempi del Mapper](mapper-sample.md) nel Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Fil \_ Data. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce deprecate](deprecated-interfaces.md)
</dt> </dl>

 

 
