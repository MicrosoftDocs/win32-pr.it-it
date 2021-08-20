---
title: Registrazione della dipendenza dell'applicazione (Windows Media Format 11 SDK)
description: Informazioni su come registrare l'applicazione con i componenti di runtime delle API fornite da Windows Media Format 11 SDK.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, registrazione delle dipendenze dell'applicazione
- registrazione delle dipendenze dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc0d1e6c9c5583ea235c196c244d9969aec65128dc206720cfacc907ae0067b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845906"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>Registrazione della dipendenza dell'applicazione (Windows Media Format 11 SDK)

Le applicazioni che usano API fornite da Windows Media Format SDK o Windows Media Player SDK dipendono dai componenti di run-time di tali tecnologie. È possibile registrare l'applicazione come dipendente da tali componenti come parte della configurazione dell'applicazione.

Quando si registra l'applicazione, è possibile scegliere uno dei due livelli di dipendenza: blocco o dipendente. Quando una o più applicazioni vengono registrate con una dipendenza di blocco da uno dei componenti di run-time, il componente verrà bloccato da un rollback a una versione precedente. Le applicazioni dipendenti non registrate come bloccante non bloccano il rollback. Prima dell'esecuzione del rollback, all'utente viene invece visualizzato un messaggio che indica che le applicazioni dipendono dal componente.

Per registrare l'applicazione, è necessario impostare un valore nel Registro di sistema che identifica l'applicazione. Il valore del Registro di sistema da impostare dipende dal componente da cui dipende l'applicazione. È anche possibile impostare due valori aggiuntivi per ogni dipendenza per fornire informazioni aggiuntive sull'applicazione.

I valori del Registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime Windows Media Format SDK:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"

Il valore del Registro di sistema seguente viene usato per registrare la dipendenza dal runtime Windows Media Player SDK:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"

Nei valori del Registro di sistema elencati sopra vengono usate le variabili seguenti:

*TIPO \_ REF*

Sostituire con BlockingRefCounts per bloccare la dipendenza o con DependentRefCounts per la dipendenza non bloccante.

*APP*

Nome o descrittore breve dell'applicazione. Questa stringa non verrà usata nei messaggi visualizzati per l'utente. Questo valore è l'identificatore usato in tutti e tre i valori del Registro di sistema associati a ognuno dei componenti di run-time.

*STRINGA \_ APP*

Descrittore dell'applicazione. Questa stringa può essere usata nei messaggi visualizzati per l'utente.

*DESCRITTORE \_ REF*

Descrizione del modo in cui l'applicazione usa il componente. Questo valore può includere un massimo di 256 caratteri.

*VERSIONE \_ WMP*

La versione Windows Media Player richiesta dall'applicazione.

*VERSIONE DI \_ WMF*

Versione dell'WINDOWS Media Format SDK richiesto dall'applicazione.

I tre valori del Registro di sistema di esempio seguenti illustrano come configurare i valori per l'applicazione:

-   HKEY \_ CLASSES \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ App, "SouthridgeVideo", "Southridge Video Player"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files".
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Version, "SouthridgeVideo", "9.0.0.2600"

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Project Considerazioni**](project-considerations.md)
</dt> </dl>

 

 




