---
description: Funzione di callback per la simulazione e la compressione PRT (Precomputed Radiance Transfer).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81e510808dd2e14af1de0d9618591d8ea3b8587bb4015e72a3e01fa33157b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799334"
---
# <a name="lpd3dxshprtsimcb"></a>LPD3DXSHPRTSIMCB

Funzione di callback per la simulazione e la compressione PRT (Precomputed Radiance Transfer).

## <a name="syntax"></a>Sintassi


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parametri

fPercentDone: numero a virgola mobile compreso tra 0 e 1,0 che rappresenta la percentuale di calcoli completati (tra 0 e 100%).

lpUserContext: puntatore a un valore definito dall'utente passato alla funzione di callback; utilizzato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione di callback.

## <a name="return-value"></a>Valore restituito

Questa funzione deve essere implementata per restituire S \_ OK per continuare a eseguire il simulatore. Qualsiasi altro valore interromperà il simulatore.

## <a name="remarks"></a>Commenti

Assicurarsi di specificare la convenzione [**di chiamata Windows tipi di**](../winprog/windows-data-types.md) dati quando si dichiara la funzione di callback. In caso contrario, possono verificarsi overflow dello stack.



| Requisito                         | Valore            |
|--------------------------|-------------|
| Intestazione                   | d3dx9mesh.h |
| Libreria di importazione           | d3dx9.lib   |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di callback](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
