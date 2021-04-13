---
description: Attivazione di code di componenti
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Attivazione di code di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401425"
---
# <a name="activating-component-queues"></a>Attivazione di code di componenti

La creazione di chiamate al metodo su un componente in coda non comporta l'esecuzione diretta del metodo. Il metodo di [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) esegue il marshalling e archivia le chiamate al metodo e i parametri in una coda in cui vengono recuperati ed eseguiti successivamente dal componente in coda. Diversamente dall'attivazione di un oggetto DCOM remoto, non viene creata un'istanza del componente in coda quando viene chiamato un metodo. Si tratta dell'idea di base per l'uso dei componenti in coda: non è necessario creare istanze dei componenti in coda contemporaneamente all'applicazione chiamante.

> [!Note]  
> Le descrizioni per l'attivazione di un'applicazione in coda presuppongono che l'applicazione sia contrassegnata come accodata e che la casella di controllo listener sia abilitata.

 

È possibile utilizzare lo scripting per avviare e arrestare un'applicazione in coda. È possibile inserire lo script sotto il controllo dell'utilità di pianificazione per eseguirlo come richiesto. Ad esempio, lo script può essere eseguito al riavvio del sistema se le applicazioni sono permanentemente disponibili. Se l'applicazione deve elaborare le transazioni in modalità batch, è possibile eseguire lo script in un determinato momento ogni giorno insieme a uno script di arresto per assicurarsi che l'elaborazione batch si arresti in un momento specifico.

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per avviare un'applicazione in coda, attenersi alla procedura seguente:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.

2.  Fare clic con il pulsante destro del mouse sull'applicazione di cui si desidera attivare la coda.

3.  Fare clic su **Start** (Avvia).

## <a name="visual-basic"></a>Visual Basic

Vedere l'esempio COMAdminCatalog. StartApplication.

## <a name="cc"></a>C/C++

Vedere l'esempio [**ICOMAdminCatalog:: StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo del moniker della coda](using-the-queue-moniker.md)
</dt> </dl>

 

 



