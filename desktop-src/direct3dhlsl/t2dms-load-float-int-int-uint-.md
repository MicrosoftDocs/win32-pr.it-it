---
title: Funzione Texture2DMS::Load(int,int,int,uint)
description: Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture2DMS::Load(int,int,int,uint)
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: cb15f420699a9b581a6ac6f498c5e7ff07437ea4371bf1c59b004af1f5a963cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506883"
---
# <a name="texture2dmsloadintintintuint-function"></a>Funzione Texture2DMS::Load(int,int,int,uint)

Legge i dati della trama e restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Coordinate di trama.

</dd> <dt>

*sampleindex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Indice di esempio.

</dd> <dt>

*Offset* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Offset applicato alle coordinate della trama prima del caricamento.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE se** tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati presi valori da un riquadro non mappato, **CheckAccessFullyMapped restituisce** **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Digitare:

Il tipo restituito corrisponde al tipo nella dichiarazione per [**l'oggetto Texture2DMS.**](sm5-object-texture2dms.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di caricamento](texture2dms-load.md)
</dt> <dt>

[**Texture2DMS**](sm5-object-texture2dms.md)
</dt> </dl>

 

 
