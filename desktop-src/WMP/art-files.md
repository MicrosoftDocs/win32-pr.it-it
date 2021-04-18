---
title: File di immagine
description: File di immagine
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di immagine per le interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298865"
---
# <a name="art-files"></a>File di immagine

È necessario creare uno o più file di immagine per l'interfaccia personalizzata. Senza l'arte, l'utente non avrà nulla da considerare. È possibile creare un'interfaccia invisibile, ma non ne verrebbe visualizzata alcuna. Anche in questo caso, è necessario creare file di immagine per contenere le immagini invisibili, perché il file di definizione dell'interfaccia richiede file di immagine per elementi specifici.

Sono disponibili tre usi per l'arte negli Skin: immagini primarie, immagini di mapping e immagini alternative.

## <a name="primary-images"></a>Immagini primarie

È necessario creare un'immagine primaria per l'interfaccia personalizzata. Questo è ciò che gli utenti visualizzeranno durante l'installazione dell'interfaccia. L'immagine principale è costituita da una o più immagini create da specifici controlli di interfaccia.

Se si dispone di più di un controllo, è necessario specificare l'ordine z, che definisce i controlli che vengono visualizzati davanti ad altri controlli. Ogni elemento di **visualizzazione** avrà un'immagine di sfondo a cui è possibile aggiungere altre immagini di elementi, consentendo di creare un'immagine composita primaria.

È anche possibile avere immagini secondarie, ad esempio una barra di scorrimento, che non vengono visualizzate quando l'interfaccia viene visualizzata per la prima volta, ma che vengono visualizzate quando l'utente esegue un'azione. Seguono le stesse regole delle immagini primarie, in quanto vengono create con un set di controlli.

## <a name="mapping-images"></a>Mapping di immagini

Una delle funzionalità più potenti di Windows Media Player Skin è che è possibile usare il mapping delle immagini per attivare gli eventi per l'interfaccia personalizzata. Le mappe immagine sono file che contengono immagini speciali. Le immagini in un file di mappa immagine, tuttavia, non sono pensate per essere visualizzate dall'utente, ma vengono usate da Windows Media Player per eseguire un'azione quando l'utente fa clic sull'interfaccia.

Per i diversi controlli sono necessari tipi diversi di mappe immagine. Se, ad esempio, si colora parte di un'immagine con un valore rosso specifico e l'utente fa clic sull'area corrispondente dell'immagine primaria, un pulsante genererà un evento. Il colore viene utilizzato per definire quali eventi vengono attivati facendo clic in una particolare area dell'interfaccia.

## <a name="alternate-images"></a>Immagini alternative

È anche possibile configurare immagini alternative da visualizzare quando un utente esegue un'operazione. Ad esempio, è possibile creare un'immagine alternativa di un pulsante che verrà visualizzato solo quando il mouse viene posizionato sul pulsante. Si tratta di un metodo efficace per consentire agli utenti di sapere cosa possono fare e anche di un'interfaccia utente altamente individuabile. Utilizzando con attenzione le descrizioni comandi e le immagini del passaggio del mouse, è possibile creare interfacce utente insolite che forniscono comunque commenti e suggerimenti sugli utenti sulle opzioni disponibili.

Nelle sezioni seguenti vengono fornite ulteriori informazioni sui file di immagine:

-   [Immagini primarie](primary-images.md)
-   [Mapping di immagini](mapping-images.md)
-   [Immagini alternative](alternate-images.md)
-   [Formati di file di immagine](art-file-formats.md)
-   [Esempio di arte semplice](simple-art-example.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di interfaccia**](skin-files.md)
</dt> </dl>

 

 




