---
description: Bump mapping è una forma speciale di mapping dell'ambiente speculare o diffuso che simula i riflessi degli oggetti tassellati senza richiedere conteggi di poligoni estremamente elevati.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Bump mapping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127390"
---
# <a name="bump-mapping-direct3d-9"></a>Bump mapping (Direct3D 9)

Bump mapping è una forma speciale di mapping dell'ambiente speculare o diffuso che simula i riflessi degli oggetti tassellati senza richiedere conteggi di poligoni estremamente elevati. Il mapping di Bump implementato da Direct3D può essere descritto accuratamente come una coordinata di trama per ogni pixel di mappe dell'ambiente speculare o diffusa, perché vengono fornite informazioni sul contorno della mappa a urto in termini di valori Delta, che il sistema applica alle coordinate di trama utente e v di una mappa dell'ambiente nella successiva fase della trama. I valori delta vengono codificati nel formato pixel della superficie della mappa di Bump (vedere la pagina relativa ai [formati dei pixel di bump map](bump-map-pixel-formats.md)).

Il mapping di Bump si basa sulla fusione di più trame. Ciò significa che il dispositivo deve supportare almeno due fasi di fusione. uno per la mappa bump e l'altro per una mappa dell'ambiente. Per applicare una mappa di trama di base aggiuntiva, ovvero il caso più comune, sono necessarie almeno tre fasi di combinazione di trame. Il diagramma seguente illustra le relazioni tra la trama di base, la mappa a urto e la mappa dell'ambiente nella trama a cascata.

![diagramma della fusione di trama a cascata](images/bumpmap-tcascade.png)

È necessario preparare le fasi di trama in modo appropriato per abilitare il mapping di Bump. Gli argomenti seguenti introducono il mapping di bump e forniscono informazioni dettagliate su come è possibile usarlo nelle applicazioni:

-   [Formati pixel della mappa Bump](bump-map-pixel-formats.md)
-   [Formule di mapping Bump](bump-mapping-formulas.md)
-   [Uso di bump mapping](using-bump-mapping.md)

Direct3D non supporta in modo nativo i mapping di altezza; sono semplicemente un formato semplice in cui archiviare e visualizzare i dati di contorno. L'applicazione può archiviare le informazioni di contorno in qualsiasi formato o persino generare una mappa Bump procedurale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline pixel](pixel-pipeline.md)
</dt> </dl>

 

 



