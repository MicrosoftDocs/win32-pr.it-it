---
description: 'Metodo ID3DX10Mesh::GenerateAdjacencyAndPointReps: genera un elenco di bordi di mesh, nonché un elenco di visi che condividono ogni bordo.'
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: Metodo ID3DX10Mesh::GenerateAdjacencyAndPointReps (D3DX10.h)
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
ms.openlocfilehash: 55198648be8952f975313dad3019063917eddf4d38f0a7d636039d5802f08e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566941"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>Metodo ID3DX10Mesh::GenerateAdjacencyAndPointReps

Generare un elenco di bordi di mesh, nonché un elenco di visi che condividono ogni bordo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Epsilon* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Specifica che i vertici che differiscono per posizione minore di epsilon devono essere considerati coincidenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Dopo che un'applicazione genera informazioni di adizia per una mesh, i dati della mesh possono essere ottimizzati per migliorare le prestazioni di disegno.

L'ordine delle voci nel buffer di adienze è determinato dall'ordine degli indici dei vertici nel index buffer. Il triangolo adiacente 0 corrisponde sempre al bordo tra gli indici degli angoli 0 e 1. Il triangolo adiacente 1 corrisponde sempre al bordo tra gli indici degli angoli 1 e 2, mentre il triangolo adiacente 2 corrisponde al bordo tra gli indici degli angoli 2 e 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
