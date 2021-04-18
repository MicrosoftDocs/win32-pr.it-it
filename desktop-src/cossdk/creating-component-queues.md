---
description: Un'applicazione che contiene almeno un componente accodabile può essere contrassegnata come accodata utilizzando lo strumento di amministrazione Servizi componenti.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Creazione di code di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304830"
---
# <a name="creating-component-queues"></a>Creazione di code di componenti

Un'applicazione che contiene almeno un componente accodabile può essere contrassegnata come accodata utilizzando lo strumento di amministrazione Servizi componenti.

Quando un'applicazione è contrassegnata come accodata, COM+ crea automaticamente una coda di Accodamento messaggi. Il nome della coda è il nome dell'applicazione. Se il nome della coda corrisponde al nome di una coda esistente, COM+ utilizzerà la coda esistente.

> [!Note]  
> Il parametro del *percorso* di Accodamento messaggi è una combinazione del nome del server remoto (RSN) e del nome dell'applicazione com+. RSN fa riferimento alla destinazione di un'attivazione remota. Si specifica un RSN durante l'installazione di un'applicazione client esportabile in un computer client. La procedura di installazione usa RSN per indirizzare l'attivazione a un computer client specifico. Per ulteriori informazioni sui nomi delle code, fare riferimento alla tabella di parametri nella sezione "parametri del moniker della coda" in [utilizzo del moniker della coda](using-the-queue-moniker.md).

 

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per specificare un'applicazione COM+ come accodata, attenersi alla procedura seguente:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.

2.  Fare clic con il pulsante destro del mouse sull'applicazione per la quale si desidera creare una coda e quindi scegliere **Proprietà**.

3.  Selezionare la scheda **Accodamento** nella finestra di dialogo Proprietà.

4.  Attivare la casella **di controllo in coda: questa applicazione può essere raggiunta dalle code MSMQ**.

    > [!Note]  
    > Se la casella di controllo in **coda** è disabilitata, l'applicazione non contiene componenti accodabili.

     

5.  Fare clic su **OK**.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Non è valida.

## <a name="remarks"></a>Commenti

Le code create dalla libreria di amministrazione COM+ o dallo strumento di amministrazione Servizi componenti sono contrassegnate con l'attributo transazionale di Accodamento messaggi.

Dopo l'installazione di un'applicazione in coda nel server, è possibile renderla disponibile ai client esportando l'applicazione e quindi importando l'applicazione in ogni client.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di componenti accodabili](creating-queuable-components.md)
</dt> <dt>

[Architettura dei componenti in coda](queued-components-architecture.md)
</dt> </dl>

 

 



