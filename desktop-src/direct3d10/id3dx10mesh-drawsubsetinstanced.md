---
description: Disegnare diverse istanze dello stesso subset di una mesh.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: Metodo ID3DX10Mesh::D rawSubsetInstanced (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 41da932b5f9445df83c0783b7788b8a7079af2acb74643ea37111d8482e8e208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990431"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>Metodo ID3DX10Mesh::D rawSubsetInstanced

Disegnare diverse istanze dello stesso subset di una mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AttribId* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Specifica il subset della mesh da disegnare. Questo valore viene usato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi. Vedere la sezione Osservazioni.

</dd> <dt>

*InstanceCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di istanze di di cui eseguire il rendering.

</dd> <dt>

*StartInstanceLocation* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Istanza da cui iniziare il recupero in ogni buffer contrassegnato come dati dell'istanza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Una mesh contiene una tabella di attributi. La tabella degli attributi può dividere una mesh in subset, in cui ogni subset viene identificato con un ID attributo. Ad esempio, una mesh con 200 visi, suddivisa in tre subset, potrebbe avere una tabella di attributi simile alla seguente:



| Subset     | Smile           |
|------------|-----------------|
| AttribID 0 | Visi 0 ~ 50    |
| AttribID 1 | Visi 51 ~ 125  |
| AttribID 2 | Visi 126 ~ 200 |



 

Le istanze possono estendere le prestazioni riutilizzando la stessa geometria per disegnare più oggetti in una scena. Un esempio di istanze può essere quello di disegnare lo stesso oggetto con posizioni e colori diversi. L'indicizzazione richiede più buffer dei vertici: almeno uno per i dati per vertice e un secondo buffer per i dati per istanza.

Il disegno di istanze con DrawSubsetInstanced è molto simile al processo usato con [**ID3D10Device::D rawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) descritto in [Esempio](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)di istanze. La differenza principale quando si usa DrawSubsetInstanced è che i buffer dei vertici e degli indici devono essere estratti dall'oggetto [**interfaccia ID3DX10Mesh**](id3dx10mesh.md) prima di poter combinare i dati di istanza.

Il codice seguente illustra l'estrazione dei buffer dei vertici e degli indici dall'oggetto mesh.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



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

 

 
