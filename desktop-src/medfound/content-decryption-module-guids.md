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
# <a name="content-decryption-module-cdm-guids"></a><span data-ttu-id="5e7b2-103">GUID Content Decryption Module (CDM)</span><span class="sxs-lookup"><span data-stu-id="5e7b2-103">Content Decryption Module (CDM) GUIDs</span></span>

<span data-ttu-id="5e7b2-104">I GUID seguenti supportano le implementazioni del modulo di decrittografia del contenuto (CDM).</span><span class="sxs-lookup"><span data-stu-id="5e7b2-104">The following GUIDs support Content Decryption Module (CDM) implementations.</span></span>

<span data-ttu-id="5e7b2-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span><span class="sxs-lookup"><span data-stu-id="5e7b2-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span></span>

<span data-ttu-id="5e7b2-106">GUID del servizio usato per ottenere le interfacce da un'implementazione di [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , ad esempio l'interfaccia WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) .</span><span class="sxs-lookup"><span data-stu-id="5e7b2-106">Service GUID used to obtain interfaces from an [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) implementation,such as the WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) interface.</span></span> <span data-ttu-id="5e7b2-107">Un'implementazione di **IMFContentDecryptionModule** deve implementare [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) e supportare questo GUID del servizio.</span><span class="sxs-lookup"><span data-stu-id="5e7b2-107">An implementation of **IMFContentDecryptionModule** should implement [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) and support this service GUID.</span></span>


## <a name="requirements"></a><span data-ttu-id="5e7b2-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e7b2-108">Requirements</span></span>



| <span data-ttu-id="5e7b2-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e7b2-109">Requirement</span></span> | <span data-ttu-id="5e7b2-110">Valore</span><span class="sxs-lookup"><span data-stu-id="5e7b2-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e7b2-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e7b2-111">Header</span></span><br/> | <dl> <span data-ttu-id="5e7b2-112"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e7b2-112"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e7b2-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e7b2-113">See also</span></span>



- [<span data-ttu-id="5e7b2-114">Costanti Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e7b2-114">Media Foundation Constants</span></span>](media-foundation-constants.md)
- <span data-ttu-id="5e7b2-115">[IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span><span class="sxs-lookup"><span data-stu-id="5e7b2-115">[IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span></span>
- [<span data-ttu-id="5e7b2-116">IMediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="5e7b2-116">IMediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [<span data-ttu-id="5e7b2-117">IMFGetService</span><span class="sxs-lookup"><span data-stu-id="5e7b2-117">IMFGetService</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




