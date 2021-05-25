---
description: Prototipo di funzione usato da D3DXComputeIMTFromSignal per descrivere un segnale definito dall'utente nello spazio u,v di una mesh di input. La funzione valuta un segnale procedurale della dimensione uSignalDimension in corrispondenza della coordinata u,v specificata.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342836"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Prototipo di funzione [**usato da D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) per descrivere un segnale definito dall'utente nello spazio u,v di una mesh di input. La funzione valuta un segnale procedurale della dimensione uSignalDimension in corrispondenza della coordinata u,v specificata.

## <a name="syntax"></a>Sintassi


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a>Parametri

\[in \] uv : puntatore a un vettore che contiene la coordinata della trama dei vertici.

\[in uPrimitiveId: indice del triangolo di input nella mesh per cui deve essere calcolato \] il segnale.

\[in \] uSignalDimension: numero di valori float da archiviare nella matrice di dati del segnale (pfSignalOut).

\[in \] pUserData: puntatore pUserData passato a [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).

\[out \] pfSignalOut: matrice di valori float che contiene i dati del segnale.

## <a name="return-value"></a>Valore restituito

Questa funzione deve essere implementata per restituire S \_ OK.

## <a name="remarks"></a>Commenti

Assicurarsi di specificare la convenzione [**di chiamata dei tipi di dati Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback. In caso contrario, possono verificarsi overflow dello stack.



| Requisito               | Valore            |
|----------------|-------------|
| Intestazione         | d3dx9mesh.h |
| Libreria di importazione | d3dx9.lib   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di callback](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
