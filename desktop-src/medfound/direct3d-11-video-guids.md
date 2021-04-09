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
# <a name="direct3d-11-video-guids"></a>GUID video Direct3D 11

I GUID seguenti supportano le API video Direct3D 11.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_ \_ Protezione HW di scambio delle chiavi d3d11 \_ \_**
</dt> <dd> <dl> <dt>



Indica che il decodificatore riceverà i dati da un componente DRM basato su hardware

**D3d11 \_ Per indicare che l'interfaccia ID3D11CryptoSession verrà utilizzata esclusivamente per la comunicazione tra un componente DRM in modalità utente e l'ambiente di esecuzione protetta, è possibile specificare la \_ \_ \_ protezione HW di scambio delle chiavi** nel parametro *pKeyExchangeType* della funzione [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) . [](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)

Quando questo GUID viene specificato, non è necessario chiamare i metodi seguenti:

-   [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession:: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext::EncryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext::D ecryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext::StartSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext::FinishSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext::GetEncryptionBltKey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**\_Crittografia del decodificatore d3d11 \_ \_ HW \_ Cenc**
</dt> <dd> <dl> <dt>



Indica che il decodificatore riceverà i dati da un componente DRM basato su hardware

L'impostazione del GUID nel membro **guidConfigBitstreamEncryption** della struttura [**di \_ \_ \_ configurazione del decodificatore video d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) passata all'API [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indica che i parametri seguenti verranno passati nella chiamata ID3D11VideoDevice [**::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ContentKeySize* | Contiene le dimensioni della struttura [**della \_ sessione di \_ avvio della \_ \_ \_ crittografia \_ del decodificatore video d3d11**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .                                                                                                  |
| *pContentKey*    | Un puntatore a una [**\_ sessione d3d11 video \_ decoder \_ Begin \_ frame \_ Crypto \_**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) che fornisce il [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) e le informazioni chiave necessarie per decrittografare il frame. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API video Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




