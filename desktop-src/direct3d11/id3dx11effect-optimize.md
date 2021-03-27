---
title: Metodo Optimize ID3DX11Effect (D3dx11effect. h)
description: Ridurre al minimo la quantità di memoria necessaria per un effetto.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Metodo Optimize Direct3D 11
- Metodo Optimize Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, Metodo Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996089"
---
# <a name="id3dx11effectoptimize-method"></a>Metodo ID3DX11Effect:: Optimize

Ridurre al minimo la quantità di memoria necessaria per un effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Optimize();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Un effetto usa uno spazio di memoria in due modi diversi: per archiviare le informazioni richieste dal runtime per eseguire un effetto e per archiviare i metadati necessari per riportare le informazioni a un'applicazione usando l'API. È possibile ridurre al minimo la quantità di memoria necessaria per un effetto chiamando **ID3DX11Effect:: Optimize** che rimuove i metadati della reflection dalla memoria. I metodi API per leggere le variabili non funzioneranno più dopo la rimozione dei dati di Reflection.

I metodi seguenti avranno esito negativo dopo la chiamata di optimize su un effetto.

-   [**ID3DX11Effect::GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md)
-   [**ID3DX11Effect::GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)
-   [**ID3DX11Effect:: getdesc**](id3dx11effect-getdesc.md)
-   [**ID3DX11Effect:: GetDevice**](id3dx11effect-getdevice.md)
-   [**ID3DX11Effect::GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)
-   [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)
-   [**ID3DX11Effect::GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)
-   [**ID3DX11Effect::GetVariableByName**](id3dx11effect-getvariablebyname.md)
-   [**ID3DX11Effect::GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> I riferimenti recuperati con questi metodi prima di chiamare **ID3DX11Effect:: Optimize** sono ancora validi dopo la chiamata a **ID3DX11Effect:: Optimize** . Ciò consente all'applicazione di ottenere tutte le variabili, le tecniche e le passate che utilizzeranno, chiamare optimize e quindi usare l'effetto.

 

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





