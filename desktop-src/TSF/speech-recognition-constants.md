---
title: Costanti di riconoscimento vocale (Ctffunc. h)
description: Con il servizio di testo riconoscimento vocale vengono usati i valori seguenti.
ms.assetid: ac433d15-738a-46ab-8f69-0fbfb6a8b654
topic_type:
- apiref
api_name:
- TF_DICTATION_ON
- TF_DICTATION_ENABLED
- TF_COMMANDING_ENABLED
- TF_COMMANDING_ON
- TF_SPEECHUI_SHOWN
- TF_SHOW_BALLOON
- TF_DISABLE_BALLOON
- TF_DISABLE_SPEECH
- TF_DISABLE_DICTATION
- TF_DISABLE_COMMANDING
api_location:
- Ctffunc.h
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04c9cfd340e79415d12202765a8db1578abba74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119122"
---
# <a name="speech-recognition-constants"></a>Costanti di riconoscimento vocale

Con il servizio di testo riconoscimento vocale vengono usati i valori seguenti.



| Costante/valore                                                                                                                                                                                                                                         | Descrizione                                                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DICTATION_ON"></span><span id="tf_dictation_on"></span><dl> <dt>**Tf \_ DETTAtura \_ su**</dt> <dt>0x00000001</dt> </dl>                   | Se questo bit è 1, la dettatura vocale è attiva. In caso contrario, la dettatura vocale è inattiva. Questo valore non può essere combinato con \_ il comando tf \_ . Utilizzato con il compartimento [ \_ DICTATIONSTAT della \_ voce \_ del raggruppamento GUID](predefined-compartments.md) .<br/> |
| <span id="TF_DICTATION_ENABLED"></span><span id="tf_dictation_enabled"></span><dl> <dt>**Tf \_ 0x00000002 \_ abilitato per la dettatura**</dt> <dt></dt> </dl>    | Se questo bit è 1, la dettatura vocale è abilitata. In caso contrario, la dettatura vocale è disabilitata. Utilizzato con il compartimento [ \_ DICTATIONSTAT della \_ voce \_ del raggruppamento GUID](predefined-compartments.md) .<br/>                                                       |
| <span id="TF_COMMANDING_ENABLED"></span><span id="tf_commanding_enabled"></span><dl> <dt>**Tf \_ COMANDO 0x00000004 \_ abilitato**</dt> <dt></dt> </dl> | Se il bit è 1, il comando vocale è abilitato. In caso contrario, il comando vocale è disabilitato. Utilizzato con il compartimento [ \_ DICTATIONSTAT della \_ voce \_ del raggruppamento GUID](predefined-compartments.md) .<br/>                                                           |
| <span id="TF_COMMANDING_ON"></span><span id="tf_commanding_on"></span><dl> <dt>**Tf \_ COMANDO \_ su**</dt> <dt>0x00000008</dt> </dl>                | Se il bit è 1, il comando vocale è attivo. In caso contrario, il comando vocale è inattivo. Questo valore non può essere combinato con la \_ Dettatura di TF \_ su. Utilizzato con il compartimento [ \_ DICTATIONSTAT della \_ voce \_ del raggruppamento GUID](predefined-compartments.md) .<br/>      |
| <span id="TF_SPEECHUI_SHOWN"></span><span id="tf_speechui_shown"></span><dl> <dt>**Tf \_ SPEECHUI \_ mostrato**</dt> <dt>0x00000010</dt> </dl>             | Attualmente non utilizzato.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SHOW_BALLOON"></span><span id="tf_show_balloon"></span><dl> <dt>**Tf \_ Mostra \_**</dt> <dt>0x00000001</dt> Balloon </dl>                   | Attualmente non utilizzato. Usato con il raggruppamento di [ \_ \_ \_ \_ stato dell'interfaccia utente del raggruppamento GUID](predefined-compartments.md) .<br/>                                                                                                                              |
| <span id="TF_DISABLE_BALLOON"></span><span id="tf_disable_balloon"></span><dl> <dt>**Tf \_ DISABILITARE \_**</dt> <dt>0x00000002</dt> Balloon </dl>          | Se il bit è 1, la visualizzazione del fumetto per la modalità di riconoscimento vocale corrente è disabilitata. In caso contrario, la visualizzazione del fumetto per la modalità di riconoscimento vocale corrente è abilitata. Usato con il raggruppamento di [ \_ \_ \_ \_ stato dell'interfaccia utente del raggruppamento GUID](predefined-compartments.md) .<br/>    |
| <span id="TF_DISABLE_SPEECH"></span><span id="tf_disable_speech"></span><dl> <dt>**Tf \_ DISABILITARE \_**</dt> <dt>0x00000001</dt> vocale </dl>             | Se il bit è 1, l'input vocale è disabilitato. In caso contrario, l'input vocale è abilitato. Utilizzato con il compartimento della [ \_ voce del raggruppamento GUID \_ \_ disabilitato](predefined-compartments.md) .<br/>                                                                    |
| <span id="TF_DISABLE_DICTATION"></span><span id="tf_disable_dictation"></span><dl> <dt>**Tf \_ DISABILITARE la \_ Dettatura**</dt> <dt>0x00000002</dt> </dl>    | Se il bit è 1, la dettatura vocale è disabilitata. In caso contrario, la dettatura vocale è abilitata. Utilizzato con il compartimento della [ \_ voce del raggruppamento GUID \_ \_ disabilitato](predefined-compartments.md) .<br/>                                                            |
| <span id="TF_DISABLE_COMMANDING"></span><span id="tf_disable_commanding"></span><dl> <dt>**Tf \_ DISABILITARE i \_ comandi**</dt> <dt>0x00000004</dt> </dl> | Se il bit è 1, il comando vocale è disabilitato. In caso contrario, il comando vocale è abilitato. Utilizzato con il compartimento della [ \_ voce del raggruppamento GUID \_ \_ disabilitato](predefined-compartments.md) .<br/>                                                                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                    |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                                                                                         |
| Intestazione<br/>                   | <dl> <dt>Ctffunc. h; </dt> <dt>Msctf. h</dt> </dl>     |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl; </dt> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raggruppamenti predefiniti](predefined-compartments.md)
</dt> </dl>

 

 





