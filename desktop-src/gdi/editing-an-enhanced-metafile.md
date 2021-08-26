---
description: Per modificare un'immagine archiviata in un metafile avanzato, un'applicazione deve eseguire le attività descritte nella procedura seguente.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Modifica di un metafile avanzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a052be915d966d90a0189376de7e1ff6e27831ebc9c44a0ff6af266b37fa65f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015581"
---
# <a name="editing-an-enhanced-metafile"></a>Modifica di un metafile avanzato

Per modificare un'immagine archiviata in un metafile avanzato, un'applicazione deve eseguire le attività descritte nella procedura seguente.

**Per modificare un'immagine archiviata in un metafile avanzato**

1.  Usare l'hit testing per acquisire le coordinate del cursore e recuperare la posizione dell'oggetto (linea, arco, rettangolo, ellisse, poligono o forma irregolare) che l'utente vuole modificare.
2.  Convertire queste coordinate in unità logiche (o globali).
3.  Chiamare la [**funzione EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) ed esaminare ogni record di metafile.
4.  Determinare se un record specificato corrisponde a una funzione di disegno GDI.
5.  In caso contrario, determinare se le coordinate archiviate nel record corrispondono alla linea, all'arco, all'ellisse o a un altro elemento grafico che interseca le coordinate specificate dall'utente.
6.  Dopo aver trovato il record corrispondente all'output che l'utente vuole modificare, cancellare l'oggetto sullo schermo che corrisponde al record originale.
7.  Eliminare il record corrispondente dal metafile, salvando un puntatore nella relativa posizione.
8.  Consente all'utente di ridisegnare o sostituire l'oggetto .
9.  Convertire le funzioni GDI usate per disegnare il nuovo oggetto in uno o più record di metafile avanzato.
10. Archiviare questi record nel metafile avanzato.

 

 



