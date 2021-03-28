---
title: Metodo ID3DX11Effect ottimizzato (D3dx11effect. h)
description: Testare un effetto per verificare se i metadati della reflection sono stati rimossi dalla memoria.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Metodo di ottimizzazione Direct3D 11
- Metodo optimized Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo di ottimizzazione
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
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355539"
---
# <a name="id3dx11effectisoptimized-method"></a>Metodo ID3DX11Effect:: optimized

Testare un effetto per verificare se i metadati della reflection sono stati rimossi dalla memoria.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** se l'effetto è ottimizzato; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Un effetto usa uno spazio di memoria in due modi diversi: per archiviare le informazioni richieste dal runtime per eseguire un effetto e per archiviare i metadati necessari per riportare le informazioni a un'applicazione usando l'API. È possibile ridurre al minimo la quantità di memoria necessaria per un effetto chiamando [**ID3DX11Effect:: Optimize**](id3dx11effect-optimize.md) che rimuove i metadati della reflection dalla memoria. Naturalmente, i metodi API per leggere le variabili non funzioneranno più dopo la rimozione dei dati di Reflection.

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

 

