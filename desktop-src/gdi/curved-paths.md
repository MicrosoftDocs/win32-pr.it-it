---
description: Percorsi curvi
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Percorsi curvi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880318"
---
# <a name="curved-paths"></a>Percorsi curvi

Un'applicazione può appiattire le curve in un percorso chiamando la funzione [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) . Questa funzione è particolarmente utile per le applicazioni che soddisfano il testo nel contorno di un tracciato che contiene curve. Per adattarsi al testo, l'applicazione deve eseguire i passaggi seguenti:

1.  Creare il percorso in cui viene visualizzato il testo.
2.  Chiamare la funzione [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) per convertire le curve in un percorso in segmenti di linea.
3.  Chiamare la funzione [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) per recuperare i segmenti di linea.
4.  Calcolare la lunghezza di ogni riga e la larghezza di ogni carattere nella stringa.
5.  Usare i dati di larghezza riga e carattere per posizionare ogni carattere lungo la curva.

 

 



