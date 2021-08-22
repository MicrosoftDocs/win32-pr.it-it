---
title: Visualizzazione di finestre di dialogo
description: Visualizzazione di finestre di dialogo
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player negozi online, visualizzazione di finestre di dialogo
- negozi online, visualizzazione di finestre di dialogo
- tipo 1 negozi online, visualizzazione di finestre di dialogo
- Windows Media Player negozi online, finestre di dialogo
- negozi online, finestre di dialogo
- tipo 1 negozi online, finestre di dialogo
- visualizzazione di finestre di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e71d177e7675822b1f2704bf62776e598c2e817d583020b0df962347dac4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997271"
---
# <a name="displaying-dialog-boxes"></a>Visualizzazione di finestre di dialogo

Lo store online può richiamare finestre di dialogo tramite Windows Media Player. A tale scopo, chiamare [External.showPopup](external-showpopup.md) dal codice script della pagina di individuazione, fornendo un valore di indice personalizzato che rappresenta la finestra di dialogo da visualizzare. Questo valore di indice ha significato solo per il codice del negozio online; Windows Media Player non interpreta questo valore. Windows Media Player chiama quindi [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo PopupURL per il \_ parametro *bstrInfoName* e il numero di indice per il *parametro pContext.* Il plug-in restituisce quindi un **BSTR** contenente l'URL della pagina Web da visualizzare nella finestra di dialogo e player visualizza la finestra di dialogo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi online di tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




