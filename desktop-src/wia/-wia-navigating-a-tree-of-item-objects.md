---
description: 'Altre informazioni: Esplorazione di un albero di oggetti Item'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Esplorazione di una struttura ad albero di oggetti Item
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ec4d1cc43738d623ac3a1f60ba4950b1f9d98afa48025b80dfa935cd1004e99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393861"
---
# <a name="navigating-a-tree-of-item-objects"></a>Esplorazione di una struttura ad albero di oggetti Item

> [!Note]  
> Questo sistema di scripting è stato sostituito con Windows di automazione di acquisizione delle immagini (WIA). Vedere [Windows di automazione dell'acquisizione di immagini.](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

Un'applicazione o uno script esplora l'albero degli elementi Windows di un dispositivo WIA (Image Acquisition) per trovare e selezionare le immagini in tale dispositivo. Usando questa tecnica, un'applicazione seleziona e acquisisce un'immagine senza usare una finestra di dialogo.

Un dispositivo WIA è rappresentato come elemento radice in un albero di [**oggetti Item.**](-wia-item.md) Gli elementi figlio nell'albero rappresentano cartelle e immagini per una fotocamera o scansioni per uno scanner.

Dopo la connessione a un dispositivo, chiamare la proprietà [**Children**](-wia-iwiadispatchitem-children.md) dell'oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo (l'elemento radice dell'albero) per ottenere una raccolta degli elementi figlio (immagini o scansioni) del dispositivo.

Enumerare questa raccolta (in modo ricorsivo, se necessario) per esplorare l'albero degli elementi.

 

 
