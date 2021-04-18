---
description: Quando si creano scene 3D, un'applicazione può a volte ottenere vantaggi in termini di prestazioni tramite il rendering di oggetti 2D in modo da renderli apparentemente oggetti 3D. Si tratta dell'idea fondamentale dietro la tecnica di affissione.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Billboard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305309"
---
# <a name="billboarding-direct3d-9"></a>Billboard (Direct3D 9)

Quando si creano scene 3D, un'applicazione può a volte ottenere vantaggi in termini di prestazioni tramite il rendering di oggetti 2D in modo da renderli apparentemente oggetti 3D. Si tratta dell'idea fondamentale dietro la tecnica di affissione.

Un cartellone nel normale senso della parola è un segno lungo una carreggiata. Le applicazioni Microsoft Direct3D possono creare ed eseguire il rendering di questo tipo di Billboard definendo un solido rettangolare e applicando una trama a essa. Il tabellone nel senso più specializzato della grafica 3D è un'estensione di questo. L'obiettivo consiste nel creare oggetti 2D che risultino 3D. La tecnica consiste nell'applicare una trama che contiene l'immagine dell'oggetto a una primitiva rettangolare. La primitiva viene ruotata in modo che faccia sempre fronte all'utente. Non è importante se l'immagine dell'oggetto non è rettangolare. È possibile rendere trasparente parti del cartellone, quindi le parti dell'immagine di Billboard che non si vuole visualizzare non sono visibili.

Molti giochi impiegano il tabellone per gli sprite animati. Ad esempio, quando l'utente si muove in un labirinto 3D, può visualizzare le armi o i ricompense che possono essere prelevati. Si tratta in genere di immagini 2D con trama su una primitiva rettangolare. Il tabellone viene spesso usato nei giochi per il rendering di immagini di alberi, cespugli e cloud.

Quando un'immagine viene applicata a un tabellone, la primitiva rettangolare deve prima essere ruotata in modo che l'immagine risultante faccia fronte all'utente. L'applicazione deve quindi tradurla in posizione. L'applicazione può quindi applicare una trama alla primitiva.

Il tabellone funziona meglio per gli oggetti simmetrici, in particolare gli oggetti simmetrici lungo l'asse verticale. Richiede inoltre che l'altitudine del punto di vista non aumenti eccessivamente. Se l'utente è autorizzato a visualizzare il tabellone indicato sopra, diventa immediatamente evidente che l'oggetto è 2D anziché 3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Alpha](alpha-examples.md)
</dt> </dl>

 

 



