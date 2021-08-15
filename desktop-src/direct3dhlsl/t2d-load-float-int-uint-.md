---
title: Funzione Texture2D::Load(int,int,uint)
description: Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture2D::Load(int,int,uint)
ms.assetid: 05A12BE2-4604-470B-9EE8-F03F51E6D254
keywords:
- Caricare la funzione HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 890f49a0609367dcf91c91146f786568fdd83f0f207f7aa69d8dd7c4019b4d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507384"
---
# <a name="texture2dloadintintuint-function"></a>Funzione Texture2D::Load(int,int,uint)

Legge i dati della trama e restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Coordinate di trama.

</dd> <dt>

*Offset* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Offset applicato alle coordinate della trama prima del campionamento.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE se** tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati presi valori da un riquadro non mappato, **CheckAccessFullyMapped restituisce** **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Digitare:

Il tipo restituito corrisponde al tipo nella dichiarazione per [**l'oggetto Texture2D.**](sm5-object-texture2d.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di caricamento](texture2d-load.md)
</dt> </dl>

 

 
