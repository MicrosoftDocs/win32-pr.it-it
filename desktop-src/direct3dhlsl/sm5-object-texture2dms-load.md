---
title: Funzione Texture2DMS::Load(int,int)
description: Ottiene un valore. | Funzione Texture2DMS::Load(int,int)
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Caricare la funzione DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0997a1bd30b4912864674015057fcafec227d90ad05b16b88fd3f05b671f155c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285729"
---
# <a name="texture2dmsloadintint-function"></a>Funzione Texture2DMS::Load(int,int)

Ottiene un valore.

## <a name="syntax"></a>Sintassi

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*coord* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Posizione di input.

</dd> <dt>

*sampleindex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Indice di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **T**

Un valore il cui tipo corrisponde al tipo di modello di trama.

## <a name="remarks"></a>Commenti

Questo è un elenco delle versioni di overload di questo metodo.


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di caricamento](texture2dms-load.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
