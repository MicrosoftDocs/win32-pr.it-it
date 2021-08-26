---
description: Ottiene le dimensioni dell'immagine decodificata, in pixel.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Proprietà AVDecVideoImageSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4c059dfb1b2aebad4da10e54a3ecc1224a00d9cffcdb13dc7c87f4e29d4e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000191"
---
# <a name="avdecvideoimagesize-property"></a>AVDecVideoImageSize - proprietà

Ottiene le dimensioni dell'immagine decodificata, in pixel.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecVideoImageSize**

## <a name="property-value"></a>Valore proprietà

I 16 bit alti contengono la larghezza e i 16 bit bassi contengono l'altezza.

## <a name="remarks"></a>Commenti

Il numero di canali include il canale LFE (Low Frequency Effect), se presente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server desktop apps UWP apps (App desktop UWP di Windows 2000 \[ \| Server)\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




