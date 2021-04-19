---
description: I GUID della classe Terminal identificano un particolare terminale in base alle funzionalità.
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: Classe Terminal (Tapi3if. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d67d7668f9e4e16ad357408c8e9087fce870a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331768"
---
# <a name="terminal-class"></a>Classe Terminal

I GUID della classe Terminal identificano un particolare terminale in base alle funzionalità.

<dl> <dt>

<span id="CLSID_FilePlaybackTerminal"></span><span id="clsid_fileplaybackterminal"></span><span id="CLSID_FILEPLAYBACKTERMINAL"></span>**\_FILEPLAYBACKTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Terminale per la riproduzione di file.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTerminal"></span><span id="clsid_filerecordingterminal"></span><span id="CLSID_FILERECORDINGTERMINAL"></span>**\_FILERECORDINGTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Terminale per la registrazione di file.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTrack"></span><span id="clsid_filerecordingtrack"></span><span id="CLSID_FILERECORDINGTRACK"></span>**\_FILERECORDINGTRACK CLSID**
</dt> <dd> <dl> <dt>



Traccia di registrazione file.


</dt> </dl> </dd> <dt>

<span id="CLSID_HandsetTerminal"></span><span id="clsid_handsetterminal"></span><span id="CLSID_HANDSETTERMINAL"></span>**\_HANDSETTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Telefono cellulare.


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**\_HEADSETTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Set Head.


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**\_MEDIASTREAMTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Terminale del flusso multimediale, creato dinamicamente.


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**\_MICROPHONETERMINAL CLSID**
</dt> <dd> <dl> <dt>



Microfono.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**\_SPEAKERPHONETERMINAL CLSID**
</dt> <dd> <dl> <dt>



Telefono altoparlante.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**\_SPEAKERSTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Altoparlanti.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**\_VIDEOINPUTTERMINAL CLSID**
</dt> <dd> <dl> <dt>



Terminale di input video.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**\_VIDEOWINDOWTERM CLSID**
</dt> <dd> <dl> <dt>



Finestra di visualizzazione video, creata dinamicamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

La versione **BSTR** delle classi terminal è designata principalmente per l'utilizzo di applicazioni Visual Basic. Ad esempio, vengono restituiti come elementi della raccolta ottenuta con [**get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses).

-   Stringa CLSID \_ BSTR \_ HandsetTerminal
-   Stringa CLSID \_ BSTR \_ HeadsetTerminal
-   Stringa CLSID \_ BSTR \_ MediaStreamTerminal
-   Stringa CLSID \_ BSTR \_ MicrophoneTerminal
-   Stringa CLSID \_ BSTR \_ SpeakerphoneTerminal
-   Stringa CLSID \_ BSTR \_ SpeakersTerminal
-   Stringa CLSID \_ BSTR \_ VideoInputTerminal
-   Stringa CLSID \_ BSTR \_ VideoWindowTerm

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                |
| Intestazione<br/>       | <dl> <dt>Tapi3if. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**ITTerminal:: Get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**ITTerminalManager::CreateDynamicTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**ITTerminalManager::GetDynamicTerminalClasses**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**ITTerminalSupport::EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

