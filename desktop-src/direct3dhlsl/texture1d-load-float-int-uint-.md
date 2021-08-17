---
title: Funzione Texture1D::Load(int,int,uint)
description: Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture1D::Load(int,int,uint)
ms.assetid: 5C489CBD-E4F6-4CB5-8E7E-EC34633D75B0
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
ms.openlocfilehash: b266ad13c050073aeb62497d9833b1f2666e70f2f32f2f9de5099cf4bee29517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722992"
---
# <a name="texture1dloadintintuint-function"></a>Funzione Texture1D::Load(int,int,uint)

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

*Località* \[ Pollici\]
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

Il tipo restituito corrisponde al tipo nella dichiarazione per [**l'oggetto Texture1D.**](sm5-object-texture1d.md)

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di caricamento](texture1d-load.md)
</dt> <dt>

[**Texture1D**](sm5-object-texture1d.md)
</dt> </dl>

 

 
