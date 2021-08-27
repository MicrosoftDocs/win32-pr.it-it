---
description: Interfaccia utente - Compatibilità DPI avanzata
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: Interfaccia utente - Compatibilità DPI avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52c2bb42ad2c54fc1d23e44edf54e4bc88f8ab40a3f3a04f9dbc57b484b55173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994581"
---
# <a name="user-interface---high-dpi-awareness"></a>Interfaccia utente - Compatibilità DPI avanzata

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** - Windows XP \| Windows Vista \| Windows 7  

## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Media  
**Frequenza** - Media  

## <a name="description"></a>Descrizione

L'obiettivo è incoraggiare gli utenti finali a impostare i display sulla risoluzione nativa e a usare DPI anziché la risoluzione dello schermo per modificare le dimensioni del testo e delle immagini visualizzate. Windows 7 è in grado di rilevare e configurare automaticamente un valore DPI predefinito nelle installazioni pulite nei computer configurati dai relativi OEM usando le impostazioni DPI. Sono disponibili strumenti che è possibile usare per progettare applicazioni con valori DPI elevati per garantire risultati più leggibili.

Sono state aggiunte due nuove funzionalità high DPI Windows 7:

-   Impostazione DPI per utente (in precedenza per computer)
-   Modificare il valore DPI senza riavvio (la disconnessione o l'accesso è ancora necessario)

## <a name="manifestation-of-impact"></a>Impatto significativo

È probabile che le applicazioni che non gestiscono il caso con valori DPI alti presentino artefatti visivi, tra cui:

-   Ritaglio dell'interfaccia utente o del testo in base ad altri elementi dell'interfaccia utente
-   Dimensioni dei caratteri incoerenti
-   UIs fuori schermo
-   Sfocatura del testo o dell'interfaccia utente
-   Trascinamento della selezione interrotto o altri input
-   Rendering di applicazioni DX a schermo intero parzialmente fuori schermo

## <a name="solution"></a>Soluzione

Per rendere le applicazioni in grado di riconoscere DPI:

1.  Eseguire un test funzionale di alto livello, inclusa l'installazione e la disinstallazione con le impostazioni seguenti:

    | Impostazione                                              | Elementi da cercare                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024x768 @ 120 DPI (ridimensionamento del 125%)                    | Si tratta di una risoluzione efficace di ~800x600, quindi cercare i problemi di interfaccia utente ritagliati sullo schermo o sul layout. Cercare anche bitmap con pixilated & icone.                         |
    | 1600 x 1200 @144 DPI (ridimensionamento al 150%)                    | Interfaccia utente sfocata. Verificare che tutte le operazioni del mouse funzionino, in particolare le operazioni di trascinamento & rilascio. Verificare anche che le modalità schermo intero funzionino correttamente.                                     |
    | 1600x1200 @ 144 DPI con virtualizzazione DPI disabilitata | Spesso i pulsanti e l'interfaccia utente non vengono ridimensionati in relazione a testo più grande & il ritaglio del testo sarà significativo. Cercare i problemi di layout in generale & bitmat con pixilated & icone. |

    

     

2.  Annota tutti i problemi rilevati, tra cui posizione, risoluzione dello schermo e impostazioni DPI, nonché il comportamento dell'applicazione nelle altre configurazioni DPI/risoluzione per completezza
3.  Verificare ogni problema in base ai problemi comuni di codifica DPI
4.  Valutare i costi per rendere l'applicazione completamente in grado di riconoscere IDPI
5.  Creare un elenco degli asset con valori DPI alti necessari (ad esempio, pulsanti, icone)
6.  Eseguire e correggere l'elenco dei problemi DPI rilevati nel passaggio 1
7.  Integrare i nuovi asset del passaggio 5
8.  Dichiarare l'applicazione in grado di riconoscere DPI

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

Eseguire nuovamente la valutazione del riconoscimento DPI e verificare che i problemi siano stati risolti.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Sviluppo di applicazioni desktop con valori DPI elevati in Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Per domande tecniche, contattare:**<disup@microsoft.com>

 

 
