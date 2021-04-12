---
description: Questa macro crea un valore utilizzato da Issue per emettere una query end.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
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
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355084"
---
# <a name="d3dissue_end"></a>\_Fine D3DISSUE

Questa macro crea un valore utilizzato da [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) per emettere una query end.

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Parametri





 

## <a name="remarks"></a>Commenti

Questa macro imposta lo stato della query su non segnalato.

D3DISSUE \_ end è valido per i tipi di query seguenti.

-   \_VCACHE D3DQUERYTYPE
-   \_RESOURCEMANAGER D3DQUERYTYPE
-   \_VERTEXSTATS D3DQUERYTYPE
-   \_Evento D3DQUERYTYPE
-   \_Occlusione D3DQUERYTYPE

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**\_Inizio D3DISSUE**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
