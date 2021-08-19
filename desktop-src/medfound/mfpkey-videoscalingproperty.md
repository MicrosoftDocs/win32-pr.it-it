---
description: Specifica se il codec userà l'ottimizzazione del ridimensionamento video.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: MFPKEY_VIDEOSCALING proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2dc069d70b167dd8da6cb308d70149aec1028f3aaf4e50b5c1cc8ab11104c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887653"
---
# <a name="mfpkey_videoscaling-property"></a>Proprietà VIDEOCALING di MFPKEY \_

Specifica se il codec userà l'ottimizzazione del ridimensionamento video.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCVideoScaling

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Il ridimensionamento video è un tipo di ottimizzazione percettiva che può migliorare la qualità visiva del video codificato a velocità in bit basse. L'ottimizzazione del ridimensionamento video riduce gli artefatti pronunciati, ma può sacrificare i dettagli dell'immagine. Questa ottimizzazione influisce sull'intervallo luma del video codificato come descritto di seguito, ma non influisce sulla risoluzione fisica del video di output.

Questa proprietà può essere impostata su uno dei valori seguenti.



| Valore | Descrizione                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| 0     | Il ridimensionamento video non verrà usato.                                                                                       |
| 1     | Il codificatore userà l'ottimizzazione conservativa del ridimensionamento video. L'intervallo luma verrà ridimensionato da 0...255 a 26...229. |
| 2     | Il codificatore userà un'ottimizzazione aggressiva del ridimensionamento video. L'intervallo luma verrà ridimensionato da 0...255 a 31...224.   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




