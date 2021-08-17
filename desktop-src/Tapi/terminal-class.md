---
description: I GUID della classe terminale identificano un terminale specifico in base alle funzionalità.
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: Classe Terminal (Tapi3if.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd20d3e540529b343d1fb848b9e8cb2579a621b40146e0d170fdb175c4c9a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975451"
---
# <a name="terminal-class"></a>Classe terminale

I GUID della classe terminale identificano un terminale specifico in base alle funzionalità.

<dl> <dt>

<span id="CLSID_FilePlaybackTerminal"></span><span id="clsid_fileplaybackterminal"></span><span id="CLSID_FILEPLAYBACKTERMINAL"></span>**File \_ CLSIDPlaybackTerminal**
</dt> <dd> <dl> <dt>



Terminale di riproduzione file.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTerminal"></span><span id="clsid_filerecordingterminal"></span><span id="CLSID_FILERECORDINGTERMINAL"></span>**File \_ CLSIDRecordingTerminal**
</dt> <dd> <dl> <dt>



Terminale di registrazione file.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTrack"></span><span id="clsid_filerecordingtrack"></span><span id="CLSID_FILERECORDINGTRACK"></span>**File \_ CLSIDRecordingTrack**
</dt> <dd> <dl> <dt>



Traccia di registrazione file.


</dt> </dl> </dd> <dt>

<span id="CLSID_HandsetTerminal"></span><span id="clsid_handsetterminal"></span><span id="CLSID_HANDSETTERMINAL"></span>**Ricevitore \_ CLSIDTerminal**
</dt> <dd> <dl> <dt>



Cornetta.


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**Visore \_ CLSIDTerminal**
</dt> <dd> <dl> <dt>



Set di testina.


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**CLSID \_ MediaStreamTerminal**
</dt> <dd> <dl> <dt>



Terminale del flusso multimediale, creato dinamicamente.


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**Microfono \_ CLSIDTerminale**
</dt> <dd> <dl> <dt>



Microfono.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**Voce CLSID \_ SpeakerphoneTerminal**
</dt> <dd> <dl> <dt>



Telefono del parlante.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**Altoparlanti \_ CLSIDTerminal**
</dt> <dd> <dl> <dt>



Altoparlanti.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**CLSID \_ VideoInputTerminal**
</dt> <dd> <dl> <dt>



Terminale di input video.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**Video \_ CLSIDWindowTerm**
</dt> <dd> <dl> <dt>



Finestra di visualizzazione video, creata dinamicamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

La **versione BSTR** delle classi terminale è principalmente designata per l'uso di Visual Basic applicazioni. Ad esempio, vengono restituiti come elementi della raccolta ottenuta con [**get \_ DynamicTerminalClasses.**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)

-   Stringa CLSID BSTR \_ \_ HandsetTerminal
-   Stringa CLSID BSTR \_ \_ HeadsetTerminal
-   Stringa CLSID BSTR \_ \_ MediaStreamTerminal
-   BSTR CLSID \_ String \_ MicrophoneTerminal
-   Stringa CLSID BSTR \_ \_ SpeakerphoneTerminal
-   BSTR CLSID \_ String \_ SpeakersTerminal
-   Stringa CLSID BSTR \_ \_ VideoInputTerminal
-   Stringa CLSID BSTR \_ \_ VideoWindowTerm

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                |
| Intestazione<br/>       | <dl> <dt>Tapi3if.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**ITTerminal::get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**ITTerminalManager::CreateDynamicTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**ITTerminalManager::GetDynamicTerminalClasses**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**ITTerminalSupport::EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

