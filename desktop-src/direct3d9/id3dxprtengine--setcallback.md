---
description: Imposta un puntatore a una funzione di callback facoltativa che calcola la percentuale di calcoli armonici sferici (SH) completati e fornisce al chiamante la possibilità di interrompere il simulatore.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'Metodo ID3DXPRTEngine:: secallback (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322979"
---
# <a name="id3dxprtenginesetcallback-method"></a>Metodo ID3DXPRTEngine:: secallback

Imposta un puntatore a una funzione di callback facoltativa che calcola la percentuale di calcoli armonici sferici (SH) completati e fornisce al chiamante la possibilità di interrompere il simulatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCB* \[ in\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Puntatore alla funzione di callback [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) che calcola la percentuale di calcoli SH completati. La funzione di callback deve essere implementata per restituire S \_ OK per tenere in esecuzione il simulatore. Qualsiasi altro valore interrompe il simulatore.

</dd> <dt>

*Frequenza* \[ di in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Frequenza delle chiamate di callback. L'inverso della frequenza è approssimativamente il numero di volte in cui la funzione di callback verrà chiamata.

</dd> <dt>

*lpUserContext* \[ in\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore a un valore definito dall'utente che viene passato alla funzione di callback. Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
