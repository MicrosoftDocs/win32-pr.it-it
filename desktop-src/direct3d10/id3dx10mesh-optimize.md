---
description: Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'Metodo ID3DX10Mesh:: Optimize (D3DX10. h)'
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
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355274"
---
# <a name="id3dx10meshoptimize-method"></a>Metodo ID3DX10Mesh:: Optimize

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

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Specifica il tipo di ottimizzazione da eseguire. Questo parametro può essere impostato su una combinazione di uno o più flag di D3DXMESHOPT e D3DXMESH (eccetto D3DXMESH a \_ 32 bit, D3DXMESH \_ IB \_ WRITEONLY e D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pFaceRemap* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Matrice di UINTs, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella mesh ottimizzata. Se il valore fornito per questo argomento è **null**, non vengono restituiti i dati di riassociazione della faccia.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Indirizzo di un puntatore a un' [**interfaccia ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti. Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Questo metodo genera una nuova mesh. Prima di eseguire l'ottimizzazione, un'applicazione deve generare un buffer adiacenza chiamando [**ID3DX10Mesh:: GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md). Il buffer adiacenza contiene dati adiacenza, ad esempio un elenco di bordi e i visi adiacenti.

Questo metodo è molto simile al metodo [**ID3DX10Mesh:: CloneMesh**](id3dx10mesh-clonemesh.md) , ad eccezione del fatto che può eseguire l'ottimizzazione durante la generazione del nuovo clone della mesh. La mesh di output eredita tutti i parametri di creazione della mesh di input.

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

 

 
