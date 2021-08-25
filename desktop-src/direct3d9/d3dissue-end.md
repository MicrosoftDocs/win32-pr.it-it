---
description: Questa macro crea un valore usato da Issue per terminare una query.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 0c2e7a197612b56eb5ae966da3cd4cc224edd2bd07e3fded3d0b72907f717d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987251"
---
# <a name="d3dissue_end"></a>D3DISSUE \_ END

Questa macro crea un valore usato da [**Issue per terminare**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) una query.

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Parametri





 

## <a name="remarks"></a>Commenti

Questa macro modifica lo stato della query in nonsignaled.

D3DISSUE \_ END è valido per i tipi di query seguenti.

-   D3DQUERYTYPE \_ VCACHE
-   D3DQUERYTYPE \_ ResourceManager
-   D3DQUERYTYPE \_ VERTEXSTATS
-   EVENTO D3DQUERYTYPE \_
-   OCCLUSIONE D3DQUERYTYPE \_

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DISSUE \_ BEGIN**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
