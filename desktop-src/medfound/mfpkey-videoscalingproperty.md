---
description: Specifica se il codec utilizzerà l'ottimizzazione del ridimensionamento del video.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: Proprietà MFPKEY_VIDEOSCALING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880626"
---
# <a name="mfpkey_videoscaling-property"></a>\_Proprietà VIDEOSCALING di MFPKEY

Specifica se il codec utilizzerà l'ottimizzazione del ridimensionamento del video.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCVideoScaling

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Il ridimensionamento video è un tipo di ottimizzazione percettiva che può migliorare la qualità visiva del video codificato a velocità in bit basso. L'ottimizzazione del ridimensionamento del video riduce gli artefatti pronunciati, ma può sacrificare i dettagli dell'immagine. Questa ottimizzazione influisce sull'intervallo di Luma del video codificato, come descritto di seguito, ma non influisce sulla risoluzione fisica del video di output.

Questa proprietà può essere impostata su uno dei valori seguenti.



| Valore | Descrizione                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| 0     | Il ridimensionamento video non verrà usato.                                                                                       |
| 1     | Il codificatore userà l'ottimizzazione del ridimensionamento video conservativa. L'intervallo di Luma verrà ridimensionato da 0... 255 a 26... 229. |
| 2     | Il codificatore userà un'ottimizzazione di ridimensionamento video aggressiva. L'intervallo di Luma verrà ridimensionato da 0... 255 a 31... 224.   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




