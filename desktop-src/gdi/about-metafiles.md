---
description: Internamente, un metafile è una matrice di strutture a lunghezza variabile denominata record di metafile.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Informazioni sui metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc573d54f1f89e2dfe06edb8e225516fe8f0946485592d7d6aaea1faa651de85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779461"
---
# <a name="about-metafiles"></a>Informazioni sui metafile

Internamente, un metafile è una matrice di strutture a lunghezza variabile denominata *record di metafile.* I primi record nel metafile specificano informazioni generali, ad esempio la risoluzione del dispositivo in cui è stata creata l'immagine, le dimensioni dell'immagine e così via. I record rimanenti, che costituiscono la maggior parte di qualsiasi metafile, corrispondono alle funzioni GDI (Graphics Device Interface) necessarie per disegnare l'immagine. Questi record vengono archiviati nel metafile dopo la creazione di un contesto di dispositivo metafile speciale. Questo contesto di dispositivo metafile viene quindi usato per tutte le operazioni di disegno necessarie per creare l'immagine. Quando il sistema elabora una funzione GDI associata a un controller di dominio metafile, converte la funzione nei dati appropriati e li archivia in un record aggiunto al metafile.

Dopo aver completato un'immagine e aver archiviato l'ultimo record nel metafile, è possibile passare il metafile a un'altra applicazione:

-   Uso degli Appunti
-   Incorporamento all'interno di un altro file
-   Archiviazione su disco
-   Riproduzione ripetuta

Un metafile viene *riprodotto* quando i record vengono convertiti in comandi del dispositivo ed elaborati dal dispositivo appropriato.

Esistono due tipi di metafile:

-   [Metafile in formato avanzato](enhanced-format-metafiles.md)
-   [Windows metafile in formato 1](windows-format-metafiles.md)

 

 



