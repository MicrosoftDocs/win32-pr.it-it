---
title: Mostra suoni (e flag Descrizione audio)
description: Questo argomento include informazioni su un parametro che indica se un'applicazione deve fornire un avviso o un segnale visivo quando usa un suono per trasmettere informazioni importanti.
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d01e3fda902c23c86279a9a4d75889ebfeff4d55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300036"
---
# <a name="show-sounds-and-audio-description-flag"></a>Mostra suoni (e flag Descrizione audio)

Questo argomento include informazioni su un parametro che indica se un'applicazione deve fornire un avviso o un segnale visivo quando usa un suono per trasmettere informazioni importanti. Fornisce inoltre informazioni su un flag che indica se un'applicazione deve fornire una descrizione audio per gli elementi visivi.

## <a name="show-sounds-parameter"></a>Mostra parametro suoni

Il parametro Mostra suoni indica se l'utente desidera che le applicazioni presentino tutte le informazioni importanti in formato visivo.

L'utente controlla l'impostazione del parametro Mostra suoni usando il centro di accesso facilitato nel pannello di controllo o un'altra applicazione per la personalizzazione dell'ambiente. Le applicazioni usano i flag **SPI \_ GETSHOWSOUNDS** e **SPI \_ SETSHOWSOUNDS** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro show Sounds. In alternativa, le applicazioni possono usare il flag **SM \_ SHOWSOUNDS** con la funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) per determinare lo stato del parametro show Sounds.

Determinare lo stato del parametro Mostra suoni è necessario solo per le applicazioni che in genere presentano informazioni importanti solo in base al suono. Le applicazioni devono fornire il supporto di Mostra suoni se usano i suoni in uno dei modi seguenti:

-   Per fornire informazioni importanti per il funzionamento dell'applicazione.
-   Per avvisare l'utente che vengono presentate visivamente informazioni importanti. In tal caso, anche se le informazioni vengono presentate visivamente, il suono ha la funzione aggiuntiva per attirare l'attenzione dell'utente.

I moduli di feedback visivi appropriati possono rendere il software molto più funzionale per gli utenti che non possono basarsi solo su un suono. La progettazione del feedback visivo è specifica dell'applicazione e dipende dalle informazioni che verranno presentate all'utente. Ad esempio, per attirare l'attenzione dell'utente quando arriva un nuovo messaggio di posta elettronica, l'applicazione potrebbe lampeggiare la finestra o anche l'intero schermo. Se l'applicazione in genere emette un suono per indicare che l'utente sta tentando di eseguire un'operazione non valida, potrebbe anche visualizzare un messaggio appropriato sulla riga di stato oppure utilizzare la funzione [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) per visualizzare un messaggio di errore specifico. Se l'applicazione è in genere progettata per riprodurre punture acustiche che portano significato, ad esempio un riconoscimento vocale digitalizzato, è possibile che venga visualizzata anche una finestra didascalia con lo stesso testo.

Per aumentare l'usabilità delle applicazioni software, è stato visualizzato un utilizzo ridondante di avvisi acustici e visivi. Il parametro show Sounds è una richiesta di commenti e suggerimenti visivi, ma il suo utilizzo non impedisce a un'applicazione di presentare le informazioni in modo visivo. Gli utenti devono essere in grado di richiedere commenti visivi indipendentemente dal fatto che vogliano anche ricevere feedback acustici.

## <a name="audio-description-flag"></a>Flag descrizione audio

Per abilitare o disabilitare le descrizioni audio, le applicazioni usano i flag **SPI \_ GETAUDIODESCRIPTION** e **SPI \_ SETAUDIODESCRIPTION** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) . Anche se è possibile che gli utenti non siano in grado di ascoltare l'audio nei contenuti video, è presente una grande quantità di azioni video senza audio corrispondente. Una descrizione audio specifica di ciò che accade in un video consente a questi utenti di comprendere meglio il contenuto. Questo flag consente di abilitare o disabilitare le descrizioni audio nelle lingue in cui sono disponibili.

 

 