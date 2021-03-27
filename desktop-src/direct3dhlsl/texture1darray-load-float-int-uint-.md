---
title: 'Funzione Texture1DArray:: Load (int, int, uint)'
description: "Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture1DArray:: Load (int, int, uint)"
ms.assetid: D5877CED-BE73-4E37-B09D-4096726776EC
keywords:
- Funzione Load HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee367aaf98aa971aa10c6859f117f15df9fcdd83
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981463"
---
# <a name="texture1darrayloadintintuint-function"></a>Funzione Texture1DArray:: Load (int, int, uint)

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

*Posizione* \[ in\]
</dt> <dd>

Tipo: **int**

Coordinate di trama.

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Tipo: **int**

Offset applicato alle coordinate di trama prima del campionamento.

</dd> <dt>

*Stato* \[ di out\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features). Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Digitare:

Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**Texture1DArray**](sm5-object-texture1darray.md) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load](texture1darray-load.md)
</dt> </dl>

 

 
