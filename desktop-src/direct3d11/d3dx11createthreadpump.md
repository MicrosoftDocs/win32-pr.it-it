---
title: Funzione D3DX11CreateThreadPump (D3DX11core.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare una pompa di thread.
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
ms.openlocfilehash: 9a3a19c338b330604caae9ce5a1e7f7222664b0521f9874c3eff07ff1fc8a4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536102"
---
# <a name="d3dx11createthreadpump-function"></a>Funzione D3DX11CreateThreadPump

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

*cIoThreads* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di thread di I/O da creare. Se si specifica 0, Direct3D tenterà di calcolare il numero ottimale di thread in base alla configurazione hardware.

</dd> <dt>

*cProcThreads* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di thread di processo da creare. Se si specifica 0, Direct3D tenterà di calcolare il numero ottimale di thread in base alla configurazione hardware.

</dd> <dt>

*ppThreadPump* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***

Thread pump creato. Vedere [**Interfaccia ID3DX11ThreadPump.**](id3dx11threadpump.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Un thread pump è un oggetto a elevato utilizzo di risorse. È necessario creare un solo thread pump per ogni applicazione.

Non esiste alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.

Per Windows Store, gli esempi di DirectX (ad esempio, l'esempio di esercitazione [Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

Per le app desktop Win32, è possibile usare il runtime di concorrenza per implementare un elemento simile al modello di programmazione asincrona Windows Runtime. [](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

