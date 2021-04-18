---
description: Prototipo di funzione usato da D3DXComputeIMTFromSignal per descrivere un segnale definito dall'utente nello spazio u, v della mesh di input. La funzione valuta un segnale procedurale della dimensione uSignalDimension alla coordinata u, v specificata.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303676"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Prototipo di funzione usato da [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) per descrivere un segnale definito dall'utente nello spazio u, v della mesh di input. La funzione valuta un segnale procedurale della dimensione uSignalDimension alla coordinata u, v specificata.

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

\[in un \] puntatore UV a un vettore che contiene la coordinata di trama del vertice.

\[in \] uPrimitiveId: Indice del triangolo di input sulla mesh per cui deve essere calcolato il segnale.

\[in \] uSignalDimension: numero di float da archiviare nella matrice di dati del segnale (pfSignalOut).

\[in \] pUserData-il puntatore pUserData passato a [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).

\[out \] pfSignalOut: matrice di float, che contiene i dati del segnale.

## <a name="return-value"></a>Valore restituito

Questa funzione deve essere implementata per restituire S \_ OK.

## <a name="remarks"></a>Commenti

Assicurarsi di specificare la convenzione di chiamata per i [**tipi di dati di Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback. In caso contrario, è possibile che si verifichino overflow dello stack.



|                |             |
|----------------|-------------|
| Intestazione         | d3dx9mesh. h |
| Libreria di importazione | d3dx9. lib   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di callback](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
