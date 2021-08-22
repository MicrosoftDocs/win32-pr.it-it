---
description: Imposta la velocità di input massima in tempo reale dei fotogrammi video da inserire nel codificatore.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: CODECAPI_AVEncMaxFrameRate proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb4202dd2079cc013560947ef11581cdb24b92ad0aaaf544e12923d5e46b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974930"
---
# <a name="codecapi_avencmaxframerate-property"></a>PROPRIETÀ CODECAPI \_ AVEncMaxFrameRate

Imposta la velocità di input massima in tempo reale dei fotogrammi video da inserire nel codificatore.

## <a name="data-type"></a>Tipo di dati

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncMaxFrameRate**

## <a name="remarks"></a>Commenti

Questa proprietà consente al chiamante di specificare la velocità di input in tempo reale massima dei fotogrammi video da inserire nel codificatore. Questo fornisce al codificatore un'indicazione della velocità necessaria per elaborare i fotogrammi in ingresso. Ciò è utile per i codificatori che si impostano in una particolare configurazione dello stato di alimentazione in base alla risoluzione e alla frequenza dei fotogrammi del video di origine.

La frequenza dei fotogrammi è espressa come rapporto. I 32 bit superiori del valore dell'attributo contengono il numeratore e i 32 bit inferiori contengono il denominatore. Ad esempio, se la frequenza dei fotogrammi è di 30 fotogrammi al secondo (fps), il rapporto è 30/1. Se la frequenza dei fotogrammi è 29,97 fps, il rapporto è 30.000/1001.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

