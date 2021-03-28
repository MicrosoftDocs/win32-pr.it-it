---
description: Per modificare un'immagine archiviata in un metafile avanzato, è necessario che un'applicazione esegua le attività descritte nella procedura seguente.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Modifica di un metafile avanzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130783"
---
# <a name="editing-an-enhanced-metafile"></a>Modifica di un metafile avanzato

Per modificare un'immagine archiviata in un metafile avanzato, è necessario che un'applicazione esegua le attività descritte nella procedura seguente.

**Per modificare un'immagine archiviata in un metafile avanzato**

1.  Usare hit testing per acquisire le coordinate del cursore e recuperare la posizione dell'oggetto (riga, arco, rettangolo, ellisse, poligono o forma irregolare) che l'utente vuole modificare.
2.  Convertire queste coordinate in unità logiche (o internazionali).
3.  Chiamare la funzione [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) ed esaminare ogni record del metafile.
4.  Determinare se un record specificato corrisponde a una funzione di disegno GDI.
5.  In caso contrario, determinare se le coordinate archiviate nel record corrispondono alla riga, all'arco, all'ellisse o ad altro elemento grafico che interseca le coordinate specificate dall'utente.
6.  Quando si trova il record che corrisponde all'output che l'utente vuole modificare, cancellare l'oggetto sullo schermo che corrisponde al record originale.
7.  Eliminare il record corrispondente dal metafile, salvando un puntatore nella relativa posizione.
8.  Consente all'utente di ricreare o sostituire l'oggetto.
9.  Converte le funzioni GDI utilizzate per creare il nuovo oggetto in uno o più record di metafile avanzati.
10. Archiviare questi record nel metafile avanzato.

 

 



