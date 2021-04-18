---
description: XAudio2 codici di errore specifici restituiti dai metodi XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Codici di errore XAudio2 (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332102"
---
# <a name="xaudio2-error-codes"></a><span data-ttu-id="cbd94-103">Codici di errore XAudio2</span><span class="sxs-lookup"><span data-stu-id="cbd94-103">XAudio2 Error Codes</span></span>

<span data-ttu-id="cbd94-104">XAudio2 codici di errore specifici restituiti dai metodi XAudio2.</span><span class="sxs-lookup"><span data-stu-id="cbd94-104">XAudio2 specific error codes returned by XAudio2 methods.</span></span>



| <span data-ttu-id="cbd94-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="cbd94-105">Constant/value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="cbd94-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbd94-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <span data-ttu-id="cbd94-107"><dt>**XAUDIO2 \_ E \_ \_ chiamata 0x88960001 non valida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cbd94-107"><dt>**XAUDIO2\_E\_INVALID\_CALL**</dt> <dt>0x88960001</dt></span></span> </dl>                          | <span data-ttu-id="cbd94-108">Restituito da XAudio2 per determinati errori di utilizzo dell'API (chiamate non valide e così via) difficili da evitare completamente e che devono essere gestiti da un titolo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cbd94-108">Returned by XAudio2 for certain API usage errors (invalid calls and so on) that are hard to avoid completely and should be handled by a title at runtime.</span></span> <span data-ttu-id="cbd94-109">Gli errori di utilizzo delle API che sono completamente evitabili, ad esempio parametri non validi, provocano un'ASSERZIONe nelle compilazioni di debug e un comportamento non definito nelle compilazioni finali, quindi non viene definito alcun codice di errore.</span><span class="sxs-lookup"><span data-stu-id="cbd94-109">(API usage errors that are completely avoidable, such as invalid parameters, cause an ASSERT in debug builds and undefined behavior in retail builds, so no error code is defined for them.)</span></span><br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <span data-ttu-id="cbd94-110"><dt>**XAUDIO2 \_ \_ \_ \_ Errore del decodificatore E XMA**</dt> <dt>0x88960002</dt></span><span class="sxs-lookup"><span data-stu-id="cbd94-110"><dt>**XAUDIO2\_E\_XMA\_DECODER\_ERROR**</dt> <dt>0x88960002</dt></span></span> </dl>          | <span data-ttu-id="cbd94-111">Si è verificato un errore irreversibile nell'hardware XMA di Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="cbd94-111">The Xbox 360 XMA hardware suffered an unrecoverable error.</span></span><br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <span data-ttu-id="cbd94-112"><dt>**XAUDIO2 \_ Creazione di E \_ XAPO \_ \_ non riuscita**</dt> <dt>0x88960003</dt></span><span class="sxs-lookup"><span data-stu-id="cbd94-112"><dt>**XAUDIO2\_E\_XAPO\_CREATION\_FAILED**</dt> <dt>0x88960003</dt></span></span> </dl> | <span data-ttu-id="cbd94-113">Non è stato possibile creare un'istanza di un effetto.</span><span class="sxs-lookup"><span data-stu-id="cbd94-113">An effect failed to instantiate.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <span data-ttu-id="cbd94-114"><dt>**XAUDIO2 \_ Dispositivo E 0x88960004 \_ \_ invalidato**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cbd94-114"><dt>**XAUDIO2\_E\_DEVICE\_INVALIDATED**</dt> <dt>0x88960004</dt></span></span> </dl>        | <span data-ttu-id="cbd94-115">Un dispositivo audio è diventato inutilizzabile durante la scollegamento o un altro evento.</span><span class="sxs-lookup"><span data-stu-id="cbd94-115">An audio device became unusable through being unplugged or some other event.</span></span><br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="cbd94-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbd94-116">Remarks</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="cbd94-117">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="cbd94-117">Platform Requirements</span></span>

<span data-ttu-id="cbd94-118">Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); DirectX SDK (XAudio 2,7)</span><span class="sxs-lookup"><span data-stu-id="cbd94-118">Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)</span></span>

## <a name="requirements"></a><span data-ttu-id="cbd94-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbd94-119">Requirements</span></span>



| <span data-ttu-id="cbd94-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbd94-120">Requirement</span></span> | <span data-ttu-id="cbd94-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cbd94-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd94-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbd94-122">Header</span></span><br/> | <dl> <span data-ttu-id="cbd94-123"><dt>Xaudio2. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbd94-123"><dt>Xaudio2.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd94-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbd94-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd94-125">XAudio2:: Constants</span><span class="sxs-lookup"><span data-stu-id="cbd94-125">XAudio2::Constants</span></span>](constants.md)
</dt> </dl>

 

 




