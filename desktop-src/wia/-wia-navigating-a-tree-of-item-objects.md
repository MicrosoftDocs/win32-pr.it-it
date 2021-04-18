---
description: 'Altre informazioni su: esplorazione di un albero di oggetti elemento'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Esplorazione di un albero di oggetti Item
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307344"
---
# <a name="navigating-a-tree-of-item-objects"></a>Esplorazione di un albero di oggetti Item

> [!Note]  
> Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA). Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Un'applicazione o uno script consente di spostarsi in un albero degli elementi del dispositivo Windows Image Acquisition (WIA) per individuare e selezionare le immagini nel dispositivo. Utilizzando questa tecnica, un'applicazione seleziona e acquisisce un'immagine senza utilizzare una finestra di dialogo.

Un dispositivo WIA viene rappresentato come elemento radice in una struttura ad albero di oggetti [**elemento**](-wia-item.md) . Gli elementi figlio nell'albero rappresentano cartelle e immagini per una fotocamera o i letti digitalizzazione per uno scanner.

Dopo la connessione a un dispositivo, chiamare la proprietà [**Children**](-wia-iwiadispatchitem-children.md) dell'oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo (l'elemento radice dell'albero) per ottenere una raccolta degli elementi figlio (le immagini o i letti di analisi) del dispositivo.

Enumerare la raccolta in modo ricorsivo, se necessario, per esplorare l'albero degli elementi.

 

 
