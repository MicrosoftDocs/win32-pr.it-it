---
description: Funzione di callback per UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342796"
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

\[out fPercentDone: numero a virgola mobile compreso tra 0 e 1,0 che rappresenta la percentuale di calcoli completati \] (tra 0 e 100%).

\[in lpUserContext: puntatore a un valore definito dall'utente passato alla funzione di callback; in genere usato da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione \] di callback.

## <a name="return-value"></a>Valore restituito

Questa funzione deve essere implementata per restituire S \_ OK per continuare a eseguire il simulatore. Qualsiasi altro valore interromperà il simulatore.

## <a name="remarks"></a>Commenti

Assicurarsi di specificare la convenzione [**di chiamata dei tipi di dati Windows**](../winprog/windows-data-types.md) quando si dichiara la funzione di callback. In caso contrario, possono verificarsi overflow dello stack.



| Requisito                         | Valore            |
|--------------------------|-------------|
| Intestazione                   | d3dx9mesh.h |
| Libreria di importazione           | d3dx9.lib   |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di callback](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
