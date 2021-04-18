---
description: Specifica il ruolo del dispositivo per il flusso audio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: Attributo MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320552"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a><span data-ttu-id="1775c-103">\_Attributo del \_ \_ ruolo dell' \_ endpoint audio del motore multimediale \_ MF</span><span class="sxs-lookup"><span data-stu-id="1775c-103">MF\_MEDIA\_ENGINE\_AUDIO\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="1775c-104">Specifica il ruolo del dispositivo per il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="1775c-104">Specifies the device role for the audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="1775c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1775c-105">Data type</span></span>

<span data-ttu-id="1775c-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1775c-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1775c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="1775c-107">Remarks</span></span>

<span data-ttu-id="1775c-108">Il valore di questo attributo è un membro dell'enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .</span><span class="sxs-lookup"><span data-stu-id="1775c-108">The value of this attribute is a member of the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>

<span data-ttu-id="1775c-109">Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="1775c-109">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="1775c-110">L'attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1775c-110">The attribute is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1775c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1775c-111">Requirements</span></span>



| <span data-ttu-id="1775c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1775c-112">Requirement</span></span> | <span data-ttu-id="1775c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="1775c-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1775c-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1775c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1775c-115">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1775c-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="1775c-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1775c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1775c-117">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1775c-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1775c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1775c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1775c-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1775c-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1775c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1775c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1775c-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1775c-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
