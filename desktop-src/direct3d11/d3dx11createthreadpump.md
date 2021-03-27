---
title: Funzione D3DX11CreateThreadPump (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare una pompa di thread.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- Funzione D3DX11CreateThreadPump Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5551cd22a4c134570c2059cc6aeaa9538311b19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982337"
---
# <a name="d3dx11createthreadpump-function"></a>D3DX11CreateThreadPump (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.

 

Creare una pompa di thread.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cIoThreads* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di thread I/O da creare. Se si specifica 0, Direct3D tenterà di calcolare il numero ottimale di thread in base alla configurazione hardware.

</dd> <dt>

*cProcThreads* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di thread di processo da creare. Se si specifica 0, Direct3D tenterà di calcolare il numero ottimale di thread in base alla configurazione hardware.

</dd> <dt>

*ppThreadPump* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***

Pompa di thread creata. Vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Una pompa di thread è un oggetto con utilizzo intensivo delle risorse. Per ogni applicazione è necessario creare solo un thread pump.

Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.

Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

