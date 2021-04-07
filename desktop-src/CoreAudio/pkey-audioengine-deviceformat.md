---
description: La \_ Proprietà pkey Audioengine \_ DeviceFormat specifica il formato del dispositivo, che è il formato selezionato dall'utente per il flusso che scorre tra il motore audio e il dispositivo dell'endpoint audio quando il dispositivo funziona in modalità condivisa.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748903"
---
# <a name="pkey_audioengine_deviceformat"></a>PKEY \_ Audioengine \_ DeviceFormat

La proprietà **pkey \_ Audioengine \_ DeviceFormat** specifica il formato del dispositivo, che è il formato selezionato dall'utente per il flusso che scorre tra il motore audio e il dispositivo dell'endpoint audio quando il dispositivo funziona in modalità condivisa. Questo formato potrebbe non essere il formato predefinito migliore per l'uso da parte di un'applicazione in modalità esclusiva. In genere, un'applicazione in modalità esclusiva trova un formato di dispositivo appropriato effettuando un certo numero di chiamate al metodo [**IAudioClient:: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) . Per altre informazioni, vedere [formati di dispositivo](device-formats.md).

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ BLOB.

Il membro **BLOB** della struttura **PROPVARIANT** è una struttura di tipo **BLOB** che contiene due membri. Member **BLOB. cbSize** è un **valore DWORD** che specifica il numero di byte nella descrizione del formato. Il membro **BLOB. pBlobData** punta a una struttura **WAVEFORMATEX** che contiene la descrizione del formato. Per ulteriori informazioni su **BLOB**, vedere la documentazione Windows SDK. Per ulteriori informazioni su **WAVEFORMATEX**, vedere la documentazione di Windows DDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




