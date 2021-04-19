---
description: .
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: Interfaccia utente - Compatibilità DPI avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e93aeed452f421e8e38df8d6d75f6bbe1f97cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319828"
---
# <a name="user-interface---high-dpi-awareness"></a>Interfaccia utente - Compatibilità DPI avanzata

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** -Windows XP Windows \| Vista Windows \| 7  

## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -medio  
**Frequenza** -media  

## <a name="description"></a>Descrizione

L'obiettivo è incoraggiare gli utenti finali a impostare gli schermi sulla risoluzione nativa e utilizzare DPI anziché la risoluzione dello schermo per modificare le dimensioni del testo e delle immagini visualizzate. Windows 7 consente di rilevare automaticamente e configurare un valore DPI predefinito in installazioni pulite nei computer configurati dagli OEM usando le impostazioni DPI. Sono disponibili strumenti che consentono di progettare applicazioni con compatibilità DPI elevata, in modo da garantire i risultati più leggibili.

Sono state aggiunte due nuove funzionalità DPI elevate a Windows 7:

-   Impostazione DPI per utente (in precedenza per computer)
-   Modificare il valore DPI senza riavviare (la disconnessione/accesso è ancora necessaria)

## <a name="manifestation-of-impact"></a>Manifesto di effetto

Le applicazioni che non gestiscono il case con valori DPI alti possono presentare artefatti visivi, tra cui:

-   Ritaglio dell'interfaccia utente o del testo da altri elementi dell'interfaccia utente
-   Dimensioni del carattere incoerenti
-   Interfacce utente non schermate
-   Sfocatura di testo o interfaccia utente
-   Trascinamento della selezione o altri input interrotti
-   Rendering delle applicazioni DX a schermo intero parzialmente fuori dallo schermo

## <a name="solution"></a>Soluzione

Per rendere le applicazioni compatibili con DPI:

1.  Eseguire un test funzionale di alto livello, incluso l'installazione e la disinstallazione, nelle impostazioni seguenti:

    | Impostazione                                              | Elementi da cercare                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024x768 @ 120 DPI (125% in scala)                    | Si tratta di una risoluzione efficace di ~ 800x600, quindi cercare l'interfaccia utente ritagliata in caso di problemi di layout o schermo. Cercare anche le bitmap scatti & icone.                         |
    | @144dpi 1600x1200 (150% in scala)                    | Interfaccia utente sfocata. Verificare che tutte le operazioni del mouse funzionino, in particolare trascinare & operazioni di rilascio. Verificare inoltre che le modalità a schermo intero funzionino correttamente.                                     |
    | 1600x1200 @ 144 DPI con virtualizzazione DPI disabilitata | Spesso i pulsanti e l'interfaccia utente non vengono ridimensionati in relazione a testo di dimensioni maggiori & il ritaglio del testo è significativo. Individuare i problemi di layout in generale & & icone di scatti bitmats. |

    

     

2.  Annotare tutti i problemi rilevati, inclusi il percorso, la risoluzione dello schermo e le impostazioni DPI, nonché il comportamento dell'applicazione nelle altre configurazioni DPI/di risoluzione per completezza
3.  Controllare ogni problema per i problemi di codifica DPI comuni
4.  Valutare il costo di rendere la compatibilità dell'applicazione con DPI
5.  Creare un elenco di asset DPI alti richiesti (ad esempio, pulsanti, icone)
6.  Risolvere e correggere l'elenco dei problemi DPI trovati nel passaggio 1
7.  Integrare i nuovi asset dal passaggio 5
8.  Dichiarare la compatibilità dell'applicazione con DPI

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilità, prestazioni, affidabilità e test di usabilità

Eseguire di nuovo la valutazione della consapevolezza DPI e verificare che i problemi siano corretti.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Sviluppo di applicazioni desktop con DPI elevato in Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Contattare per domande tecniche:**<disup@microsoft.com>

 

 
