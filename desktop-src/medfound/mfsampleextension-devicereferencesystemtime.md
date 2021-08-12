---
description: Specifica il timestamp del dispositivo originale nell'esempio.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: MFSampleExtension_DeviceReferenceSystemTime attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0458c1a2b0f5b204483cba0e6f571a2a5ace34b7b39463cc20ded664eecaaa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241136"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>Attributo DeviceReferenceSystemTime di MFSampleExtension \_

Specifica il timestamp del dispositivo originale nell'esempio.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Si tratta del timestamp di riferimento del dispositivo degli esempi di supporti con risoluzione 100ns. Questo timestamp può contenere o meno il valore effettivo del contatore delle prestazioni di query (QPC), a seconda dell'origine che produce gli esempi. Questo valore può essere modificato da altri componenti nella pipeline multimediale. Questo valore non è disponibile per i MFT inseriti nella pipeline di acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                   |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




