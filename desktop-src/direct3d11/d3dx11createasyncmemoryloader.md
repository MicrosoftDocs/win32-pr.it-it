---
title: Funzione D3DX11CreateAsyncMemoryLoader (D3DX11async.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un caricatore di memoria asincrona.
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- Funzione D3DX11CreateAsyncMemoryLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c65f1f094337aed5fee6b026896bba98c151576077c4d89ad750486e0fa48cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124876"
---
# <a name="d3dx11createasyncmemoryloader-function"></a>Funzione D3DX11CreateAsyncMemoryLoader

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.

 

Creare un caricatore di memoria asincrona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Puntatore ai dati.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Dimensioni dei dati.

</dd> <dt>

*ppDataLoader* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***

Indirizzo di un puntatore al caricatore di dati asincroni (vedere [**Interfaccia ID3DX11DataLoader).**](id3dx11dataloader.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Non esiste alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.

Per Windows Store, gli esempi di DirectX (ad esempio, l'esempio di esercitazione [Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

Per le app desktop Win32, è possibile usare il runtime di concorrenza per implementare un elemento simile al modello di programmazione asincrona Windows Runtime. [](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

