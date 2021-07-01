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
# <a name="direct3d-11-video-guids"></a>GUID video Direct3D 11

I GUID seguenti supportano le API Video Direct3D 11.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**PROTEZIONE HW DELLO SCAMBIO DI \_ \_ \_ \_ CHIAVI D3D11**
</dt> <dd> <dl> <dt>



Indica che il decodificatore riceverà dati da un componente DRM basato su hardware

**D3D11 \_ KEY \_ EXCHANGE \_ HW \_ PROTECTION** può essere specificato nel *parametro pKeyExchangeType* della funzione [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) per indicare che l'interfaccia [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) verrà usata esclusivamente per la comunicazione tra un componente DRM in modalità utente e l'ambiente di esecuzione protetto.

Quando viene specificato questo GUID, non è necessario chiamare i metodi seguenti:

-   [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext::EncryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext::D ecryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext::StartSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext::FinishSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext::GetEncryptionBltKey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ DECODER \_ ENCRYPTION \_ HW \_ CENC**
</dt> <dd> <dl> <dt>



Indica che il decodificatore riceverà dati da un componente DRM basato su hardware

L'impostazione di questo GUID nel membro **guidConfigBitstreamEncryption** della struttura [**D3D11 \_ VIDEO \_ DECODER \_ CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) passata all'API [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indica che i parametri seguenti verranno passati nella chiamata [**ID3D11VideoDevice::D ecoderBeginFrame:**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)



| Valore                 | Descrizione                                                                                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ContentKeySize* | Contiene le dimensioni della struttura [**D3D11 \_ VIDEO \_ DECODER \_ BEGIN FRAME \_ \_ CRYPTO \_ SESSION.**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session)                                                                                                  |
| *pContentKey*    | Puntatore a [**un oggetto D3D11 \_ VIDEO \_ DECODER BEGIN FRAME CRYPTO \_ \_ \_ \_ SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) che fornisce [**id3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) e le informazioni sulla chiave necessarie per decrittografare il frame. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10 solo \[ app desktop\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2016 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>D3d11.h</dt> </dl> |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[API video Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




