---
description: Internamente, un metafile è una matrice di strutture a lunghezza variabile denominate record metafile.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Informazioni sui metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753594"
---
# <a name="about-metafiles"></a>Informazioni sui metafile

Internamente, un metafile è una matrice di strutture a lunghezza variabile denominate *record metafile*. I primi record del metafile specificano informazioni generali, ad esempio la risoluzione del dispositivo in cui è stata creata l'immagine, le dimensioni dell'immagine e così via. I record rimanenti, che costituiscono la maggior parte dei metafile, corrispondono alle funzioni GDI (Graphics Device Interface) necessarie per tracciare l'immagine. Questi record vengono archiviati nel metafile dopo la creazione di un contesto di dispositivo metafile speciale. Questo contesto di dispositivo metafile viene quindi utilizzato per tutte le operazioni di disegno necessarie per la creazione dell'immagine. Quando il sistema elabora una funzione GDI associata a un controller di dominio metafile, converte la funzione nei dati appropriati e archivia questi dati in un record aggiunto al metafile.

Una volta completata un'immagine e l'ultimo record viene archiviato nel metafile, è possibile passare il metafile a un'altra applicazione per:

-   Uso degli Appunti
-   Incorporamento in un altro file
-   Archiviazione su disco
-   Riproduzione ripetuta

Un metafile viene *riprodotto* quando i relativi record vengono convertiti in comandi del dispositivo ed elaborati dal dispositivo appropriato.

Esistono due tipi di metafile:

-   [File di formato avanzato](enhanced-format-metafiles.md)
-   [Metafile in formato Windows](windows-format-metafiles.md)

 

 



