---
title: Proprietà MinimumScaleRotateRadius di IManipulationProcessor
description: Specifica la dimensione dei contatti di distanza in un movimento di ridimensionamento o rotazione che devono essere per attivare la manipolazione.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Proprietà di MinimumScaleRotateRadius Windows Touch
- Proprietà MinimumScaleRotateRadius Windows Touch, interfaccia IManipulationProcessor
- Interfaccia IManipulationProcessor Windows Touch, Proprietà MinimumScaleRotateRadius
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718619"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a>Proprietà IManipulationProcessor:: MinimumScaleRotateRadius

Specifica la dimensione dei contatti di distanza in un movimento di ridimensionamento o rotazione che devono essere per attivare la manipolazione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a>Valore proprietà

Specifica la distanza minima tra i contatti per attivare il ridimensionamento o la rotazione dei movimenti.

## <a name="error-codes"></a>Codici di errore

## <a name="remarks"></a>Commenti

> [!Note]  
> Questa proprietà viene impostata in centipixels (100 di un pixel).

 

Impostando questo valore si farà in modo che il processore di manipolazione ignori i movimenti con un raggio troppo piccolo. Questa opzione è utile se si desidera impedire a un utente di modificare un oggetto in un raggio troppo piccolo. Se, ad esempio, si utilizza un processore di manipolazione con un cerchio e si desidera assicurarsi che mantenga un raggio maggiore di 100 pixel, impostare questo valore su 10000.

## <a name="examples"></a>Esempi


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




