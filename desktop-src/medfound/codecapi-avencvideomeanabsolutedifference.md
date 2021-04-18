---
description: Controlla la segnalazione di MFSampleExtension \_ MeanAbsoluteDifference tramite IMFAttribute in ogni esempio di output.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: Proprietà CODECAPI_AVEncVideoMeanAbsoluteDifference (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305487"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a>Proprietà AVEncVideoMeanAbsoluteDifference di codecapi \_

Controlla la segnalazione di [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) tramite [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) in ogni esempio di output.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoMeanAbsoluteDifference**

## <a name="remarks"></a>Commenti

Se l'applicazione imposta un valore diverso da zero, il codificatore deve aggiungere l'attributo di esempio [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a ogni esempio di output. L' \_ attributo MeanAbsoluteDifference di MFSampleExtension indica la differenza assoluta media tra gli esempi di origine e gli esempi stimati nel piano Y.

Se il codificatore restituisce 0 per **GetParameterRange**, il codificatore non supporta l'output di [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sugli esempi di output.

Il valore predefinito deve essere 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




