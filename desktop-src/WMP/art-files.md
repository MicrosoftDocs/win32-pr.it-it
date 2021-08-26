---
title: File di grafica
description: File di grafica
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Windows Media Player, file art
- skins, file art
- file per le interfaccia, grafica
- file di grafica per le interfaccia, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89ccf07757e511f7717cbe3bbeff2cdacee004da8d3b64d27ddcef7ae2199a29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956371"
---
# <a name="art-files"></a>File di grafica

È necessario creare uno o più file di grafica per l'interfaccia. Senza grafica, l'utente non avrà nulla da guardare. È possibile creare un'interfaccia invisibile, ma nessuno la vede. E anche in questo caso, sarebbe comunque necessario creare file di grafica per contenere le immagini invisibili, perché il file di definizione dell'interfaccia richiede file di grafica per elementi specifici.

Esistono tre usi per le immagini nelle interfaccia: immagini primarie, immagini di mapping e immagini alternative.

## <a name="primary-images"></a>Immagini primarie

È necessario creare un'immagine primaria per l'interfaccia. Questo è ciò che gli utenti visualizzano quando installano l'interfaccia utente. L'immagine primaria è costituita da una o più immagini create da specifici controlli dell'interfaccia utente.

Se sono presenti più controlli, è necessario specificare l'ordine z, che definisce i controlli da visualizzare davanti ad altri controlli. Ogni **elemento View** avrà un'immagine di sfondo a cui è possibile aggiungere altre immagini di elemento, consentendo di creare un'immagine composita primaria.

È anche possibile avere immagini secondarie, ad esempio una barra scorrevole, che non vengono visualizzate quando viene visualizzata l'interfaccia per la prima volta, ma che vengono visualizzate quando l'utente esegue un'azione. Seguono le stesse regole delle immagini primarie, in quanto vengono create con un set di controlli.

## <a name="mapping-images"></a>Mapping di immagini

Una delle funzionalità più potenti delle Windows Media Player è che è possibile usare il mapping delle immagini per attivare eventi per l'interfaccia. Le mappe immagini sono file che contengono immagini speciali. Le immagini in un file di mappa immagine, tuttavia, non sono destinate a essere visualizzate dall'utente, ma vengono usate da Windows Media Player per intervenire quando l'utente fa clic sull'interfaccia.

Controlli diversi necessitano di tipi diversi di mappe immagine. Ad esempio, se si colora una parte di una mappa immagine con un valore rosso specifico e l'utente fa clic sull'area corrispondente dell'immagine primaria, un pulsante genera un evento. Il colore viene usato per definire quali eventi vengono attivati facendo clic in una determinata area dell'interfaccia.

## <a name="alternate-images"></a>Immagini alternative

È anche possibile configurare immagini alternative da visualizzare quando un utente esegue un'applicazione. Ad esempio, è possibile creare un'immagine alternativa di un pulsante che verrà visualizzata solo quando si passa il mouse sul pulsante. Si tratta di un modo efficace per far sapere agli utenti cosa possono fare e consente anche un'interfaccia utente altamente individuabile. Usando con attenzione le descrizioni comandi e le immagini al passaggio del mouse, è possibile creare interfacce utente insolite che forniscono comunque all'utente commenti e suggerimenti sulle opzioni disponibili.

Le sezioni seguenti forniscono altre informazioni sui file di grafica:

-   [Immagini primarie](primary-images.md)
-   [Mapping di immagini](mapping-images.md)
-   [Immagini alternative](alternate-images.md)
-   [Formati di file di grafica](art-file-formats.md)
-   [Esempio di grafica semplice](simple-art-example.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di interfaccia**](skin-files.md)
</dt> </dl>

 

 




