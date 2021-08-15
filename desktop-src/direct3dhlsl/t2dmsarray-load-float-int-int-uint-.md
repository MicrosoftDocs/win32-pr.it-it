---
title: Funzione Texture2DMSArray::Load(int,int,int,uint)
description: Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture2DMSArray::Load(int,int,int,uint)
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
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
ms.openlocfilehash: c237de43a52650af1d365a6b95c47f51f525b698152b0be0adf2ffe83f15c1fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506879"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a>Funzione Texture2DMSArray::Load(int,int,int,uint)

Legge i dati della trama e restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
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

*sampleindex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Indice di esempio.

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

Il tipo restituito corrisponde al tipo nella dichiarazione per [**l'oggetto Texture2DMSArray.**](sm5-object-texture2dmsarray.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di caricamento](texture2dmsarray-load.md)
</dt> <dt>

[**Texture2DMSArray**](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
