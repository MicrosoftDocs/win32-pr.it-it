---
description: La posizione, la velocità e l'orientamento delle origini audio e dei listener nello spazio 3D sono rappresentati da coordinate cartesiane, ovvero valori su tre assi, ovvero l'asse x, l'asse y e l'asse z.
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Coordinate dello spazio 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232297"
---
# <a name="coordinates-of-3d-space"></a>Coordinate dello spazio 3D

La posizione, la velocità e l'orientamento delle origini audio e dei listener nello spazio 3D sono rappresentati da coordinate cartesiane, ovvero valori su tre assi, ovvero l'asse x, l'asse y e l'asse z.

Gli assi sono relativi a un punto di vista stabilito dall'applicazione. I valori sull'asse x aumentano da sinistra verso destra, sull'asse y da giù verso l'alto e sull'asse z da vicino a lungo.

La **struttura \_ vettoriale X3DAUDIO** contiene valori che descrivono la posizione, la velocità o l'orientamento sui tre assi.

Convenzionalmente, i vettori sono espressi come tre valori racchiusi tra parentesi e separati da virgole, nell'ordine (x, y, z).

Per position, i valori si trovano in unità internazionali definite dall'utente.

Per velocità, il vettore descrive la frequenza di spostamento lungo ogni asse in unità internazionali al secondo.

Per l'orientamento, i valori sono in unità arbitrarie e sono relativi tra loro. Ad esempio, se la visualizzazione di base del mondo 3D si trova verso nord verso l'orizzonte e l'orientamento del listener è (-1, 0, 1), il listener viene rivolto a nordovest. Poiché i valori all'interno di un vettore non sono in unità assolute, il vettore può essere espresso in modo analogo (-5, 0, 5) o (-0,25, 0, 0,25).

i vettori 3D funzionano in modo analogo ai vettori 2D, ma con un asse aggiuntivo nella direzione di scorrimento. È possibile vedere in che modo i vettori funzionano nello spazio 2D disegnando questi ultimi in un foglio grafico. Lasciare che i valori aumentino dalla parte inferiore alla parte superiore della carta e da sinistra a destra. Una linea disegnata da (0,0) a (1,1) ha lo stesso orientamento, o direzione, di uno tracciato da (0, 0) a (5, 5). Tuttavia, la seconda riga indica una distanza o una velocità maggiore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti audio comuni](common-audio-concepts.md)
</dt> <dt>

[Panoramica di X3DAudio](x3daudio-overview.md)
</dt> </dl>

 

 



