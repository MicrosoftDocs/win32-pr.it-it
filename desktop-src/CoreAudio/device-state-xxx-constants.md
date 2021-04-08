---
description: Le \_ costanti xxx dello stato del dispositivo \_ indicano lo stato corrente di un dispositivo endpoint audio.
ms.assetid: d03f2fbc-313a-42cf-902a-fd9f6dce2a35
title: Costanti DEVICE_STATE_XXX (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65fc09a547ad702d27e96e968915f9d70e3313e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747759"
---
# <a name="device_state_xxx-constants"></a>\_Costanti xxx dello stato del dispositivo \_

Le \_ costanti xxx dello stato del dispositivo \_ indicano lo stato corrente di un dispositivo endpoint audio.



| Costante/valore                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <dt>**Dispositivo \_ STATO \_**</dt> <dt>0x00000001</dt> attivo </dl>             | Il dispositivo dell'endpoint audio è attivo. Ovvero la scheda audio che si connette al dispositivo endpoint è presente e abilitata. Inoltre, se il dispositivo dell'endpoint si connette a un jack sulla scheda, il dispositivo dell'endpoint viene collegato.<br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <dt>**Dispositivo \_ STATO \_ disabilitato**</dt> <dt>0x00000002</dt> </dl>       | Il dispositivo dell'endpoint audio è disabilitato. L'utente ha disabilitato il dispositivo nel pannello di controllo multimediale di Windows Mmsys.cpl. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <dt>**Dispositivo \_ STATO \_ NOTPRESENT**</dt> <dt>0x00000004</dt> </dl> | Il dispositivo dell'endpoint audio non è presente perché la scheda audio che si connette al dispositivo dell'endpoint è stata rimossa dal sistema o l'utente ha disabilitato il dispositivo adapter in Gestione dispositivi.<br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <dt>**Dispositivo \_ STATO \_ scollegato**</dt> <dt>0x00000008</dt> </dl>    | Il dispositivo dell'endpoint audio viene scollegato. La scheda audio che contiene la presa per il dispositivo endpoint è presente e abilitata, ma il dispositivo endpoint non è collegato al Jack. In questo stato è possibile usare solo un dispositivo con rilevamento della presenza Jack. Per altre informazioni sul rilevamento della presenza di Jack, vedere [dispositivi endpoint audio](audio-endpoint-devices.md).<br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <dt>**Dispositivo \_ STATEMASK \_ tutti**</dt> <dt>0x0000000F</dt> </dl>          | Include i dispositivi endpoint audio in tutti gli Stati attivi, disabilitati, non presenti e scollegati.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Commenti

I metodi [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints), [**IMMDevice:: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)e [**IMMNotificationClient:: OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged) usano le \_ costanti xxx dello stato del dispositivo \_ . Questi metodi consentono ai client di ottenere informazioni sui dispositivi endpoint che si trovano in uno degli Stati rappresentati dalle \_ costanti xxx dello stato del dispositivo \_ .

Tuttavia, un client può aprire un flusso, ad esempio ottenendo un'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) per il dispositivo, solo in un dispositivo che si trova nello \_ stato attivo dello stato del dispositivo \_ .

Il pannello di controllo multimediale di Windows, Mmsys.cpl, Visualizza i dispositivi dell'endpoint audio nel sistema. La disabilitazione di un dispositivo in Mmsys.cpl nasconde il dispositivo dai meccanismi di individuazione dei dispositivi nelle API audio di livello superiore, ma non invalida gli oggetti di flusso di cui un client potrebbe avere creato un'istanza prima che il dispositivo venisse disabilitato. Se, ad esempio, un flusso viene riprodotto sul dispositivo quando l'utente lo Disabilita in Mmsys.cpl, il flusso continua a essere riprodotto senza interruzioni.

Al contrario, la disabilitazione di un dispositivo in Gestione dispositivi rimuove efficacemente il dispositivo dal sistema.

Per usare Mmsys.cpl per visualizzare i dispositivi di rendering, aprire una finestra del prompt dei comandi e immettere il comando seguente:

**controllo mmsys.cpl,, 0**

Per visualizzare i dispositivi di acquisizione, immettere il comando seguente:

**controllo mmsys.cpl,, 1**

In alternativa, è possibile visualizzare i dispositivi di rendering o i dispositivi di acquisizione in Mmsys.cpl facendo clic con il pulsante destro del mouse sull'icona dell'altoparlante nell'area di notifica che si trova sul lato destro della barra delle applicazioni e scegliendo **dispositivi di riproduzione** o **registrazione dispositivi**.

Mmsys.cpl Visualizza sempre i dispositivi endpoint che si trovano nello \_ stato attivo dello stato del dispositivo \_ . Inoltre, può essere configurato per visualizzare dispositivi disabilitati e disconnessi.

Per visualizzare i dispositivi endpoint che si trovano nello \_ stato del dispositivo \_ disabilitato e \_ lo stato del dispositivo \_ NOTPRESENT Stati, fare clic con il pulsante destro del mouse nella finestra Mmsys.cpl e selezionare l'opzione **Mostra dispositivi disabilitati** .

Per visualizzare i dispositivi endpoint che si trovano nello \_ stato del dispositivo \_ scollegato, fare clic con il pulsante destro del mouse nella finestra Mmsys.cpl e selezionare l'opzione **Mostra dispositivi disconnessi** .

Per visualizzare solo i dispositivi endpoint che si trovano nello \_ stato attivo dello stato del dispositivo \_ , deselezionare entrambe le opzioni **Mostra dispositivi disabilitati** e **Mostra dispositivi disconnessi** .

Per abilitare o disabilitare un dispositivo endpoint in Mmsys.cpl, fare clic su **riproduzione** o **registrazione**, a seconda che il dispositivo sia una riproduzione o un dispositivo di registrazione. Selezionare quindi il dispositivo e fare clic su **Proprietà**. Nella finestra **Proprietà** accanto a **utilizzo dispositivo** Selezionare **Usa questo dispositivo (Abilita)** o **non usare questo dispositivo (Disabilita)**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti audio Core](core-audio-constants.md)
</dt> <dt>

[**IMMDevice:: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[**Interfaccia IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 




