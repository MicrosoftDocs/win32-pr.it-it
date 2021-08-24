---
title: Mostra suoni (e flag di descrizione audio)
description: Questo argomento include informazioni su un parametro che indica se un'applicazione deve fornire un avviso visivo o un segnale acustico quando usa il suono per comunicare informazioni importanti.
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf32dfacdf1dc0b8ed3bc51c986ae572e43300263565254ad6b3a48a981beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734321"
---
# <a name="show-sounds-and-audio-description-flag"></a>Mostra suoni (e flag di descrizione audio)

Questo argomento include informazioni su un parametro che indica se un'applicazione deve fornire un avviso visivo o un segnale acustico quando usa il suono per comunicare informazioni importanti. Fornisce inoltre informazioni su un flag che indica se un'applicazione deve fornire una descrizione audio per gli elementi visivi.

## <a name="show-sounds-parameter"></a>Parametro Mostra suoni

Il parametro show sounds indica se l'utente vuole che le applicazioni presentino tutte le informazioni importanti in formato visivo.

L'utente controlla l'impostazione del parametro show sounds usando il Centro accessibilità in Pannello di controllo o un'altra applicazione per personalizzare l'ambiente. Le applicazioni usano i flag **SPI \_ GETSHOWSOUNDS** e **SPI \_ SETSHOWSOUNDS** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro show sounds. In alternativa, le applicazioni possono usare il flag **\_ SM SHOWSOUNDS** con la [**funzione GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) per determinare lo stato del parametro show sounds.

Determinare lo stato del parametro show sounds è necessario solo per le applicazioni che in genere presentano informazioni importanti solo in base al suono. Le applicazioni devono fornire il supporto per la visualizzazione di suoni se usano suoni in uno dei modi seguenti:

-   Trasmettere informazioni importanti per il funzionamento dell'applicazione.
-   Per avvisare l'utente che le informazioni importanti vengono presentate visivamente. In questo caso, anche se le informazioni vengono presentate visivamente, il suono ha la funzione aggiuntiva di attirare l'attenzione dell'utente.

I moduli appropriati per il feedback visivo possono rendere il software molto più funzionale per gli utenti che non possono basarsi solo sul suono. La progettazione del feedback visivo è specifica dell'applicazione e dipende dalle informazioni che verranno presentate all'utente. Ad esempio, per attirare l'attenzione dell'utente quando arriva una nuova posta elettronica, l'applicazione potrebbe lampeggiare la finestra o persino l'intero schermo. Se l'applicazione in genere fa rumore per indicare che l'utente sta tentando di eseguire un'operazione non valida, potrebbe anche visualizzare un messaggio appropriato sulla relativa riga di stato o usare la funzione [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) per visualizzare un messaggio di errore specifico. Se l'applicazione è in genere progettata per riprodurre bit audio che hanno un significato, ad esempio la voce digitalizzata, potrebbe anche visualizzare una finestra della didascalia con lo stesso testo.

È stato dimostrato l'uso ridondante di avvisi acustici e visivi per aumentare l'usabilità delle applicazioni software. Il parametro show sounds è una richiesta di feedback visivo, ma il suo uso non limita un'applicazione alla presentazione visiva delle informazioni. Gli utenti devono essere in grado di richiedere feedback visivo indipendentemente dal fatto che vogliano o meno commenti e suggerimenti udibili.

## <a name="audio-description-flag"></a>Flag di descrizione audio

Le applicazioni usano **i flag SPI \_ GETAUDIODESCRIPTION** e **SPI \_ SETAUDIODESCRIPTION** con la [**funzione SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per abilitare o disabilitare le descrizioni audio. Anche se è possibile per gli utenti con problemi di vista ascoltare l'audio nel contenuto video, nel video è presente una grande quantità di azioni che non hanno audio corrispondente. Una descrizione audio specifica di ciò che accade in un video consente a questi utenti di comprendere meglio il contenuto. Questo flag consente di abilitare o disabilitare le descrizioni audio nelle lingue in cui vengono fornite.

 

 