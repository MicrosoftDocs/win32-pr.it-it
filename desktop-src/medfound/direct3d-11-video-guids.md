---
description: I GUID seguenti supportano le API Video Direct3D 11.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUID video Direct3D 11 (D3d11.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f5277123c3d174427debc3f0ad5e184e49a6c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118636"
---
# <a name="direct3d-11-video-guids"></a><span data-ttu-id="1e6e5-103">GUID video Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1e6e5-103">Direct3D 11 Video GUIDs</span></span>

<span data-ttu-id="1e6e5-104">I GUID seguenti supportano le API Video Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-104">The following GUIDs support Direct3D 11 Video APIs.</span></span>

<dl> <dt>

<span data-ttu-id="1e6e5-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**PROTEZIONE HW DELLO SCAMBIO DI \_ \_ \_ \_ CHIAVI D3D11**</span><span class="sxs-lookup"><span data-stu-id="1e6e5-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1e6e5-106">Indica che il decodificatore riceverà dati da un componente DRM basato su hardware</span><span class="sxs-lookup"><span data-stu-id="1e6e5-106">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="1e6e5-107">**D3D11 \_ KEY \_ EXCHANGE \_ HW \_ PROTECTION** può essere specificato nel *parametro pKeyExchangeType* della funzione [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) per indicare che l'interfaccia [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) verrà usata esclusivamente per la comunicazione tra un componente DRM in modalità utente e l'ambiente di esecuzione protetto.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-107">**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION** can be specified in the *pKeyExchangeType* parameter of the [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) function to indicate that the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) interface will be used purely for communication between a user mode DRM component and the secure execution environment.</span></span>

<span data-ttu-id="1e6e5-108">Quando viene specificato questo GUID, non è necessario chiamare i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e6e5-108">When this GUID is specified, the following methods should not be called:</span></span>

-   [<span data-ttu-id="1e6e5-109">**ID3D11CryptoSession::GetCertificateSize**</span><span class="sxs-lookup"><span data-stu-id="1e6e5-109">**ID3D11CryptoSession::GetCertificateSize**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [<span data-ttu-id="1e6e5-110">**ID3D11CryptoSession::GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="1e6e5-110">**ID3D11CryptoSession::GetCertificate**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [<span data-ttu-id="1e6e5-111">**ID3D11VideoContext::EncryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="1e6e5-111">**ID3D11VideoContext::EncryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [<span data-ttu-id="1e6e5-112">**ID3D11VideoContext::D ecryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="1e6e5-112">**ID3D11VideoContext::DecryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [<span data-ttu-id="1e6e5-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="1e6e5-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [<span data-ttu-id="1e6e5-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="1e6e5-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [<span data-ttu-id="1e6e5-115">**ID3D11VideoContext::GetEncryptionBltKey**</span><span class="sxs-lookup"><span data-stu-id="1e6e5-115">**ID3D11VideoContext::GetEncryptionBltKey**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e6e5-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ DECODER \_ ENCRYPTION \_ HW \_ CENC**</span><span class="sxs-lookup"><span data-stu-id="1e6e5-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11\_DECODER\_ENCRYPTION\_HW\_CENC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1e6e5-117">Indica che il decodificatore riceverà dati da un componente DRM basato su hardware</span><span class="sxs-lookup"><span data-stu-id="1e6e5-117">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="1e6e5-118">L'impostazione di questo GUID nel membro **guidConfigBitstreamEncryption** della struttura [**D3D11 \_ VIDEO \_ DECODER \_ CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) passata all'API [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indica che i parametri seguenti verranno passati nella chiamata [**ID3D11VideoDevice::D ecoderBeginFrame:**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)</span><span class="sxs-lookup"><span data-stu-id="1e6e5-118">Setting this GUID in the **guidConfigBitstreamEncryption** member of the [**D3D11\_VIDEO\_DECODER\_CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) structure passed to the [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API indicates that the following parameters will be passed in the [**ID3D11VideoDevice::DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) call:</span></span>



| <span data-ttu-id="1e6e5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1e6e5-119">Value</span></span>                 | <span data-ttu-id="1e6e5-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e6e5-120">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6e5-121">*ContentKeySize*</span><span class="sxs-lookup"><span data-stu-id="1e6e5-121">*ContentKeySize*</span></span> | <span data-ttu-id="1e6e5-122">Contiene le dimensioni della struttura [**D3D11 \_ VIDEO \_ DECODER \_ BEGIN FRAME \_ \_ CRYPTO \_ SESSION.**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session)</span><span class="sxs-lookup"><span data-stu-id="1e6e5-122">Contains the size of the [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) structure.</span></span>                                                                                                  |
| <span data-ttu-id="1e6e5-123">*pContentKey*</span><span class="sxs-lookup"><span data-stu-id="1e6e5-123">*pContentKey*</span></span>    | <span data-ttu-id="1e6e5-124">Puntatore a [**un oggetto D3D11 \_ VIDEO \_ DECODER BEGIN FRAME CRYPTO \_ \_ \_ \_ SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) che fornisce [**id3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) e le informazioni sulla chiave necessarie per decrittografare il frame.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-124">A pointer to a [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) providing the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) and the key information needed to decrypt the frame.</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e6e5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e6e5-125">Requirements</span></span>



| <span data-ttu-id="1e6e5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e6e5-126">Requirement</span></span> | <span data-ttu-id="1e6e5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1e6e5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6e5-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e6e5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1e6e5-129">Windows 10 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1e6e5-129">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e6e5-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e6e5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1e6e5-131">Solo app desktop di Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e6e5-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1e6e5-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e6e5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e6e5-133"><dt>D3d11.h</dt></span><span class="sxs-lookup"><span data-stu-id="1e6e5-133"><dt>D3d11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e6e5-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1e6e5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6e5-135">API video Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1e6e5-135">Direct3D 11 Video APIs</span></span>](direct3d-11-video-apis.md)
</dt> </dl>

 

 




