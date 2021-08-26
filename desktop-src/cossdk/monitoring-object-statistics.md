---
description: È possibile monitorare le statistiche degli oggetti durante l'esecuzione di un'applicazione. In questo modo, è possibile ottimizzare le caratteristiche del pool di oggetti per ottenere il bilanciamento delle prestazioni e delle risorse desiderate.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Monitoraggio delle statistiche degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e58946953ef1688dcb44223522cc58ccd1195f07ec0173a0b75413fe441195f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070461"
---
# <a name="monitoring-object-statistics"></a>Monitoraggio delle statistiche degli oggetti

È possibile monitorare le statistiche degli oggetti durante l'esecuzione di un'applicazione. In questo modo, è possibile ottimizzare le caratteristiche del pool di oggetti per ottenere il bilanciamento delle prestazioni e delle risorse desiderate.

È possibile monitorare lo stato per tutti gli oggetti configurati per supportare le statistiche degli oggetti e la creazione di report di eventi. L'abilitazione delle statistiche degli oggetti presenta un leggero sovraccarico delle prestazioni.

**Per abilitare le statistiche degli oggetti**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare e quindi scegliere **Proprietà.**

2.  Nella finestra di dialogo delle proprietà del componente fare clic **sulla scheda** Attivazione .

3.  Per abilitare le statistiche degli oggetti per il componente, in **Contesto di attivazione** selezionare la casella di controllo Componente che supporta **eventi** e statistiche.

**Per monitorare lo stato degli oggetti**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti aprire la cartella dell'applicazione che include i componenti da monitorare.

2.  Fare clic con il pulsante **destro del mouse** sulla cartella Componenti , scegliere **Visualizza**, quindi fare clic su **Visualizzazione stato**. Nel riquadro dei dettagli viene ora visualizzata la visualizzazione dello stato per tutti i componenti dell'applicazione. Nella tabella seguente vengono descritte le sei colonne della visualizzazione stato.

    

    | Colonna                        | Descrizione                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **ProgID**<br/>         | Identifica un componente specifico.<br/>                                                                                                                                                                                |
    | **Oggetti**<br/>        | Mostra il numero di oggetti attualmente utilizzati dai riferimenti client.<br/>                                                                                                                                       |
    | **Attivato**<br/>      | Mostra il numero di oggetti attualmente attivati. <br/>                                                                                                                                                      |
    | **In pool**<br/>         | Mostra il numero totale di oggetti creati dal pool, inclusi gli oggetti in uso e gli oggetti disattivati.<br/>                                                                                      |
    | **In chiamata**<br/>        | Identifica gli oggetti nella chiamata.<br/>                                                                                                                                                                                     |
    | **Ora chiamata (ms)**<br/> | Mostra la durata media delle chiamate al metodo (in millisecondi) effettuate negli ultimi 20 secondi (fino a 20 chiamate). Il tempo di chiamata viene misurato in corrispondenza dell'oggetto e non include il tempo usato per attraversare la rete.<br/> |

    

     

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione di un componente da creare in pool](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




