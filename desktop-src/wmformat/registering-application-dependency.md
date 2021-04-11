---
title: Registrazione delle dipendenze dell'applicazione (Windows Media Format 11 SDK)
description: Registrazione delle dipendenze dell'applicazione
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, registrazione delle dipendenze dell'applicazione
- registrazione delle dipendenze dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047670"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>Registrazione delle dipendenze dell'applicazione (Windows Media Format 11 SDK)

Le applicazioni che usano le API fornite da Windows Media Format SDK o Windows Media Player SDK dipendono dai componenti di runtime di tali tecnologie. È possibile registrare l'applicazione come dipendente da tali componenti come parte della configurazione dell'applicazione.

Quando si registra l'applicazione, è possibile scegliere uno dei due livelli di dipendenza: blocco o dipendente. Quando una o più applicazioni vengono registrate con una dipendenza di blocco da uno dei componenti di runtime, il componente verrà bloccato da un rollback a una versione precedente. Le applicazioni dipendenti che non sono registrate come bloccanti non bloccano il rollback. Al contrario, prima che venga eseguito il rollback, all'utente viene richiesto di specificare un messaggio che informa che le applicazioni dipendono dal componente.

Per registrare l'applicazione, è necessario impostare un valore nel registro di sistema che identifichi l'applicazione. Il valore del registro di sistema da impostare dipende dal componente da cui dipende l'applicazione. È anche possibile impostare due valori aggiuntivi per dipendenza per fornire informazioni aggiuntive sull'applicazione.

I valori del registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime di Windows Media Format SDK:

-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ installazione \\ *ref \_ Type* \\ app, "*app*", "*\_ stringa app*"
-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ descriptor, "*app*", "*ref \_ descrittor*"
-   HKEY \_ Classes \_ root \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ Version, "*app*", "*WMF \_ Version*"

Il valore del registro di sistema seguente viene usato per registrare la dipendenza dal runtime di Windows Media Player SDK:

-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ installazione \\ *ref \_ Type* \\ app, "*app*", "*\_ stringa app*"
-   HKEY \_ Classes \_ root \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ *ref \_ Type* \\ descrittor, "*app*", "*ref \_ descrittor*"
-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ configurazione \\ *\_ tipo di riferimento* \\ versione, "*app*",*" \_ versione WMP*"

Nei valori del registro di sistema elencati sopra vengono usate le variabili seguenti:

*tipo di riferimento \_*

Sostituire con BlockingRefCounts per la dipendenza di blocco o con DependentRefCounts per la dipendenza non bloccante.

*APP*

Nome o breve descrittore dell'applicazione. Questa stringa non verrà utilizzata nei messaggi visualizzati per l'utente. Questo valore è l'identificatore utilizzato in tutti e tre i valori del registro di sistema associati a ognuno dei componenti di run-time.

*\_stringa app*

Descrittore dell'applicazione. Questa stringa può essere utilizzata nei messaggi visualizzati per l'utente.

*\_descrittore Ref*

Descrizione della modalità di utilizzo del componente da parte dell'applicazione. Questo valore può includere un massimo di 256 caratteri.

*versione di WMP \_*

Versione di Windows Media Player richiesta dall'applicazione.

*\_versione WMF*

Versione di Windows Media Format SDK richiesta dall'applicazione.

I tre valori di registro di esempio seguenti illustrano come configurare i valori per l'applicazione:

-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ app, "southridgevideo", "Southridge Video Player"
-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ descrittore, "southridgevideo", "Southridge Video Player usa Windows Media Format SDK per riprodurre file video".
-   HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ Version, "southridgevideo", "9.0.0.2600"

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Considerazioni sui progetti**](project-considerations.md)
</dt> </dl>

 

 




