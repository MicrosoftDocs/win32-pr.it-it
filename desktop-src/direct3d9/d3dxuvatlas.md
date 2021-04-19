---
description: Definisce le opzioni per l'esecuzione di calcoli della distanza geodetica, quando si adatta una trama a una superficie curva. Usare questo flag per scegliere tra i calcoli di alta qualità rispetto a quelli veloci durante il calcolo di un Atlante di trama.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Enumerazione D3DXUVATLAS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322470"
---
# <a name="d3dxuvatlas-enumeration"></a>Enumerazione D3DXUVATLAS

Definisce le opzioni per l'esecuzione di calcoli della distanza geodetica, quando si adatta una trama a una superficie curva. Usare questo flag per scegliere tra i calcoli di alta qualità rispetto a quelli veloci durante il calcolo di un Atlante di trama.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**\_Impostazione predefinita D3DXUVATLAS**
</dt> <dd>

Ai mesh con più di 25K visi sarà applicato il metodo di distanza geodasic veloce, mentre i mesh con meno di 25K visi avranno a disposizione il metodo di distanza geodetica di qualità superiore.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ geodetica \_ veloce**
</dt> <dd>

USA approssimazioni per migliorare la velocità di creazione dei grafici a scapito dell'estensione aggiuntiva o di più grafici restituiti per la mesh.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**\_Qualità geodetica D3DXUVATLAS \_**
</dt> <dd>

Fornisce grafici di qualità migliori, ma richiede più tempo e memoria rispetto alla velocità.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




