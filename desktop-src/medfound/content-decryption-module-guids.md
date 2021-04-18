---
description: I GUID seguenti supportano le implementazioni del modulo di decrittografia del contenuto (CDM).
title: GUID Content Decryption Module (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327701"
---
# <a name="content-decryption-module-cdm-guids"></a>GUID Content Decryption Module (CDM)

I GUID seguenti supportano le implementazioni del modulo di decrittografia del contenuto (CDM).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

GUID del servizio usato per ottenere le interfacce da un'implementazione di [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , ad esempio l'interfaccia WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) . Un'implementazione di **IMFContentDecryptionModule** deve implementare [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) e supportare questo GUID del servizio.


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche



- [Costanti Media Foundation](media-foundation-constants.md)
- [IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule
- [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




