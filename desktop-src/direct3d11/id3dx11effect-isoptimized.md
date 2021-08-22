---
title: Metodo IsOptimized ID3DX11Effect (D3dx11effect.h)
description: Testare un effetto per verificare se i metadati di reflection sono stati rimossi dalla memoria.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Metodo IsOptimized Direct3D 11
- Metodo IsOptimized Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo IsOptimized
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd04bf43869f23bfec38db34be1b83b2c4f3953c7017120ebe2f0c985504b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124506"
---
# <a name="id3dx11effectisoptimized-method"></a>Metodo ID3DX11Effect::IsOptimized

Testare un effetto per verificare se i metadati di reflection sono stati rimossi dalla memoria.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE** se l'effetto è ottimizzato; in caso **contrario, FALSE.**

## <a name="remarks"></a>Commenti

Un effetto usa lo spazio di memoria in due modi diversi: per archiviare le informazioni richieste dal runtime per eseguire un effetto e per archiviare i metadati necessari per riflettere le informazioni a un'applicazione usando l'API. È possibile ridurre al minimo la quantità di memoria richiesta da un effetto chiamando [**ID3DX11Effect::Optimize**](id3dx11effect-optimize.md) che rimuove i metadati di reflection dalla memoria. Naturalmente, i metodi API per leggere le variabili non funzioneranno più dopo la rimozione dei dati di reflection.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

