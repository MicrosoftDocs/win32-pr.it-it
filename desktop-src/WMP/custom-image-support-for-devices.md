---
title: Supporto di immagini personalizzate per i dispositivi
description: Supporto di immagini personalizzate per i dispositivi
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player, supporto immagini personalizzate per i dispositivi
- Windows Media Player, supporto immagini per i dispositivi
- supporto per immagini personalizzate del dispositivo
- supporto di immagini personalizzate per i dispositivi
- supporto delle immagini per i dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300064"
---
# <a name="custom-image-support-for-devices"></a>Supporto di immagini personalizzate per i dispositivi

> [!Note]  
> In questa sezione viene documentata una funzionalità di Windows Media Player 10 disponibile quando si utilizza il sistema operativo Windows XP. Potrebbe non essere disponibile nelle versioni successive.

 

I produttori di dispositivi possono fornire due file di immagine speciali per personalizzare la modalità di rappresentazione di un dispositivo nell'interfaccia utente di Windows Media Player 10. Questi due file sono:

-   Devicon. fil. Un file di formato dell'icona Windows che rappresenta l'hardware del dispositivo. Questa immagine viene visualizzata in Windows Media Player 10 in qualsiasi punto in cui viene usata un'icona per rappresentare un dispositivo, ad esempio l'elenco dei dispositivi nella funzionalità di **sincronizzazione** .
-   Devlogo. fil. Un file di formato PNG che rappresenta il logo aziendale del produttore del dispositivo. Questa immagine viene visualizzata in Windows Media Player 10 ovunque viene utilizzata la personalizzazione aziendale, ad esempio la finestra di dialogo **Configurazione dispositivo** .

## <a name="general-guidelines-for-images"></a>Linee guida generali per le immagini

Le linee guida seguenti si applicano al supporto di immagini personalizzate in generale:

-   Questa funzionalità è facoltativa. I dispositivi che non forniscono immagini verranno rappresentati da immagini predefinite.
-   Questa funzionalità è supportata solo per i dispositivi abilitati per MTP.
-   Per evitare modifiche ai file, è consigliabile archiviare i file di immagine nel firmware o in un supporto di archiviazione protetto, non con i file creati dall'utente.
-   I file non devono essere restituiti a Windows Media Gestione dispositivi client che enumerano l'archiviazione radice del dispositivo. Inoltre, l'eliminazione, lo stato di trasferimento o la ridenominazione dei file dovrebbe avere esito negativo.
-   Se il dispositivo fornisce più di un supporto di archiviazione, il dispositivo deve restituire i file di immagine in risposta alle richieste di apertura dei file da qualsiasi supporto. È possibile che vengano restituite icone del dispositivo diverse da ogni supporto di archiviazione.
-   Per i client Windows Media Gestione dispositivi 1,2 abilitati, queste immagini avranno la precedenza sulle proprietà delle icone fornite dai meccanismi di installazione di Windows, ad esempio le proprietà dei nodi del dispositivo.
-   Le immagini non devono contenere informazioni che richiedono la localizzazione.
-   Per i dispositivi multifunzione, solo le funzionalità di riproduzione musica di Windows XP utilizzeranno tali immagini.

## <a name="creating-the-device-icon-image"></a>Creazione dell'immagine dell'icona del dispositivo

Il file di immagine dell'icona del dispositivo, devicon. fil, deve contenere un file nel formato dell'icona di Windows. [Nelle icone degli articoli di MSDN in Win32](/previous-versions/ms997538(v=msdn.10)) viene descritto come creare un file di questo tipo. L'articolo di MSDN [creazione di icone di Windows XP](/previous-versions/ms997636(v=msdn.10)) offre linee guida di stile per le icone di Windows XP. Il file di immagine dell'icona del dispositivo incorpora dodici immagini in un singolo file, fornendo quattro dimensioni diverse con tre diverse profondità di colore.

Accertarsi di prestare particolare attenzione alle linee guida seguenti:

-   Le dimensioni consigliate (in pixel) sono 16x16, 32x32, 48x48 e 256x256.
-   Le profondità di colore consigliate sono a 24 bit con canale alfa a 8 bit, a 8 bit con trasparenza a 1 bit e a 4 bit con trasparenza a 1 bit.
-   Usare l'angolo prospettico e i consigli per l'ombreggiatura descritti negli articoli di MSDN menzionati in precedenza.

Una volta creato il file icona, è sufficiente rinominarlo devicon. fil.

## <a name="creating-the-corporate-logo-image"></a>Creazione dell'immagine del logo aziendale

Il file di immagine del logo aziendale, devlogo. fil, deve contenere un file in formato PNG. Quando si crea l'immagine, attenersi alle linee guida seguenti:

-   Le dimensioni massime per l'immagine sono 150x32 pixel.
-   L'immagine deve supportare la fusione alfa per consentire una transizione uniforme tra l'interfaccia utente di Windows Media Player 10 e il logo.

Una volta creato il file del logo aziendale, è sufficiente rinominarlo devlogo. fil.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 