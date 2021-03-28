---
title: 'Funzione StructuredBuffer:: Load (int)'
description: 'Legge i dati del buffer. | Funzione StructuredBuffer:: Load (int)'
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
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
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981898"
---
# <a name="structuredbufferloadint-function"></a>Funzione StructuredBuffer:: Load (int)

Legge i dati del buffer.

## <a name="syntax"></a>Sintassi


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ in\]
</dt> <dd>

Tipo: **int**

Posizione del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Digitare:

Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**StructuredBuffer**](sm5-object-structuredbuffer.md) .

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load](structuredbuffer-load.md)
</dt> </dl>

 

 




