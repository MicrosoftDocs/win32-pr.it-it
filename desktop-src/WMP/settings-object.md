---
title: Oggetto Settings (Windows Media Player SDK)
description: L'oggetto Settings fornisce un modo per modificare diverse impostazioni di Windows Media Player usando le proprietà e i metodi seguenti.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Finestra oggetti Impostazioni Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "103857741"
---
# <a name="settings-object"></a>Oggetto Settings

L'oggetto **Settings** fornisce un modo per modificare diverse impostazioni di Windows Media Player usando le proprietà e i metodi seguenti.

L'oggetto **Settings** supporta le proprietà seguenti.



| Proprietà                                                  | Descrizione                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Avvio automatico](settings-autostart.md)                       | Specifica o recupera un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.                           |
| [bilanciare](settings-balance.md)                           | Specifica o Recupera il saldo stereo corrente.                                                                               |
| [baseURL](settings-baseurl.md)                           | Specifica o recupera l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati nei file multimediali. |
| [defaultAudioLanguage](settings-defaultaudiolanguage.md) | Recupera l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita specificata in Windows Media Player.                          |
| [defaultFrame](settings-defaultframe.md)                 | Specifica o Recupera il nome del fotogramma utilizzato per visualizzare un URL ricevuto in un evento **ScriptCommand** .                |
| [enableErrorDialogs](settings-enableerrordialogs.md)     | Specifica o recupera un valore che indica se le finestre di dialogo di errore vengono visualizzate automaticamente.                                    |
| [invokeURLs](settings-invokeurls.md)                     | Specifica o recupera un valore che indica se gli eventi URL devono avviare un Web browser.                                        |
| [isAvailable](settings-isavailable.md)                   | Recupera un valore che indica se è disponibile un tipo di informazioni specificato oppure se è possibile eseguire un'azione specificata.                           |
| [mediaAccessRights](settings-mediaaccessrights.md)       | Recupera un valore che indica i diritti attualmente concessi per l'accesso alla libreria.                                                    |
| [mute](settings-mute.md)                                 | Specifica o recupera un valore che indica se l'audio è disattivato.                                                                |
| [playCount](settings-playcount.md)                       | Specifica o Recupera il numero di volte in cui un elemento multimediale viene riprodotto.                                                               |
| [tasso](settings-rate.md)                                 | Specifica o recupera la frequenza di riproduzione corrente.                                                                                |
| [volume](settings-volume.md)                             | Specifica o Recupera il volume corrente.                                                                                       |



 

L'oggetto **Settings** supporta i metodi seguenti:



| Metodo                                                            | Descrizione                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [getMode](settings-getmode.md)                                   | Determina se la modalità ciclo o shuffle è attiva. |
| [requestMediaAccessRights](settings-requestmediaaccessrights.md) | Richiede un livello specificato di accesso alla libreria.        |
| [setMode](settings-setmode.md)                                   | Imposta la modalità ciclo o shuffle su attivo o inattivo.   |



 

È possibile accedere all'oggetto **Settings** tramite la proprietà seguente.



| Oggetto                      | Proprietà                        |
|-----------------------------|---------------------------------|
| [Player](player-object.md) | [impostazioni](player-settings.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




