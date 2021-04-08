---
description: Specifica il modo in cui il sink multimediale ASF deve applicare Windows Media DRM.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: Proprietà MFPKEY_ASFMEDIASINK_DRMACTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761477"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>MFPKEY \_ ASFMEDIASINK- \_ Proprietà DRMACTION

Specifica il modo in cui il sink multimediale ASF deve applicare Windows Media DRM.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**ULONG**

\_UI4 VT

**ulVal**



## <a name="remarks"></a>Commenti

Il valore di questa proprietà è un membro dell'enumerazione [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .

È possibile utilizzare questo attributo per configurare il sink del supporto ASF. L'utilizzo dipende dalla funzione chiamata per creare il sink multimediale ASF:

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): esegue una query sul puntatore [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperato per l'interfaccia **IPropertyStore** .

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sul puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) specificato nel parametro *pContentInfo* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
