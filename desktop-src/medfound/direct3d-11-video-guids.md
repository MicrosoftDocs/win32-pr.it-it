---
description: I GUID seguenti supportano le API video Direct3D 11.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUID video Direct3D 11 (d3d11. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d97a43285a59cf5196584b9be04fc36b02e5243f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049311"
---
# <a name="direct3d-11-video-guids"></a><span data-ttu-id="a1526-103">GUID video Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a1526-103">Direct3D 11 Video GUIDs</span></span>

<span data-ttu-id="a1526-104">I GUID seguenti supportano le API video Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="a1526-104">The following GUIDs support Direct3D 11 Video APIs.</span></span>

<dl> <dt>

<span data-ttu-id="a1526-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_ \_ Protezione HW di scambio delle chiavi d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a1526-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a1526-106">Indica che il decodificatore riceverà i dati da un componente DRM basato su hardware</span><span class="sxs-lookup"><span data-stu-id="a1526-106">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="a1526-107">**D3d11 \_ Per indicare che l'interfaccia ID3D11CryptoSession verrà utilizzata esclusivamente per la comunicazione tra un componente DRM in modalità utente e l'ambiente di esecuzione protetta, è possibile specificare la \_ \_ \_ protezione HW di scambio delle chiavi** nel parametro *pKeyExchangeType* della funzione [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) . [](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)</span><span class="sxs-lookup"><span data-stu-id="a1526-107">**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION** can be specified in the *pKeyExchangeType* parameter of the [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) function to indicate that the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) interface will be used purely for communication between a user mode DRM component and the secure execution environment.</span></span>

<span data-ttu-id="a1526-108">Quando questo GUID viene specificato, non è necessario chiamare i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1526-108">When this GUID is specified, the following methods should not be called:</span></span>

-   [<span data-ttu-id="a1526-109">**ID3D11CryptoSession::GetCertificateSize**</span><span class="sxs-lookup"><span data-stu-id="a1526-109">**ID3D11CryptoSession::GetCertificateSize**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [<span data-ttu-id="a1526-110">**ID3D11CryptoSession:: GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="a1526-110">**ID3D11CryptoSession::GetCertificate**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [<span data-ttu-id="a1526-111">**ID3D11VideoContext::EncryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="a1526-111">**ID3D11VideoContext::EncryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [<span data-ttu-id="a1526-112">**ID3D11VideoContext::D ecryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="a1526-112">**ID3D11VideoContext::DecryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [<span data-ttu-id="a1526-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="a1526-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [<span data-ttu-id="a1526-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="a1526-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [<span data-ttu-id="a1526-115">**ID3D11VideoContext::GetEncryptionBltKey**</span><span class="sxs-lookup"><span data-stu-id="a1526-115">**ID3D11VideoContext::GetEncryptionBltKey**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span data-ttu-id="a1526-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**\_Crittografia del decodificatore d3d11 \_ \_ HW \_ Cenc**</span><span class="sxs-lookup"><span data-stu-id="a1526-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11\_DECODER\_ENCRYPTION\_HW\_CENC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a1526-117">Indica che il decodificatore riceverà i dati da un componente DRM basato su hardware</span><span class="sxs-lookup"><span data-stu-id="a1526-117">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="a1526-118">L'impostazione del GUID nel membro **guidConfigBitstreamEncryption** della struttura [**di \_ \_ \_ configurazione del decodificatore video d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) passata all'API [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indica che i parametri seguenti verranno passati nella chiamata ID3D11VideoDevice [**::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :</span><span class="sxs-lookup"><span data-stu-id="a1526-118">Setting this GUID in the **guidConfigBitstreamEncryption** member of the [**D3D11\_VIDEO\_DECODER\_CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) structure passed to the [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API indicates that the following parameters will be passed in the [**ID3D11VideoDevice::DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) call:</span></span>



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1526-119">*ContentKeySize*</span><span class="sxs-lookup"><span data-stu-id="a1526-119">*ContentKeySize*</span></span> | <span data-ttu-id="a1526-120">Contiene le dimensioni della struttura [**della \_ sessione di \_ avvio della \_ \_ \_ crittografia \_ del decodificatore video d3d11**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .</span><span class="sxs-lookup"><span data-stu-id="a1526-120">Contains the size of the [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) structure.</span></span>                                                                                                  |
| <span data-ttu-id="a1526-121">*pContentKey*</span><span class="sxs-lookup"><span data-stu-id="a1526-121">*pContentKey*</span></span>    | <span data-ttu-id="a1526-122">Un puntatore a una [**\_ sessione d3d11 video \_ decoder \_ Begin \_ frame \_ Crypto \_**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) che fornisce il [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) e le informazioni chiave necessarie per decrittografare il frame.</span><span class="sxs-lookup"><span data-stu-id="a1526-122">A pointer to a [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) providing the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) and the key information needed to decrypt the frame.</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1526-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1526-123">Requirements</span></span>



| <span data-ttu-id="a1526-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1526-124">Requirement</span></span> | <span data-ttu-id="a1526-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a1526-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1526-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1526-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a1526-127">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a1526-127">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1526-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1526-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a1526-129">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="a1526-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a1526-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1526-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1526-131"><dt>D3d11. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1526-131"><dt>D3d11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1526-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1526-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1526-133">API video Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a1526-133">Direct3D 11 Video APIs</span></span>](direct3d-11-video-apis.md)
</dt> </dl>

 

 




