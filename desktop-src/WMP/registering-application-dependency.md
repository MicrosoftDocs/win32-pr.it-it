---
title: Registrazione delle dipendenze dell'applicazione (Windows Media Player SDK)
description: Registrazione delle dipendenze dell'applicazione
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player, impostazioni del registro di sistema di dipendenza dell'applicazione
- Windows Media Player, impostazioni del registro di sistema delle dipendenze
- Windows Media Player, registro di sistema
- Registro di sistema, impostazioni delle dipendenze dell'applicazione
- Registro di sistema, impostazioni di dipendenza
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema delle dipendenze
- impostazioni del registro di sistema delle dipendenze applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67aac78417f5ec8e4347b97a5c2b5f37db20183e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474986"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a>Registrazione delle dipendenze dell'applicazione (Windows Media Player SDK)

Le applicazioni che usano le API fornite da Windows Media Player SDK o Windows Media Format SDK dipendono dai componenti di runtime di tali tecnologie. È possibile registrare l'applicazione come dipendente da tali componenti come parte della configurazione dell'applicazione.

Quando si registra l'applicazione, è possibile scegliere uno dei due livelli di dipendenza: blocco o dipendente. Quando una o più applicazioni vengono registrate con una dipendenza di blocco su uno dei componenti di runtime, il componente verrà bloccato da un rollback a una versione precedente. Le applicazioni dipendenti non registrate come bloccanti non bloccano il rollback. Prima di eseguire il rollback, viene invece visualizzato un messaggio che informa che le applicazioni dipendono dal componente.

Per registrare l'applicazione, è necessario impostare un valore nel registro di sistema che identifichi l'applicazione. Il valore del registro di sistema da impostare dipende dal componente da cui dipende l'applicazione. È anche possibile impostare due valori aggiuntivi per dipendenza per fornire informazioni aggiuntive sull'applicazione.

I valori del registro di sistema seguenti vengono utilizzati per registrare la dipendenza dal runtime di Windows Media Player SDK:

-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ installazione \\ *ref \_ Type* \\ app, "*app*", "*\_ stringa app*"
-   HKEY \_ Classes \_ root \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ *ref \_ Type* \\ descrittor, "*app*", "*ref \_ descrittor*"
-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ configurazione \\ *\_ tipo di riferimento* \\ versione, "*app*",*" \_ versione WMP*"

I valori del registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime di Windows Media Format SDK:

-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ installazione \\ *ref \_ Type* \\ app, "*app*", "*\_ stringa app*"
-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ descriptor, "*app*", "*ref \_ descrittor*"
-   HKEY \_ Classes \_ root \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ Version, "*app*", "*WMF \_ Version*"

Nei valori del registro di sistema elencati sopra vengono usate le variabili seguenti:

*tipo di riferimento \_*

Sostituire con BlockingRefCounts per la dipendenza di blocco o con DependentRefCounts per la dipendenza non bloccante.

*APP*

Nome o breve descrittore dell'applicazione. Questa stringa non verrà utilizzata nei messaggi visualizzati per l'utente. Questo valore è l'identificatore utilizzato in tutti e tre i valori del registro di sistema associati a ognuno dei componenti Runtime.

*\_stringa app*

Descrittore dell'applicazione. Questa stringa può essere utilizzata nei messaggi visualizzati per l'utente.

*\_descrittore Ref*

Descrizione della modalità di utilizzo del componente da parte dell'applicazione. Questo valore può includere un massimo di 256 caratteri.

*versione di WMP \_*

Versione di Windows Media Player richiesta dall'applicazione. Se non viene specificata alcuna versione, viene utilizzato il valore predefinito 9.0.0.0.

*\_versione WMF*

Versione di Windows Media Format SDK richiesta dall'applicazione.

I tre valori di registro di esempio seguenti illustrano come configurare i valori per l'applicazione:

-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ app, "southridgevideo", "Southridge Video Player"
-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ descrittore, "southridgevideo", "Southridge Video Player usa Windows Media Format SDK per riprodurre file video".
-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Version, "southridgevideo", "9.0.0.2600"

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema**](registry-settings.md)
</dt> </dl>

 

 




