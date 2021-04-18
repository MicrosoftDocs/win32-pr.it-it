---
description: Funzione di callback per UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda7c58ef001a936b01f3af2027f9207c3d2770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304094"
---
# <a name="lpd3dxuvatlascb"></a>LPD3DXUVATLASCB

Funzione di callback per UVAtlas.

## <a name="syntax"></a>Sintassi


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parametri

\[out \] fPercentDone-numero a virgola mobile compreso tra 0 e 1,0 che rappresenta la percentuale di calcoli completati (compreso tra 0 e 100%).

\[in \] lpUserContext-puntatore a un valore definito dall'utente che viene passato alla funzione di callback; in genere utilizzato da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.

## <a name="return-value"></a>Valore restituito

Questa funzione deve essere implementata per restituire S \_ OK per tenere in esecuzione il simulatore. Qualsiasi altro valore arresterà il simulatore.

## <a name="remarks"></a>Commenti

Assicurarsi di specificare la convenzione di chiamata per i [**tipi di dati di Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback. In caso contrario, è possibile che si verifichino overflow dello stack.



|                          |             |
|--------------------------|-------------|
| Intestazione                   | d3dx9mesh. h |
| Libreria di importazione           | d3dx9. lib   |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di callback](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
