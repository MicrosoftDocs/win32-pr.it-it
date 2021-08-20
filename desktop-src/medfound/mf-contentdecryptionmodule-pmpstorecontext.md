---
description: Specifica una stringa di contesto utilizzata dalle implementazioni cdM (Content Decryption Module) che usano MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: e82bfb5bcf833957fa07ec5aa5c6dacdab346905692ab7cfcf6cbb18b940817b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060715"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a>Proprietà MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT

Specifica una stringa di contesto utilizzata dalle implementazioni di Content Decryption Module (CDM) che usano [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).


## <a name="data-type"></a>Tipo di dati

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID proprietà

**MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT**

## <a name="property-value"></a>Valore proprietà

Stringa di contesto utilizzata dalle implementazioni di Content Decryption Module (CDM).

## <a name="remarks"></a>Commenti

L'implementatore CDM deve cercare questo valore e passare il valore al costruttore [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) usando il nome della proprietà "Windows. Media.Protection.PMPStoreContext".


Le app non devono creare questa proprietà quando chiamano [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10 Aggiornamento di aprile 2020<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

- [Media Foundation proprietà](media-foundation-properties.md)
- [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




