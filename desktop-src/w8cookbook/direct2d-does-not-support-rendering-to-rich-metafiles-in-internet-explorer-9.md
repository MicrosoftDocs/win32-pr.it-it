---
title: Direct2D non supporta il rendering in metafile rtf in Internet Explorer 9
description: Direct2D non supporta il rendering in metafile rtf in Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebe10310202385fa4e9458cb1a442cbf98a3f6f178331d888c096449631ca61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057351"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D non supporta il rendering in metafile rtf in Internet Explorer 9

## <a name="platforms"></a>Piattaforme

**Client:** Windows Vista, Windows 7, Windows 8  
**Server** : Windows Server 2008, Windows Server 2008 R2, Windows Server 2012  




## <a name="description"></a>Descrizione

A causa delle modifiche interne al rendering in Internet Explorer 9, le API [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) e [IViewObject::D raw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) creeranno ora un metafile contenente una singola bitmap che rappresenta il contenuto Web anziché un metafile avanzato contenente testo e informazioni vettoriali. Questa modifica è dovuta al passaggio dal rendering GDI al rendering Direct2D (D2D) con accelerazione hardware.

Questa modifica influisce sulle app che usano queste API e si basano su informazioni di testo o vettoriali nel metafile.

## <a name="manifestation"></a>Manifestazione

A seconda dell'app interessata da questa modifica, gli utenti potrebbero vedere un comportamento errato o interrotto nelle app.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Le app che devono estrarre solo informazioni di testo da un documento Web (senza informazioni di posizionamento) possono usare la [proprietà innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) per estrarre il testo.

Le app che usano IViewObject::D raw possono usare il tasto di controllo della funzionalità [FEATURE \_ IVIEWOBJECTDRAW \_ DMLT9 \_ WITH GDI \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) per ripristinare il rendering GDI se la modalità documento:

-   È minore o uguale a 8
-   Il FCK autorizza l'host all'uso di GDI
-   E un controller di dominio metafile viene passato all'API

## <a name="resources"></a>Risorse

-   [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject::D raw](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [Proprietà IHTMLElement::innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Internet Feature Controls (I., controlli delle funzionalità Internet) L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 