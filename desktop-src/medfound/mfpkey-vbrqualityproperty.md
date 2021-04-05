---
description: Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: Proprietà MFPKEY_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967162"
---
# <a name="mfpkey_vbrquality-property"></a>\_Proprietà VBRQUALITY di MFPKEY

Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCVBRQuality, g \_ wszWMCPAudioVBRQuality

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

Non tutti i valori nell'intervallo hanno un significato univoco. I valori che rappresentano un passaggio di qualità rispetto al livello precedente sono: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 e 100.

Per gli oggetti del codificatore audio, le modalità di qualità vengono fornite nella struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) dei tipi di output recuperati tramite [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazione dei tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
