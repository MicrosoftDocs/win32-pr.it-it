---
description: 'LPD3DXFILL2D: tipo di funzione usato dalle funzioni di riempimento della trama.'
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8046c324511f2b308243d62fec1b6508a1d483ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087969"
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

pOut: puntatore a un vettore, che la funzione usa per restituire il risultato. X, Y, Z e W verranno mappati rispettivamente a R, G, B e A.

pTexCoord: puntatore a un vettore contenente le coordinate del texel attualmente valutato. I componenti delle coordinate di trama per le trame di trama e volume sono da 0 a 1. I componenti delle coordinate di trama per le trame dei cubi sono da -1 a 1.

pTexelSize: puntatore a un vettore contenente le dimensioni del texel corrente.

pData: puntatore ai dati utente.

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Assicurarsi di specificare la convenzione [**di chiamata dei tipi di dati Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback. In caso contrario, possono verificarsi overflow dello stack.



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3dx9tex.h |
| Libreria di importazione           | d3dx9.lib  |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di callback](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL3D](lpd3dxfill3d.md)
</dt> </dl>

 

 
