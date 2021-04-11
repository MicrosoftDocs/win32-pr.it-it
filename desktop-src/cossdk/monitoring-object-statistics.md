---
description: È possibile monitorare le statistiche degli oggetti durante l'esecuzione di un'applicazione. In questo modo, è possibile ottimizzare le caratteristiche del pool di oggetti per ottenere il bilanciamento delle prestazioni e delle risorse che si desidera ottenere.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Monitoraggio delle statistiche degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342201"
---
# <a name="monitoring-object-statistics"></a>Monitoraggio delle statistiche degli oggetti

È possibile monitorare le statistiche degli oggetti durante l'esecuzione di un'applicazione. In questo modo, è possibile ottimizzare le caratteristiche del pool di oggetti per ottenere il bilanciamento delle prestazioni e delle risorse che si desidera ottenere.

È possibile monitorare lo stato di tutti gli oggetti configurati per supportare le statistiche degli oggetti e la segnalazione degli eventi. L'abilitazione delle statistiche degli oggetti presenta un lieve sovraccarico delle prestazioni.

**Per abilitare le statistiche degli oggetti**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .

3.  Per abilitare le statistiche degli oggetti per il componente, in **contesto di attivazione** selezionare la casella di controllo **componente supporta eventi e statistiche** .

**Per monitorare lo stato di un oggetto**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti aprire la cartella per l'applicazione che include i componenti che si desidera monitorare.

2.  Fare clic con il pulsante destro del mouse sulla cartella **componenti** , scegliere **Visualizza** e quindi fare clic su **visualizzazione stato**. Il riquadro dei dettagli Visualizza ora la visualizzazione stato per tutti i componenti dell'applicazione. Nella tabella seguente vengono descritte le sei colonne della vista di stato.

    

    | Colonna                        | Descrizione                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **ProgID**<br/>         | Identifica un componente specifico.<br/>                                                                                                                                                                                |
    | **Oggetti**<br/>        | Mostra il numero di oggetti attualmente conservati dai riferimenti client.<br/>                                                                                                                                       |
    | **Attivato**<br/>      | Mostra il numero di oggetti attualmente attivati. <br/>                                                                                                                                                      |
    | **In pool**<br/>         | Mostra il numero totale di oggetti creati dal pool, inclusi gli oggetti in uso e gli oggetti che sono stati disattivati.<br/>                                                                                      |
    | **Nella chiamata**<br/>        | Identifica gli oggetti nella chiamata.<br/>                                                                                                                                                                                     |
    | **Tempo di chiamata (MS)**<br/> | Mostra la durata media della chiamata (in millisecondi) di chiamate al metodo effettuate negli ultimi 20 secondi (fino a 20 chiamate). Il tempo di chiamata viene misurato in corrispondenza dell'oggetto e non include il tempo usato per attraversare la rete.<br/> |

    

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione di un componente da raggruppare](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




