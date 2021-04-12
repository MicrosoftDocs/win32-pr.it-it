---
description: Tipo di funzione usato dalle funzioni di riempimento della trama.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8c9d9ef610ee10faa069841a05f43c17b0885c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225352"
---
# <a name="lpd3dxfill2d"></a>LPD3DXFILL2D

Tipo di funzione usato dalle funzioni di riempimento della trama.

## <a name="syntax"></a>Sintassi


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a>Parametri

Puntatore broncio a un vettore, usato dalla funzione per restituirne il risultato. Verrà eseguito il mapping di X, Y, Z e W rispettivamente a R, G, B e A.

pTexCoord: puntatore a un vettore che contiene le coordinate del Texel attualmente in fase di valutazione. I componenti delle coordinate di trama per trama e trama del volume variano da 0 a 1. I componenti delle coordinate di trama per le trame del cubo variano da-1 a 1.

pTexelSize: puntatore a un vettore che contiene le dimensioni del Texel corrente.

pData: puntatore ai dati utente.

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Assicurarsi di specificare la convenzione di chiamata per i [**tipi di dati di Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback. In caso contrario, è possibile che si verifichino overflow dello stack.



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3dx9tex. h |
| Libreria di importazione           | d3dx9. lib  |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di callback](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL3D](lpd3dxfill3d.md)
</dt> </dl>

 

 
