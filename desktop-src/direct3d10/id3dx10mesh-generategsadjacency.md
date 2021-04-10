---
description: Aggiunge i dati di adiacenza al buffer di indice della mesh. Quando la mesh deve essere inviata a un geometry shader che accetta i dati di adiacenza, è necessario che il buffer di indice della mesh contenga i dati adiacenza.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'Metodo ID3DX10Mesh:: GenerateGSAdjacency (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058642"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a>Metodo ID3DX10Mesh:: GenerateGSAdjacency

Aggiunge i dati di adiacenza al buffer di indice della mesh. Quando la mesh deve essere inviata a un geometry shader che accetta i dati di adiacenza, è necessario che il buffer di indice della mesh contenga i dati adiacenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




