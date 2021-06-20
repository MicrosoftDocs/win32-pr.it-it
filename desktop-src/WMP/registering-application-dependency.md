---
title: Registrazione della dipendenza dell'applicazione (Windows Media Player SDK)
description: Informazioni su come registrare l'applicazione con i componenti di runtime delle API fornite da Windows Media Player SDK.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player,impostazioni del Registro di sistema delle dipendenze dell'applicazione
- Windows Media Player,impostazioni del Registro di sistema delle dipendenze
- Windows Media Player,registro
- registro, impostazioni delle dipendenze dell'applicazione
- registro, impostazioni delle dipendenze
- registro, impostazioni per Windows Media Player
- impostazioni del Registro di sistema delle dipendenze
- impostazioni del Registro di sistema delle dipendenze dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b1692c6a4e1a8274472bbe9d718721c1ab4f1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407364"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a>Registrazione della dipendenza dell'applicazione (Windows Media Player SDK)

Le applicazioni che usano API fornite da Windows Media Player SDK o Windows Media Format SDK dipendono dai componenti di runtime di tali tecnologie. È possibile registrare l'applicazione come dipendente da tali componenti come parte della configurazione dell'applicazione.

Quando si registra l'applicazione, è possibile scegliere uno dei due livelli di dipendenza: blocco o dipendente. Quando una o più applicazioni vengono registrate con una dipendenza di blocco da uno dei componenti di runtime, il componente verrà bloccato da un rollback a una versione precedente. Le applicazioni dipendenti non registrate come bloccante non bloccano il rollback. Al contrario, prima che venga eseguito il rollback, all'utente viene visualizzato un messaggio che indica che le applicazioni dipendono dal componente.

Per registrare l'applicazione, è necessario impostare un valore nel Registro di sistema che identifica l'applicazione. Il valore del Registro di sistema da impostare dipende dal componente da cui dipende l'applicazione. È anche possibile impostare due valori aggiuntivi per ogni dipendenza per fornire informazioni aggiuntive sull'applicazione.

I valori del Registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime Windows Media Player SDK:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"

I valori del Registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime di Windows Media Format SDK:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"

Nei valori del Registro di sistema elencati in precedenza vengono usate le variabili seguenti:

*TIPO \_ REF*

Sostituire con BlockingRefCounts per bloccare la dipendenza o con DependentRefCounts per la dipendenza non bloccante.

*APP*

Nome o breve descrittore dell'applicazione. Questa stringa non verrà usata nei messaggi visualizzati per l'utente. Questo valore è l'identificatore usato in tutti e tre i valori del Registro di sistema associati a ognuno dei componenti di runtime.

*STRINGA \_ APP*

Descrittore dell'applicazione. Questa stringa può essere usata nei messaggi visualizzati per l'utente.

*DESCRITTORE \_ REF*

Descrizione del modo in cui l'applicazione usa il componente. Questo valore può includere un massimo di 256 caratteri.

*VERSIONE \_ WMP*

La versione Windows Media Player richiesta dall'applicazione. Se non viene specificata alcuna versione, si presuppone che il valore predefinito sia 9.0.0.0.

*VERSIONE DI \_ WMF*

Versione di Windows Media Format SDK richiesta dall'applicazione.

I tre valori del Registro di sistema di esempio seguenti illustrano come configurare i valori per l'applicazione:

-   HKEY \_ CLASSES \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ App, "SouthridgeVideo", "Southridge Video Player"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files".
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Version, "SouthridgeVideo", "9.0.0.2600"

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del Registro di sistema**](registry-settings.md)
</dt> </dl>

 

 




