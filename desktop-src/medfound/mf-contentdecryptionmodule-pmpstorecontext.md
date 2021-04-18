---
description: Specifica una stringa di contesto usata dalle implementazioni del modulo di decrittografia del contenuto (CDM) che usano MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309578"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a>\_ \_ Proprietà PMPSTORECONTEXT di MF CONTENTDECRYPTIONMODULE

Specifica una stringa di contesto usata dalle implementazioni del modulo di decrittografia del contenuto (CDM) che usano [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).


## <a name="data-type"></a>Tipo di dati

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID proprietà

**MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT**

## <a name="property-value"></a>Valore proprietà

Stringa di contesto utilizzata dalle implementazioni del modulo di decrittografia del contenuto (CDM).

## <a name="remarks"></a>Commenti

Il responsabile dell'implementazione CDM deve cercare questo valore e passare il valore al [Costruttore MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) usando il nome della proprietà "Windows. Media. Protection. PMPStoreContext".


Le app non devono creare questa proprietà quando viene chiamato [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Aggiornamento di Windows 10 aprile 2020<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

- [Proprietà Media Foundation](media-foundation-properties.md)
- [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




