---
description: Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'Metodo ID3DX10Mesh:: GenerateAdjacencyAndPointReps (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530991"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>Metodo ID3DX10Mesh:: GenerateAdjacencyAndPointReps

Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Epsilon* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Specifica che i vertici che differiscono dalla posizione minore di Epsilon devono essere considerati coincidenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Quando un'applicazione genera informazioni adiacenza per una mesh, i dati della mesh possono essere ottimizzati per migliorare le prestazioni di disegno.

L'ordine delle voci nel buffer adiacenza è determinato dall'ordine degli indici dei vertici nel buffer dell'indice. Il triangolo adiacente 0 corrisponde sempre al bordo tra gli indici degli angoli 0 e 1. Il triangolo adiacente 1 corrisponde sempre al bordo tra gli indici degli angoli 1 e 2, mentre il triangolo adiacente 2 corrisponde al bordo tra gli indici degli angoli 2 e 0.

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

 

 
