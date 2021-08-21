---
description: La proprietà \_ PKEY AudioEngine DeviceFormat specifica il formato del dispositivo, ovvero il formato selezionato dall'utente per il flusso che passa tra il motore audio e il dispositivo endpoint audio quando il dispositivo opera in modalità \_ condivisa.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13245d23095c25173a894a7a4c7cc11b2cdc534f6ae7198508b725d0fd1cf0b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018329"
---
# <a name="pkey_audioengine_deviceformat"></a>PKEY \_ AudioEngine \_ DeviceFormat

La **proprietà \_ PKEY AudioEngine \_ DeviceFormat** specifica il formato del dispositivo, ovvero il formato selezionato dall'utente per il flusso che passa tra il motore audio e il dispositivo endpoint audio quando il dispositivo opera in modalità condivisa. Questo formato potrebbe non essere il formato predefinito migliore da usare per un'applicazione in modalità esclusiva. In genere, un'applicazione in modalità esclusiva trova un formato di dispositivo appropriato effettuando alcune chiamate al metodo [**IAudioClient::IsFormatSupported.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) Per altre informazioni, vedere [Formati di dispositivo](device-formats.md).

Il **membro vt** della **struttura PROPVARIANT** è impostato su BLOB VT. \_

Il **membro BLOB** della struttura **PROPVARIANT** è una struttura di tipo **BLOB** che contiene due membri. Member **blob.cbSize** è un **valore DWORD** che specifica il numero di byte nella descrizione del formato. Il **membro blob.pBlobData** punta a una **struttura WAVEFORMATEX** che contiene la descrizione del formato. Per altre informazioni su **BLOB,** vedere la documentazione Windows SDK. Per altre informazioni su **WAVEFORMATEX,** vedere la documentazione Windows DDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà dell'endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio di base](core-audio-properties.md)
</dt> </dl>

 

 




