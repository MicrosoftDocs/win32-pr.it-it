---
description: Codici di errore specifici di XAudio2 restituiti dai metodi XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Codici di errore XAudio2 (Xaudio2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bbfb29153ca55064c1019e9cfb8fd1019caaa0ffe17dfa103f123faa812f762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545401"
---
# <a name="xaudio2-error-codes"></a>Codici di errore XAudio2

Codici di errore specifici di XAudio2 restituiti dai metodi XAudio2.



| Costante/valore                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <dt>**XAUDIO2 \_ E \_ INVALID \_ CALL**</dt> <dt>0x88960001</dt> </dl>                          | Restituito da XAudio2 per determinati errori di utilizzo dell'API (chiamate non valide e così via) difficili da evitare completamente e che devono essere gestiti da un titolo in fase di esecuzione. Gli errori di utilizzo dell'API completamente evitabili, ad esempio i parametri non validi, causano un'istruzione ASSERT nelle build di debug e un comportamento non definito nelle build di vendita al dettaglio, quindi non viene definito alcun codice di errore per tali build.<br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <dt>**XAUDIO2 \_ ERRORE \_ DEL \_ DECODIFICATORE \_ XMA**</dt> <dt>0x88960002</dt> </dl>          | Il Xbox 360 hardware XMA ha subito un errore irreversibile.<br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <dt>**XAUDIO2 \_ Creazione \_ di E XAPO \_ \_ non**</dt> <dt>riuscita 0x88960003</dt> </dl> | Impossibile creare un'istanza di un effetto.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <dt>**XAUDIO2 \_ E \_ DISPOSITIVO \_ INVALIDATO**</dt> <dt>0x88960004</dt> </dl>        | Un dispositivo audio è diventato inutilizzabile grazie alla scollegamento o a un altro evento.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Commenti

### <a name="platform-requirements"></a>Requisiti della piattaforma

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Xaudio2.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[XAudio2::Constants](constants.md)
</dt> </dl>

 

 




