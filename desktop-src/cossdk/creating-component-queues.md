---
description: Un'applicazione che contiene almeno un componente accodabile può essere contrassegnata come accodata tramite lo strumento di amministrazione Servizi componenti.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Creazione di code di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c44f670cea15e1cb1a4549d5c1e847956eb41d400ae01d557803dbd1ce2b439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793461"
---
# <a name="creating-component-queues"></a>Creazione di code di componenti

Un'applicazione che contiene almeno un componente accodabile può essere contrassegnata come accodata tramite lo strumento di amministrazione Servizi componenti.

Quando un'applicazione viene contrassegnata come in coda, COM+ crea automaticamente una coda di accodamento messaggi per l'applicazione. Il nome della coda è il nome dell'applicazione. Se il nome della coda corrisponde al nome di una coda esistente, COM+ userà la coda esistente.

> [!Note]  
> Il parametro PathName di *Accodamento* messaggi è una combinazione del nome del server remoto (RSN) e del nome dell'applicazione COM+. L'RSN fa riferimento alla destinazione di un'attivazione remota. Si specifica un RSN durante l'installazione di un'applicazione client esportabile in un computer client. La procedura di installazione usa l'RSN per indirizzare l'attivazione a un computer client specificato. Per altre informazioni sui nomi delle code, vedere la tabella dei parametri nella sezione "Parametri del moniker della coda" in [Uso del moniker della coda](using-the-queue-moniker.md).

 

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per specificare un'applicazione COM+ come in coda, seguire questa procedura:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in Servizi componenti **aprire** la cartella **Applicazioni COM+** associata al computer da gestire.

2.  Fare clic con il pulsante destro del mouse sull'applicazione per cui si desidera creare una coda e quindi **scegliere Proprietà.**

3.  Selezionare la **scheda Accodamento** nella finestra di dialogo delle proprietà.

4.  Attivare la casella di controllo **Queued : questa applicazione può essere raggiunta dalle code MSMQ**.

    > [!Note]  
    > Se la **casella di controllo** In coda è disattivata, l'applicazione non contiene componenti accodabili.

     

5.  Fare clic su **OK**.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Non è valida.

## <a name="remarks"></a>Commenti

Le code create dalla libreria di amministrazione COM+ o dallo strumento di amministrazione Servizi componenti sono contrassegnate con l'attributo transazionale Accodamento messaggi.

Dopo l'installazione nel server, un'applicazione in coda può essere resa disponibile ai client esportando l'applicazione e quindi importando l'applicazione in ogni client.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di componenti accodamento](creating-queuable-components.md)
</dt> <dt>

[Architettura dei componenti in coda](queued-components-architecture.md)
</dt> </dl>

 

 



