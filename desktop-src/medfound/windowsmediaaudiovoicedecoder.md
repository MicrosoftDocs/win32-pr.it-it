---
description: Il decodificatore Voice Windows Media Audio decodifica i flussi codificati dal codificatore Voice Windows Media Audio.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Decodificatore Windows Media Audio Voice (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326964"
---
# <a name="windows-media-audio-voice-decoder"></a><span data-ttu-id="8d182-103">Decodificatore Voice Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="8d182-103">Windows Media Audio Voice Decoder</span></span>

<span data-ttu-id="8d182-104">Il decodificatore Voice Windows Media Audio decodifica i flussi codificati dal [**codificatore voice Windows Media Audio**](windowsmediaaudiovoiceencoder.md).</span><span class="sxs-lookup"><span data-stu-id="8d182-104">The Windows Media Audio Voice decoder decodes streams that were encoded by the [**Windows Media Audio Voice Encoder**](windowsmediaaudiovoiceencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="8d182-105">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="8d182-105">Class Identifier</span></span>

<span data-ttu-id="8d182-106">L'identificatore di classe (CLSID) per il decodificatore Voice Windows Media Audio è rappresentato dalla costante **CLSID \_ CWMSPDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="8d182-106">The class identifier (CLSID) for the Windows Media Audio Voice decoder is represented by the constant **CLSID\_CWMSPDecMediaObject**.</span></span> <span data-ttu-id="8d182-107">È possibile creare un'istanza del decodificatore vocale chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="8d182-107">You can create an instance of the voice decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="8d182-108">Formati di input</span><span class="sxs-lookup"><span data-stu-id="8d182-108">Input Formats</span></span>

<span data-ttu-id="8d182-109">Windows Media Audio contenuto con codifica Voice viene identificato dal tag di formato 0x00A.</span><span class="sxs-lookup"><span data-stu-id="8d182-109">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d182-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d182-110">Requirements</span></span>



| <span data-ttu-id="8d182-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d182-111">Requirement</span></span> | <span data-ttu-id="8d182-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8d182-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d182-113">Client</span><span class="sxs-lookup"><span data-stu-id="8d182-113">Client</span></span><br/> | <span data-ttu-id="8d182-114">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="8d182-114">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="8d182-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d182-115">Header</span></span><br/> | <dl> <span data-ttu-id="8d182-116"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d182-116"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="8d182-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8d182-117">DLL</span></span><br/>    | <dl> <span data-ttu-id="8d182-118"><dt>Wmspdmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d182-118"><dt>Wmspdmod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d182-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d182-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d182-120">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="8d182-120">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="8d182-121">Uso del codec Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="8d182-121">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="8d182-122">Codificatore Voice Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="8d182-122">Windows Media Audio Voice Encoder</span></span>](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




