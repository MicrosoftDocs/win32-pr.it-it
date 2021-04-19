---
title: Direct2D non supporta il rendering in metafile avanzati in Internet Explorer 9
description: Direct2D non supporta il rendering in metafile avanzati in Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314824"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D non supporta il rendering in metafile avanzati in Internet Explorer 9

## <a name="platforms"></a>Piattaforme

**Client** : Windows Vista, Windows 7, Windows 8  
**Server** : windows Server 2008, windows Server 2008 R2, windows Server 2012  




## <a name="description"></a>Descrizione

A causa delle modifiche di rendering interne in Internet Explorer 9, le API [IHTMLElementRender::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) e [IViewObject::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) creeranno ora un metafile contenente un'unica bitmap che rappresenta il contenuto Web invece di un metafile completo contenente informazioni sul testo e sul vettore. Questa modifica era dovuta al passaggio dal rendering GDI al rendering Direct2D con accelerazione hardware (D2D).

Questa modifica influiscono sulle app che usano queste API e si basa su informazioni sul testo o sul vettore nel metafile.

## <a name="manifestation"></a>Manifestazione

A seconda dell'app interessata da questa modifica, gli utenti potrebbero vedere un comportamento danneggiato o errato nelle app.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Le app che devono solo estrarre informazioni di testo da un documento Web (senza informazioni di posizionamento) possono usare la proprietà [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) per estrarre il testo.

Le app che usano IViewObject::D RAW possono usare la [funzionalità \_ IVIEWOBJECTDRAW \_ DMLT9 \_ con \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) la chiave di controllo della funzionalità GDI per ripristinare il rendering GDI se la modalità documento è la seguente:

-   È minore o uguale a 8
-   Il FCK autorizza l'host a usare GDI
-   E un controller di dominio metafile viene passato all'API

## <a name="resources"></a>Risorse

-   [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject::D RAW](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [Proprietà IHTMLElement:: innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Controlli delle funzionalità Internet (I.. L](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 