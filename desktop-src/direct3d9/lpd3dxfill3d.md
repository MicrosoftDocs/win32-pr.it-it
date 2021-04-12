---
description: Tipo di funzione usato dalle funzioni di riempimento della trama.
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97342895cb119a786aa71626aeea6d93650c6dc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482053"
---
# <a name="lpd3dxfill3d"></a>LPD3DXFILL3D

Tipo di funzione usato dalle funzioni di riempimento della trama.

## <a name="syntax"></a>Sintassi


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
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

[LPD3DXFILL2D](lpd3dxfill2d.md)
</dt> </dl>

 

 
