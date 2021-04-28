---
description: 'Metodo ID3DX10Mesh::Optimize: genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.'
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: Metodo ID3DX10Mesh::Optimize (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f530995a2388d3ec2627ac5ce128271ed085a779
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108049"
---
# <a name="id3dx10meshoptimize-method"></a>Metodo ID3DX10Mesh::Optimize

Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Specifica il tipo di ottimizzazione da eseguire. Questo parametro può essere impostato su una combinazione di uno o più flag di D3DXMESHOPT e D3DXMESH (ad eccezione di D3DXMESH \_ 32BIT, D3DXMESH \_ IB \_ WRITEONLY e D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pFaceRemap* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Matrice di UINT, uno per viso, che identifica il viso della mesh originale che corrisponde a ogni viso nella mesh ottimizzata. Se il valore fornito per questo argomento è **NULL,** i dati di modifica del mapping dei visi non vengono restituiti.

</dd> <dt>

*ppVertexRemap* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Indirizzo di un puntatore a [**un'interfaccia ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)che contiene un valore DWORD per ogni vertice che specifica il mapping dei nuovi vertici ai vertici vecchi. Questo nuovo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Questo metodo genera una nuova mesh. Prima di eseguire Optimize, un'applicazione deve generare un buffer di adiacenza chiamando [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md). Il buffer di adienze contiene dati di adizia, ad esempio un elenco di bordi e le facce adiacenti l'una all'altra.

Questo metodo è molto simile al metodo [**ID3DX10Mesh::CloneMesh,**](id3dx10mesh-clonemesh.md) ad eccezione del fatto che può eseguire l'ottimizzazione durante la generazione del nuovo clone della mesh. La mesh di output eredita tutti i parametri di creazione della mesh di input.

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

 

 
