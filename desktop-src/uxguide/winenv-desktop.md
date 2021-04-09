---
title: Desktop
description: Il desktop è l'area di lavoro dell'utente per i propri programmi. Non è un modo per promuovere la consapevolezza del programma o del suo marchio. Non abusarlo.
ms.assetid: 99cb218d-9b1f-4e43-94d2-4ea74b0e10d3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 159be01b1058eac99c30b83534b7a9eafd9c4eb4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104058413"
---
# <a name="desktop"></a>Desktop

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Il desktop è l'area di lavoro dell'utente per i propri programmi. Non è un modo per promuovere la consapevolezza del programma o del suo marchio. Non abusa!

Il desktop è l'area di lavoro sullo schermo fornita da Microsoft Windows, analoga a un desktop fisico. È costituito da un' [area di lavoro](glossary.md) e da una [barra delle applicazioni](winenv-taskbar.md). L'area di lavoro può estendersi su più monitor.

![Screenshot di un tipico desktop di Windows ](images/winenv-desktop-image1.png)

Un tipico desktop di Windows.

Il monitoraggio attivo è il monitoraggio in cui è in esecuzione il programma attivo. Il monitoraggio predefinito è quello con il menu Start, la barra delle applicazioni e l'area di notifica.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Il desktop di Windows presenta i seguenti punti di accesso al programma:

-   **Area di lavoro.** Area sullo schermo in cui gli utenti possono eseguire il proprio lavoro, oltre ad archiviare programmi, documenti e collegamenti. Sebbene tecnicamente il desktop includa la barra delle applicazioni, nella maggior parte dei contesti si riferisce solo all'area di lavoro.
-   **Pulsante Avvia.** Il punto di accesso per tutti i programmi e i luoghi speciali di Windows (documenti, immagini, musica, giochi, computer, pannello di controllo) con gli elenchi "usati di recente" per accedere rapidamente ai programmi e ai documenti usati di recente.
-   **Avvio veloce. Rimosso da Windows 7.** Un punto di accesso diretto per i programmi selezionati dall'utente.
-   **Barra delle applicazioni.** Il punto di accesso per l'esecuzione di programmi con presenza desktop. Sebbene tecnicamente la barra delle applicazioni si estenda sull'intera barra dal pulsante Start all'area di notifica, nella maggior parte dei contesti sulla barra delle applicazioni si fa riferimento all'area in cui è presente la barra delle applicazioni. Questa area viene a volte definita TaskBand.
-   **Deskbands. Non consigliato.** Programmi funzionali e a esecuzione prolungata ridotta, ad esempio la barra del linguaggio. I programmi che riducono al minimo deskbands non visualizzano i pulsanti della barra delle applicazioni se ridotti a icona
-   **Area di notifica.** Un'origine a breve termine per le notifiche e lo stato, oltre a un punto di accesso per le funzionalità relative al sistema e al programma che non hanno alcuna presenza sul desktop.

![screenshot del pulsante avvia, della barra delle applicazioni, dell'anteprima ](images/winenv-desktop-image2.png)

I punti di accesso desktop di Windows includono il pulsante avvia, la barra delle applicazioni e l'area di notifica. Si noti la funzionalità di anteprima del pulsante della barra delle applicazioni.

**Il desktop di Windows è una risorsa condivisa limitata che rappresenta il punto di ingresso dell'utente per Windows. Lascia gli utenti sotto controllo.** È consigliabile usare le relative aree come previsto: qualsiasi altro uso dovrebbe essere considerato un abuso. Non visualizzarli mai come modi per promuovere la consapevolezza del programma o del suo [marchio](exper-branding.md).

Per Windows 7, i produttori di apparecchiature originali (OEM) e i fornitori di hardware indipendenti (IHV) possono utilizzare la fase del dispositivo per progettare un'interfaccia utente personalizzata personalizzata per il computer e i dispositivi, senza ingombrare i desktop degli utenti. Gli OEM in particolare possono usare il PC per la fase del dispositivo per presentare programmi personalizzati, offerte di servizi e supporto. Per ulteriori informazioni, vedere [Microsoft Device Experience Development Kit](https://www.microsoft.com/whdc/device/DeviceExperience/Dev-Kit.mspx).

**Se si esegue una sola operazione...**

-   Non abusa del desktop: Mantieni gli utenti sotto controllo. Se è probabile che gli utenti di destinazione usino spesso il programma, fornire un'opzione durante l'installazione per inserire un collegamento sul desktop, deselezionato per impostazione predefinita.

## <a name="guidelines"></a>Indicazioni

-   **Se è molto probabile che gli utenti usino spesso il programma, fornire un'opzione durante l'installazione per inserire un collegamento a un programma sul desktop.** La maggior parte dei programmi non verrà usata abbastanza spesso per garantire l'offerta di questa opzione.
-   **Presentare l'opzione deselezionata per impostazione predefinita.** Chiedere agli utenti di selezionare l'opzione è importante perché, quando sul desktop sono presenti icone indesiderate, molti utenti sono riluttanti a rimuoverli. Questo può causare confusione sul desktop superfluo.
-   **Se gli utenti selezionano l'opzione, fornire un solo collegamento al programma.** Se il prodotto è costituito da più programmi, fornire un collegamento solo al programma principale.
-   **Inserire solo i tasti di scelta rapida del programma sul desktop.** Non inserire il programma effettivo o altri tipi di file.

    **Corretto:**

    ![screenshot dell'icona del collegamento con sovrapposizione a freccia ](images/winenv-desktop-image3.png)

    **Non corretto:**

    ![screenshot dell'icona del programma ](images/winenv-desktop-image4.png)

    Nell'esempio errato, il programma, non un tasto di scelta rapida, viene copiato sul desktop.

-   **Scegliere un'etichetta che può essere visualizzata senza troncamento.** Gli utenti non dovrebbero visualizzare i puntini di sospensione.

    **Corretto:**

    ![screenshot dell'icona del collegamento con il nome completo ](images/winenv-desktop-image3.png)

    **Non corretto:**

    ![screenshot dell'icona del collegamento con il nome troncato ](images/winenv-desktop-image5.png)

    Nell'esempio errato, l'etichetta del collegamento del programma è talmente lungo che viene troncata.

## <a name="documentation"></a>Documentazione

-   Quando si fa riferimento al desktop, utilizzare desktop, non in maiuscolo.
-   Quando si fa riferimento a collegamenti desktop, usare il collegamento, non maiuscolo.

 

 