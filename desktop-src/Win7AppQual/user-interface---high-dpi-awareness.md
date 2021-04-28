---
description: Interfaccia utente - Compatibilità DPI avanzata
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: Interfaccia utente - Compatibilità DPI avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116069"
---
# <a name="user-interface---high-dpi-awareness"></a>Interfaccia utente - Compatibilità DPI avanzata

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** - Windows XP \| Windows Vista Windows \| 7  

## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Media  
**Frequenza** - Media  

## <a name="description"></a>Descrizione

L'obiettivo è quello di invitare gli utenti finali a impostare la risoluzione nativa e usare DPI anziché la risoluzione dello schermo per modificare le dimensioni del testo e delle immagini visualizzate. Windows 7 può rilevare e configurare automaticamente un valore DPI predefinito nelle installazioni pulite nei computer configurati dagli OEM usando le impostazioni DPI. Sono disponibili strumenti che è possibile usare per progettare applicazioni con valori DPI elevati per garantire risultati più leggibili.

Sono state aggiunte due nuove funzionalità high DPI a Windows 7:

-   Impostazione DPI per utente (in precedenza per computer)
-   Modificare il valore DPI senza riavviare (la disconnessione/accesso è ancora necessaria)

## <a name="manifestation-of-impact"></a>Manifestazione di impatto

È probabile che le applicazioni che non gestiscono il caso DPI elevato presentino artefatti visivi, tra cui:

-   Ritaglio dell'interfaccia utente o del testo da altri elementi dell'interfaccia utente
-   Dimensioni dei caratteri incoerenti
-   Off-screen UIs
-   Sfocatura del testo o dell'interfaccia utente
-   Trascinamento della selezione interrotto o altri input
-   Rendering di applicazioni DX a schermo intero parzialmente fuori schermo

## <a name="solution"></a>Soluzione

Per rendere le applicazioni in grado di riconoscere DPI:

1.  Eseguire un test funzionale di alto livello, inclusa l'installazione e la disinstallazione nelle impostazioni seguenti:

    | Impostazione                                              | Elementi da cercare                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024x768 @ 120 DPI (ridimensionamento del 125%)                    | Si tratta di una risoluzione efficace di ~800x600, quindi cercare i problemi di interfaccia utente tagliati fuori dalla schermata o dal layout. Cercare anche bitmap con pixilated & icone.                         |
    | 1600 x 1200 @144 DPI (ridimensionamento del 150%)                    | Interfaccia utente sfocata. Verificare che tutte le operazioni del mouse funzionino, in particolare trascinare & di rilascio. Verificare anche che le modalità schermo intero funzionino correttamente.                                     |
    | 1600x1200 @ 144 DPI con Virtualizzazione DPI disabilitata | Spesso i pulsanti e l'interfaccia utente non vengono ridimensionati in relazione al testo più grande & sarà presente un ritaglio di testo significativo. Cercare i problemi di layout in generale & bitmat con pixilated & icone. |

    

     

2.  Annota tutti i problemi rilevati, tra cui la posizione, la risoluzione dello schermo e le impostazioni DPI, nonché il comportamento dell'applicazione nelle altre configurazioni DPI/Risoluzione per la completezza
3.  Verificare ogni problema in base ai problemi comuni di codifica DPI
4.  Valutare il costo per rendere l'applicazione completamente consapevole di DPI
5.  Creare un elenco degli asset High DPI necessari (ad esempio, pulsanti, icone)
6.  Eseguire e correggere l'elenco dei problemi DPI rilevati nel passaggio 1
7.  Integrare i nuovi asset del passaggio 5
8.  Dichiarare l'applicazione che è in grado di riconoscere DPI

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

Eseguire nuovamente la valutazione del riconoscimento DPI e verificare che i problemi siano stati risolti.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Sviluppo di applicazioni desktop con valori DPI alti in Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Per domande tecniche, contattare:**<disup@microsoft.com>

 

 
