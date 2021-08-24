---
title: Costanti Direct2D
description: Direct2D definisce l'elenco di costanti seguente.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: cd8adfa3d6fa3c59a05331c82ea12100918a4697d9478097a890eedff039d5e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768731"
---
# <a name="direct2d-constants"></a>Costanti Direct2D

Le costanti seguenti vengono dichiarate nei file `d2d1effectauthor.h` di intestazione , , e `d2d1.h` `d2d1_1.h` `d2d1effects_2.h` .

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1)
Utilizzato per la creazione di un pacchetto di elementi di layout di input. Indica che gli elementi devono essere imballati in modo contiguo.

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25f)
Tolleranza predefinita per le operazioni di appiattimento geometrico.

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)
Definisce un indice di proprietà non valido.

Questa costante viene restituita da [**ID2D1Properties::GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) per indicare che la proprietà denominata specificata non ha un indice nell'interfaccia delle proprietà.

Se si passa questa costante a [**ID2D1Properties::GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) o [**ID2D1Properties::GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), la chiamata ha esito negativo e il buffer di output è con riempimento zero.

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX)
Riservato; non usare .

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0f)
Numero di lendini che lo spazio colori sRGB o scRGB usa per il bianco SDR o valori a virgola mobile di 1,0f. Questo valore è costante solo quando lo spazio colori usa la luminanza con riferimento alla scena, che è vera per il contenuto HDR (High Dynamic Range). Se invece lo spazio colori usa la luminanza indicata dalla visualizzazione, il livello di bianco SDR deve essere sottoposto a query dal display.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 7, Windows Vista con SP2 e Aggiornamento piattaforma per Windows app desktop di Vista \[ \| app UWP\] |
| Server minimo supportato | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per Windows app desktop di Windows Server 2008 \[ app desktop \| UWP\] |
| Telefono minimo supportato | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e app Windows Runtime \] , Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e app Windows Runtime\] |
| Intestazione | d2d1effectauthor.h, d2d1.h, d2d1_1.h, d2d1effects_2.h |
