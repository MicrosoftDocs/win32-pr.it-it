---
description: Proietta una funzione rappresentata in una mappa cubo in armoniche sferiche.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: Funzione D3DX10SHProjectCubeMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322766"
---
# <a name="d3dx10shprojectcubemap-function"></a>D3DX10SHProjectCubeMap (funzione)

Proietta una funzione rappresentata in una mappa cubo in armoniche sferiche.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ordine* 
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione SH, genera l'ordine ^ 2 coefs, Degree è Order-1.

</dd> <dt>

*pCubeMap* 
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Mappa cubi che verrà proiettato in armoniche sferiche. Vedere [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).

</dd> <dt>

*pROut* 
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Output SH Vector per rosso.

</dd> <dt>

*pGOut* 
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Output SH Vector per verde.

</dd> <dt>

*pBOut* 
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Output SH Vector per Blue.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
