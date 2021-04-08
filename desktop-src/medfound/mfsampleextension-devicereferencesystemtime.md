---
description: Specifica il timestamp originale del dispositivo nell'esempio.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: Attributo MFSampleExtension_DeviceReferenceSystemTime (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880070"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>\_Attributo DeviceReferenceSystemTime di MFSampleExtension

Specifica il timestamp originale del dispositivo nell'esempio.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Si tratta del timestamp di riferimento del dispositivo degli esempi di supporti nella risoluzione 100 ns. Questo timestamp può contenere o meno il valore effettivo del contatore delle prestazioni della query (QPC), a seconda dell'origine che produce gli esempi. Questo valore può essere modificato da altri componenti della pipeline multimediale. Questo valore non è disponibile per MFTs inserito nella pipeline di acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                   |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




