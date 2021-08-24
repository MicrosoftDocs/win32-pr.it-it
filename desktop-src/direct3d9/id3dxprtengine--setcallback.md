---
description: Imposta un puntatore a una funzione di callback facoltativa che calcola la percentuale di calcoli sferici aricali completati e offre al chiamante la possibilità di interrompere il simulatore.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: Metodo ID3DXPRTEngine::SetCallBack (D3DX9Mesh.h)
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
ms.openlocfilehash: e1ed2570c45380ce4faa0be42ddb9231d6420940dd9a6d669d6f2540154dc644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847360"
---
# <a name="id3dxprtenginesetcallback-method"></a>Metodo ID3DXPRTEngine::SetCallBack

Imposta un puntatore a una funzione di callback facoltativa che calcola la percentuale di calcoli sferici aricali completati e offre al chiamante la possibilità di interrompere il simulatore.

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

*pCB* \[ Pollici\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Puntatore alla funzione di callback [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) che calcola la percentuale di calcoli SH completati. La funzione di callback deve essere implementata per restituire S \_ OK per continuare a eseguire il simulatore. Qualsiasi altro valore interromperà il simulatore.

</dd> <dt>

*Frequenza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Frequenza delle chiamate di callback. L'inverso di Frequency corrisponde approssimativamente al numero di volte in cui verrà chiamata la funzione di callback.

</dd> <dt>

*lpUserContext* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore a un valore definito dall'utente passato alla funzione di callback. Utilizzato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
