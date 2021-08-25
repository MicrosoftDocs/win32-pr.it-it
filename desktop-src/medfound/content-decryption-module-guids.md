---
description: I GUID seguenti supportano le implementazioni di Content Decryption Module (CDM).
title: GUID Content Decryption Module (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: ef4016b731b492ed61c6aed859a905446de72c308e03a734aa3cc8f573645668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958781"
---
# <a name="content-decryption-module-cdm-guids"></a>GUID Content Decryption Module (CDM)

I GUID seguenti supportano le implementazioni di Content Decryption Module (CDM).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

GUID del servizio usato per ottenere interfacce da [un'implementazione di IMFContentDecryptionModule,](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) ad esempio l'interfaccia [WinRT IMediaProtectionPMPServer.](/uwp/api/windows.media.protection.mediaprotectionpmpserver) Un'implementazione **di IMFContentDecryptionModule deve** implementare [IMFGetService e](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) supportare questo GUID del servizio.


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche



- [Media Foundation costanti](media-foundation-constants.md)
- [IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule
- [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




