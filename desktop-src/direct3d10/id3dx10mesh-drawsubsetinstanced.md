---
description: Creare diverse istanze dello stesso subset di una mesh.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: Metodo ID3DX10Mesh::D rawSubsetInstanced (D3DX10. h)
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
ms.openlocfilehash: 314f85d896be629254def560e55ce6a05bfe1fbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323158"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>ID3DX10Mesh::D Metodo rawSubsetInstanced

Creare diverse istanze dello stesso subset di una mesh.

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

*AttribId* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Specifica il subset della mesh da creare. Questo valore viene utilizzato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi. Vedere la sezione Osservazioni.

</dd> <dt>

*InstanceCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di istanze di di cui eseguire il rendering.

</dd> <dt>

*StartInstanceLocation* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Istanza da cui iniziare il recupero in ogni buffer contrassegnato come dati dell'istanza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Una mesh contiene una tabella degli attributi. La tabella degli attributi può dividere una mesh in subset, in cui ogni subset viene identificato con un ID attributo. Ad esempio, una mesh con 200 visi, divisa in tre subset, potrebbe avere una tabella di attributi simile alla seguente:



|            |                 |
|------------|-----------------|
| AttribID 0 | Visi 0 ~ 50    |
| AttribID 1 | Visi 51 ~ 125  |
| AttribID 2 | Visi 126 ~ 200 |



 

La creazione di istanze può estendere le prestazioni riutilizzando la stessa geometria per creare più oggetti in una scena. Un esempio di istanza può consistere nel creare lo stesso oggetto con posizioni e colori diversi. L'indicizzazione richiede più buffer vertex: almeno uno per i dati per vertice e un secondo buffer per i dati per istanza.

Il disegno di istanze con DrawSubsetInstanced è molto simile al processo usato con [**ID3D10Device::D rawindexedinstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) descritto nell' [esempio di istanze](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx). La differenza principale quando si usa DrawSubsetInstanced è che i buffer dei vertici e degli indici devono essere estratti dall'oggetto [**interfaccia ID3DX10Mesh**](id3dx10mesh.md) prima di poter combinare i dati di istanza.

Il codice seguente illustra l'estrazione dei buffer di Vertex e index dall'oggetto mesh.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



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

 

 
