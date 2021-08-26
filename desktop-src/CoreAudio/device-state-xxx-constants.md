---
description: Le costanti DEVICE \_ STATE XXX indicano lo stato corrente di un dispositivo endpoint \_ audio.
ms.assetid: d03f2fbc-313a-42cf-902a-fd9f6dce2a35
title: DEVICE_STATE_XXX costanti (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d5632f14ff52fec2aa907dc2786f2a3ab893f921cd44433548510163f66a1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053871"
---
# <a name="device_state_xxx-constants"></a>Costanti \_ DEVICE STATE \_ XXX

Le costanti DEVICE \_ STATE XXX indicano lo stato corrente di un dispositivo endpoint \_ audio.



| Costante/valore                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <dt>**DISPOSITIVO \_ STATE \_ ACTIVE**</dt> <dt>0x00000001</dt> </dl>             | Il dispositivo endpoint audio è attivo. In altri modo, la scheda audio che si connette al dispositivo endpoint è presente e abilitata. Inoltre, se il dispositivo endpoint si collega a un jack sull'adattatore, il dispositivo endpoint è collegato.<br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <dt>**DISPOSITIVO \_ STATO \_ DISABILITATO**</dt> <dt>0x00000002</dt> </dl>       | Il dispositivo endpoint audio è disabilitato. L'utente ha disabilitato il dispositivo nel pannello Windows di controllo multimediale, Mmsys.cpl. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <dt>**DISPOSITIVO \_ STATE \_ NOTPRESENT**</dt> <dt>0x00000004</dt> </dl> | Il dispositivo endpoint audio non è presente perché la scheda audio che si connette al dispositivo endpoint è stata rimossa dal sistema o l'utente ha disabilitato il dispositivo adapter in Gestione dispositivi.<br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <dt>**DISPOSITIVO \_ STATE \_ UNPLUGGED**</dt> <dt>0x00000008</dt> </dl>    | Il dispositivo endpoint audio è scollegato. La scheda audio che contiene il jack per il dispositivo endpoint è presente e abilitata, ma il dispositivo endpoint non è collegato al jack. Solo un dispositivo con rilevamento della presenza jack può essere in questo stato. Per altre informazioni sul rilevamento della presenza jack, vedere [Dispositivi endpoint audio](audio-endpoint-devices.md).<br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <dt>**DISPOSITIVO \_ STATEMASK \_ ALL**</dt> <dt>0x0000000F</dt> </dl>          | Include i dispositivi endpoint audio in tutti gli stati attivi, disabilitati, non presenti e scollegati.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Commenti

I metodi [**IMMDeviceEnumerator::EnumAudioEndpoints,**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) [**IMMDevice::GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)e [**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged) usano le costanti DEVICE \_ STATE \_ XXX. Questi metodi consentono ai client di ottenere informazioni sui dispositivi endpoint presenti in uno degli stati rappresentati dalle costanti DEVICE \_ STATE \_ XXX.

Tuttavia, un client può aprire un flusso (ad esempio, ottenendo [**un'interfaccia IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) per il dispositivo) solo in un dispositivo che si trova nello stato DEVICE \_ STATE \_ ACTIVE.

Il Windows di controllo multimediale, Mmsys.cpl, visualizza i dispositivi endpoint audio nel sistema. La disabilitazione di un dispositivo in Mmsys.cpl nasconde il dispositivo dai meccanismi di individuazione dei dispositivi nelle API audio di livello superiore, ma non invalida gli oggetti flusso di cui un client potrebbe aver creato un'istanza prima della disabilitazione del dispositivo. Ad esempio, se un flusso viene riprodotto nel dispositivo quando l'utente lo Mmsys.cpl, il flusso continua a essere riprodotto ininterrottamente.

Al contrario, la disabilitazione di un dispositivo in Gestione dispositivi rimuove in modo efficace il dispositivo dal sistema.

Per usare Mmsys.cpl per visualizzare i dispositivi di rendering, aprire una finestra del prompt dei comandi e immettere il comando seguente:

**controllo mmsys.cpl,0**

Per visualizzare i dispositivi di acquisizione, immettere il comando seguente:

**controllo mmsys.cpl,,1**

In alternativa, è possibile visualizzare i dispositivi di rendering o i dispositivi di acquisizione in Mmsys.cpl facendo clic con il pulsante  destro del mouse sull'icona del parlante nell'area di notifica, che si trova sul lato destro della barra delle applicazioni, e selezionando Dispositivi di riproduzione o Dispositivi di registrazione **.**

Mmsys.cpl visualizza sempre i dispositivi endpoint nello stato \_ DEVICE STATE \_ ACTIVE. Inoltre, può essere configurato per visualizzare i dispositivi disabilitati e disconnessi.

Per visualizzare i dispositivi endpoint negli stati DEVICE STATE DISABLED e DEVICE STATE NOTPRESENT, fare clic con il pulsante destro del mouse nella finestra Mmsys.cpl e selezionare l'opzione \_ \_ Mostra \_ \_ **dispositivi** disabilitati.

Per visualizzare i dispositivi endpoint nello stato DEVICE \_ STATE \_ UNPLUGGED, fare clic con  il pulsante destro del mouse nella finestra Mmsys.cpl e selezionare l'opzione Mostra dispositivi disconnessi.

Per visualizzare solo i dispositivi endpoint nello stato DEVICE STATE ACTIVE, deselezionare entrambe le opzioni Mostra dispositivi disabilitati e Mostra \_ \_ dispositivi **disconnessi.** 

Per abilitare o disabilitare un dispositivo endpoint in Mmsys.cpl, fare clic su **Riproduzione** o **Registrazione,** a seconda che il dispositivo sia un dispositivo di riproduzione o di registrazione. Selezionare quindi il dispositivo e fare clic su **Proprietà**. Nella finestra **Proprietà,** accanto a **Utilizzo del** dispositivo, selezionare Usa questo dispositivo **(abilita)** o Non usare questo **dispositivo (disabilita).**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti audio di base](core-audio-constants.md)
</dt> <dt>

[**IMMDevice::GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[**Interfaccia IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 




