---
description: Un'applicazione esplora l'Windows di elementi di un dispositivo WIA (Image Acquisition) per trovare e selezionare le immagini in tale dispositivo. Usando questa tecnica, un'applicazione seleziona e acquisisce un'immagine senza presentare una finestra di dialogo all'utente.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Esplorazione di un albero degli elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a8ef11fc534a621c31461df897c8cc81f987ef83163a1300b0e392ce4f190e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593021"
---
# <a name="navigating-an-item-tree"></a>Esplorazione di un albero degli elementi

Un'applicazione esplora l'Windows di elementi di un dispositivo WIA (Image Acquisition) per trovare e selezionare le immagini in tale dispositivo. Usando questa tecnica, un'applicazione seleziona e acquisisce un'immagine senza presentare una finestra di dialogo all'utente.

Un dispositivo WIA è rappresentato come elemento radice in un albero di [**oggetti IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2.**](-wia-iwiaitem2.md) Gli elementi figlio nell'albero rappresentano immagini per una fotocamera o letti di scansione per uno scanner.

Dopo aver selezionato un dispositivo WIA, un'applicazione chiama il metodo [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) dell'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) del dispositivo per enumerare gli elementi figlio (immagini o letti di scansione) del dispositivo. Per istruzioni, vedere [Selezione di un dispositivo](-wia-selecting-a-device.md).

Il [**metodo IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) crea un oggetto di enumerazione per gli elementi figlio del dispositivo e restituisce un [**puntatore all'interfaccia IEnumWiaItem di**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) tale oggetto. L'applicazione può quindi usare i metodi **dell'interfaccia IEnumWiaItem** per ottenere puntatori agli elementi nell'albero degli elementi del dispositivo.

 

 



