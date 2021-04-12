---
description: Specifica se il motore di acquisizione usa l'accelerazione video DirectX (DXVA) per la decodifica dei video.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: Attributo MF_CAPTURE_ENGINE_DISABLE_DXVA (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343936"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>\_Motore di acquisizione MF disabilitare l' \_ \_ \_ attributo DXVA

Specifica se il motore di acquisizione usa l'accelerazione video DirectX (DXVA) per la decodifica dei video.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Questo attributo si applica se vengono soddisfatte le condizioni seguenti:

-   Il motore di acquisizione decodifica un flusso video compresso dal dispositivo di acquisizione, ad esempio se il dispositivo di acquisizione genera il video H. 264.
-   Il decodificatore video supporta la decodifica con accelerazione hardware con DXVA.
-   L'applicazione usa l'attributo di [ \_ \_ \_ \_ gestione D3D del motore di acquisizione MF](mf-capture-engine-d3d-manager.md) per impostare il gestione dispositivi DXGI nel motore di acquisizione.

In caso contrario, questo attributo viene ignorato.

Questo attributo consente all'applicazione di disabilitare DXVA, pur continuando a eseguire la decodifica nelle superfici Direct3D.

Il valore predefinito di questo attributo è **false**, vale a dire che la decodifica DXVA è abilitata quando disponibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore di acquisizione](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




