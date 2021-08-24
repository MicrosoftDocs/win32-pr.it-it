---
description: Tracciati curvi
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Tracciati curvi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58018b7ef95b30c5ae2751ed963caefee7b9313ca86a8c6a2a4fee246908f8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849181"
---
# <a name="curved-paths"></a>Tracciati curvi

Un'applicazione può appiattire le curve in un percorso chiamando la [**funzione FlattenPath.**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) Questa funzione è particolarmente utile per le applicazioni che adattano il testo al contorno di un tracciato che contiene curve. Per adattare il testo, l'applicazione deve eseguire la procedura seguente:

1.  Creare il percorso in cui viene visualizzato il testo.
2.  Chiamare la [**funzione FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) per convertire le curve di un tracciato in segmenti di linea.
3.  Chiamare la [**funzione GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) per recuperare i segmenti di linea.
4.  Calcolare la lunghezza di ogni riga e la larghezza di ogni carattere nella stringa.
5.  Usare i dati di larghezza di riga e di caratteri per posizionare ogni carattere lungo la curva.

 

 



