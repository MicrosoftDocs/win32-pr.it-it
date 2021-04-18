---
description: Recupera le opzioni di mesh abilitate per questa mesh al momento della creazione.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'Metodo ID3DXBaseMesh:: GetOptions (D3DX9Mesh. h)'
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
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323219"
---
# <a name="id3dxbasemeshgetoptions-method"></a>Metodo ID3DXBaseMesh:: GetOptions

Recupera le opzioni di mesh abilitate per questa mesh al momento della creazione.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetOptions();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Restituisce una combinazione di uno o più dei flag seguenti, che indica le opzioni abilitate per la mesh al momento della creazione.



| Valore                   | Descrizione                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXMESH a \_ 32 bit         | Usare gli indici a 32 bit.                                                                                                                                                                              |
| \_DONOTCLIP D3DXMESH     | Usare il \_ flag di utilizzo di DONOTCLIP D3DUSAGE per i buffer di Vertex e index.                                                                                                                             |
| D3DXMESH \_ dinamico       | Equivale a specificare D3DXMESH \_ VB \_ Dynamic e D3DXMESH \_ IB \_ Dynamic.                                                                                                                   |
| \_RTPATCHES D3DXMESH     | Usare il \_ flag di utilizzo di RTPATCHES D3DUSAGE per i buffer di Vertex e index.                                                                                                                             |
| \_NPATCHES D3DXMESH      | Se si specifica questo flag, il vertice e il buffer dell'indice della mesh verranno creati con il \_ flag D3DUSAGE NPATCHES. Questa operazione è obbligatoria se è necessario eseguire il rendering dell'oggetto mesh usando la funzionalità di miglioramento della patch N. |
| D3DXMESH \_ gestito       | Equivale a specificare sia \_ gestito D3DXMESH VB \_ che D3DXMESH \_ IB \_ gestito.                                                                                                                   |
| \_Punti D3DXMESH        | Usare il \_ flag di utilizzo dei punti di D3DUSAGE per i buffer dei vertici e degli indici.                                                                                                                                |
| D3DXMESH \_ IB \_ dinamico   | Usare il \_ flag di utilizzo dinamico D3DUSAGE per i buffer di indice.                                                                                                                                          |
| D3DXMESH \_ IB \_ gestito   | Usare la \_ classe di memoria gestita D3DPOOL per i buffer di indice.                                                                                                                                         |
| D3DXMESH \_ IB \_ SYSTEMMEM | Usare la \_ classe D3DPOOL SYSTEMMEM Memory per i buffer di indice.                                                                                                                                       |
| D3DXMESH \_ IB \_ WRITEONLY | Usare il \_ flag di utilizzo di D3DUSAGE WRITEONLY per i buffer di indice.                                                                                                                                        |
| \_SYSTEMMEM D3DXMESH     | Equivale a specificare sia D3DXMESH \_ VB \_ SYSTEMMEM che D3DXMESH \_ IB \_ SYSTEMMEM.                                                                                                               |
| D3DXMESH \_ VB \_ dinamico   | Usare il \_ flag di utilizzo dinamico D3DUSAGE per i buffer dei vertici.                                                                                                                                         |
| D3DXMESH \_ VB \_ gestito   | Usare la \_ classe di memoria gestita D3DPOOL per i buffer dei vertici.                                                                                                                                        |
| D3DXMESH \_ VB \_ SYSTEMMEM | Usare la \_ classe D3DPOOL SYSTEMMEM Memory per i buffer dei vertici.                                                                                                                                      |
| D3DXMESH \_ VB \_ WRITEONLY | Usare il \_ flag di utilizzo di D3DUSAGE WRITEONLY per i buffer dei vertici.                                                                                                                                       |
| \_WRITEONLY D3DXMESH     | Equivale a specificare sia D3DXMESH \_ VB \_ WRITEONLY che D3DXMESH \_ IB \_ WRITEONLY.                                                                                                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
