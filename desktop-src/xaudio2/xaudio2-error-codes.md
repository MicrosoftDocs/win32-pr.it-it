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
# <a name="xaudio2-error-codes"></a>Codici di errore XAudio2

XAudio2 codici di errore specifici restituiti dai metodi XAudio2.



| Costante/valore                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <dt>**XAUDIO2 \_ E \_ \_ chiamata 0x88960001 non valida**</dt> <dt></dt> </dl>                          | Restituito da XAudio2 per determinati errori di utilizzo dell'API (chiamate non valide e così via) difficili da evitare completamente e che devono essere gestiti da un titolo in fase di esecuzione. Gli errori di utilizzo delle API che sono completamente evitabili, ad esempio parametri non validi, provocano un'ASSERZIONe nelle compilazioni di debug e un comportamento non definito nelle compilazioni finali, quindi non viene definito alcun codice di errore.<br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <dt>**XAUDIO2 \_ \_ \_ \_ Errore del decodificatore E XMA**</dt> <dt>0x88960002</dt> </dl>          | Si è verificato un errore irreversibile nell'hardware XMA di Xbox 360.<br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <dt>**XAUDIO2 \_ Creazione di E \_ XAPO \_ \_ non riuscita**</dt> <dt>0x88960003</dt> </dl> | Non è stato possibile creare un'istanza di un effetto.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <dt>**XAUDIO2 \_ Dispositivo E 0x88960004 \_ \_ invalidato**</dt> <dt></dt> </dl>        | Un dispositivo audio è diventato inutilizzabile durante la scollegamento o un altro evento.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Commenti

### <a name="platform-requirements"></a>Requisiti della piattaforma

Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); DirectX SDK (XAudio 2,7)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[XAudio2:: Constants](constants.md)
</dt> </dl>

 

 




