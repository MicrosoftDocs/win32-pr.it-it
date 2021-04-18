---
description: Ottiene le dimensioni in pixel dell'immagine decodificata.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Proprietà AVDecVideoImageSize (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304250"
---
# <a name="avdecvideoimagesize-property"></a>Proprietà AVDecVideoImageSize

Ottiene le dimensioni in pixel dell'immagine decodificata.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecVideoImageSize**

## <a name="property-value"></a>Valore proprietà

I 16 bit alti contengono la larghezza e i 16 bit bassi contengono l'altezza.

## <a name="remarks"></a>Commenti

Il numero di canali include il canale LFE (Low Frequency Effect), se presente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




