---
title: Costanti Direct2D
description: Direct2D definisce l'elenco seguente di costanti.
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
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302108"
---
# <a name="direct2d-constants"></a>Costanti Direct2D

Le costanti seguenti sono dichiarate nei `d2d1effectauthor.h` `d2d1.h` file di intestazione,, `d2d1_1.h` e `d2d1effects_2.h` .

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1)
Utilizzato per la compressione degli elementi di layout di input. Indica che gli elementi devono essere compressi in modo contiguo.

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)
Tolleranza predefinita per le operazioni di Flat geometrico.

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)
Definisce un indice di proprietà non valido.

Questa costante viene restituita da [**ID2D1Properties:: GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) per indicare che la proprietà denominata fornita non ha un indice nell'interfaccia della proprietà.

Se si passa questa costante a [**ID2D1Properties:: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) o [**ID2D1Properties:: GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), la chiamata ha esito negativo e il buffer di output viene riempito con zero.

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX)
Riservati Non usare.

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0 f)
Numero di NIT utilizzati dallo spazio dei colori sRGB o scRGB per i valori di DSP bianco o a virgola mobile pari a 1,0 f. Questo valore è costante solo quando lo spazio dei colori usa una luminanza a cui viene fatto riferimento dalla scena, che è vera per il contenuto HDR (High Dynamic Range). Se lo spazio dei colori usa invece la luminanza a cui viene fatto riferimento, è necessario eseguire una query sul livello del bianco SDR dallo schermo.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\] |
| Server minimo supportato | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\] |
| Telefono minimo supportato | Windows Phone 8,1 \[ Windows Phone silverlight 8,1 e Windows Runtime app \] , Windows Phone 8,1 \[ Windows Phone silverlight 8,1 e Windows Runtime app\] |
| Intestazione | d2d1effectauthor. h, d2d1. h, d2d1_1. h, d2d1effects_2. h |
