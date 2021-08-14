---
description: Specifica la modalità di applicazione del sink multimediale ASF Windows DRM multimediale.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: MFPKEY_ASFMEDIASINK_DRMACTION proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed62f62a5d03d7fe938101d9837bd8ed9bccefe69b2bf30e0566ea0b471e37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874345"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>MFPKEY \_ ASFMEDIASINK \_ DRMACTION - proprietà

Specifica la modalità di applicazione del sink multimediale ASF Windows DRM multimediale.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Ulong**

Interfaccia utente \_ VT4

**ulVal**



## <a name="remarks"></a>Commenti

Il valore di questa proprietà è un membro [**dell'enumerazione MFSINK \_ WMDRMACTION.**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction)

È possibile usare questo attributo per configurare il sink multimediale ASF. L'utilizzo dipende dalla funzione chiamata per creare il sink multimediale ASF:

-   [**MFCreateASFMediaSink:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)esegue una query sul puntatore [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperato per **l'interfaccia IPropertyStore.**

-   [**MFCreateASFMediaSinkActivate:**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)chiamare [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sul puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) specificato nel *parametro pContentInfo.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
