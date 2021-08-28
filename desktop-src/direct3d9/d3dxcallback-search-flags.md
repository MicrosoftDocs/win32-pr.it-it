---
description: Flag utilizzati per ottenere informazioni di callback.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: D3DXCALLBACK_SEARCH_FLAGS enumerazione (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0a050263934684f766bb9b7d58b83665a31a5edbd099a43ad1947eba74ca25bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676381"
---
# <a name="d3dxcallback_search_flags-enumeration"></a>Enumerazione D3DXCALLBACK \_ SEARCH \_ FLAGS

Flag utilizzati per ottenere informazioni di callback.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**RICERCA D3DXCALLBACK \_ \_ ESCLUSA \_ LA POSIZIONE \_ INIZIALE**
</dt> <dd>

Escludere dalla ricerca i callback che si trovano nella posizione iniziale.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**RICERCA DI D3DXCALLBACK \_ \_ DIETRO LA POSIZIONE \_ \_ INIZIALE**
</dt> <dd>

Invertire la direzione di ricerca del callback.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK \_ SEARCH \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




