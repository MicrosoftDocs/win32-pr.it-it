---
description: Consente all'applicazione di eseguire l'override delle impostazioni predefinite per varie proprietà del DSP di acquisizione voce.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: Proprietà MFPKEY_WMAAECMA_FEATURE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753959"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a>\_ \_ Proprietà modalità funzionalità WMAAECMA MFPKEY \_

Consente all'applicazione di eseguire l'override delle impostazioni predefinite per varie proprietà del DSP di acquisizione voce.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

VARIANTE \_ false

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Se questa proprietà è VARIANT \_ true, l'applicazione può impostare le proprietà seguenti nel DSP:

-   [MFPKEY \_ WMAAECMA \_ featr \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)
-   [MFPKEY \_ WMAAECMA \_ featr \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)
-   [\_clip MFPKEY WMAAECMA \_ featr \_ Center \_](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [\_lunghezza Echo MFPKEY WMAAECMA \_ featr \_ \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [\_dimensioni frame MFPKEY WMAAECMA \_ Feater \_ \_](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [\_modalità MFPKEY WMAAECMA \_ featr \_ MICARR \_](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [MFPKEY \_ WMAAECMA \_ featr \_ MICARR \_ Preproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [\_riempimento rumore MFPKEY WMAAECMA \_ featr \_ \_](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [\_NS MFPKEY WMAAECMA \_ featr \_](mfpkey-wmaaecma-featr-nsproperty.md)
-   [\_VAD MFPKEY WMAAECMA \_ featr \_](mfpkey-wmaaecma-featr-vadproperty.md)

Se questa proprietà è VARIANT \_ false, il DSP ignora queste proprietà e usa le impostazioni predefinite. Il valore predefinito di questa proprietà è VARIANT \_ false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP di acquisizione vocale](voicecapturedmo.md)
</dt> </dl>

 

 
