---
description: Recupera le opzioni della mesh abilitate per questa mesh al momento della creazione.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: Metodo ID3DXBaseMesh::GetOptions (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b8ed6281e1418246027a05f281ef5c01d8fbe757a8bd88d2bf6f44ca41ed1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121763"
---
# <a name="id3dxbasemeshgetoptions-method"></a>Metodo ID3DXBaseMesh::GetOptions

Recupera le opzioni della mesh abilitate per questa mesh al momento della creazione.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetOptions();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Restituisce una combinazione di uno o più dei flag seguenti, che indica le opzioni abilitate per questa mesh al momento della creazione.



| Valore                   | Descrizione                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXMESH \_ 32 BIT         | Usare indici a 32 bit.                                                                                                                                                                              |
| D3DXMESH \_ DONOTCLIP     | Usare il flag di utilizzo D3DUSAGE \_ DONOTCLIP per i buffer dei vertici e degli indici.                                                                                                                             |
| D3DXMESH \_ DYNAMIC       | Equivale a specificare sia D3DXMESH \_ VB \_ DYNAMIC che D3DXMESH \_ IB \_ DYNAMIC.                                                                                                                   |
| D3DXMESH \_ RTPATCHES     | Usare il flag di utilizzo D3DUSAGE \_ RTPATCHES per i buffer dei vertici e degli indici.                                                                                                                             |
| D3DXMESH \_ NPATCHES      | Se si specifica questo flag, il vertice e index buffer della mesh vengono creati con il flag D3DUSAGE \_ NPATCHES. Questa operazione è necessaria se è necessario eseguire il rendering dell'oggetto mesh usando il miglioramento N-Patch. |
| D3DXMESH \_ GESTITO       | Equivale a specificare sia D3DXMESH \_ VB \_ MANAGED che D3DXMESH \_ IB \_ MANAGED.                                                                                                                   |
| PUNTI D3DXMESH \_        | Usare il flag di utilizzo D3DUSAGE \_ POINTS per i buffer dei vertici e degli indici.                                                                                                                                |
| D3DXMESH \_ IB \_ DYNAMIC   | Usare il flag di utilizzo D3DUSAGE \_ DYNAMIC per i buffer di indice.                                                                                                                                          |
| D3DXMESH \_ IB \_ MANAGED   | Usare la classe di memoria gestita D3DPOOL \_ per i buffer di indice.                                                                                                                                         |
| D3DXMESH \_ IB \_ SYSTEMMEM | Usare la classe di memoria D3DPOOL \_ SYSTEMMEM per i buffer di indice.                                                                                                                                       |
| D3DXMESH \_ IB \_ WRITEONLY | Usare il flag di utilizzo D3DUSAGE \_ WRITEONLY per i buffer di indice.                                                                                                                                        |
| D3DXMESH \_ SYSTEMMEM     | Equivale a specificare sia D3DXMESH \_ VB \_ SYSTEMMEM che D3DXMESH \_ IB \_ SYSTEMMEM.                                                                                                               |
| D3DXMESH \_ VB \_ DYNAMIC   | Usare il flag di utilizzo D3DUSAGE \_ DYNAMIC per i vertex buffer.                                                                                                                                         |
| D3DXMESH \_ VB \_ GESTITO   | Usare la classe di memoria gestita D3DPOOL \_ per i vertex buffer.                                                                                                                                        |
| D3DXMESH \_ VB \_ SYSTEMMEM | Usare la classe di memoria D3DPOOL \_ SYSTEMMEM per i vertex buffer.                                                                                                                                      |
| D3DXMESH \_ VB \_ WRITEONLY | Usare il flag di utilizzo D3DUSAGE \_ WRITEONLY per i vertex buffer.                                                                                                                                       |
| D3DXMESH \_ WRITEONLY     | Equivale a specificare sia D3DXMESH \_ VB \_ WRITEONLY che D3DXMESH \_ IB \_ WRITEONLY.                                                                                                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
