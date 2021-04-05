---
title: Visualizzazione di finestre di dialogo
description: Visualizzazione di finestre di dialogo
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player Online Stores, visualizzazione di finestre di dialogo
- archivi online, visualizzazione di finestre di dialogo
- digitare 1 archivi online, visualizzare le finestre di dialogo
- Windows Media Player Online Stores, finestre di dialogo
- archivi online, finestre di dialogo
- digitare 1 archivi online, finestre di dialogo
- visualizzazione di finestre di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723511"
---
# <a name="displaying-dialog-boxes"></a>Visualizzazione di finestre di dialogo

L'archivio online può richiamare le finestre di dialogo tramite Media Player di Windows. A tale scopo, chiamare [External. ShowPopup](external-showpopup.md) dal codice dello script della pagina di individuazione, fornendo un valore di indice personalizzato che rappresenta la finestra di dialogo da visualizzare. Il valore di indice è significativo solo per il codice del negozio online; Windows Media Player non interpreta questo valore. Windows Media Player chiama quindi [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo \_ PopupURL per il parametro *bstrInfoName* e il numero di indice per il parametro *pContext* . Il plug-in restituisce quindi un **BSTR** contenente l'URL della pagina Web da visualizzare nella finestra di dialogo e il lettore Visualizza la finestra di dialogo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi di tipo 1 online**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




