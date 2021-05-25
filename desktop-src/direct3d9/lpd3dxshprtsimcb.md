---
description: Funzione di callback per la simulazione e la compressione PRT (Precomputed Radiance Transfer).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a7c4911bf2a7b7fa2aa83422a206644f6eb747
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342806"
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

fPercentDone : numero a virgola mobile compreso tra 0 e 1,0 che rappresenta la percentuale di calcoli completati (tra 0 e 100%).

lpUserContext: puntatore a un valore definito dall'utente passato alla funzione di callback. in genere usato da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.

## <a name="return-value"></a>Valore restituito

Questa funzione deve essere implementata per restituire S \_ OK per continuare a eseguire il simulatore. Qualsiasi altro valore arresterà il simulatore.

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

 

 
