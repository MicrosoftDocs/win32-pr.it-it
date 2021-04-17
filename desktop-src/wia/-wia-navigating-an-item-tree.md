---
description: Un'applicazione consente di spostarsi in un albero degli elementi del dispositivo Windows Image Acquisition (WIA) per individuare e selezionare le immagini nel dispositivo. Utilizzando questa tecnica, un'applicazione seleziona e acquisisce un'immagine senza presentare una finestra di dialogo all'utente.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Esplorazione di un albero di elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526431"
---
# <a name="navigating-an-item-tree"></a>Esplorazione di un albero di elementi

Un'applicazione consente di spostarsi in un albero degli elementi del dispositivo Windows Image Acquisition (WIA) per individuare e selezionare le immagini nel dispositivo. Utilizzando questa tecnica, un'applicazione seleziona e acquisisce un'immagine senza presentare una finestra di dialogo all'utente.

Un dispositivo WIA viene rappresentato come elemento radice in una struttura ad albero di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) . Gli elementi figlio nell'albero rappresentano le immagini per una fotocamera o i letti digitalizzazione per uno scanner.

Dopo aver selezionato un dispositivo WIA, un'applicazione chiama il metodo [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) dell'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) del dispositivo per enumerare gli elementi figlio (le immagini o i letti di analisi) del dispositivo. Per istruzioni, vedere [selezione di un dispositivo](-wia-selecting-a-device.md).

Il metodo [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) crea un oggetto di enumerazione per gli elementi figlio del dispositivo e restituisce un puntatore all'interfaccia [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) dell'oggetto. L'applicazione può quindi usare i metodi dell'interfaccia **IEnumWiaItem** per ottenere i puntatori agli elementi nell'albero degli elementi del dispositivo.

 

 



