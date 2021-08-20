---
description: Un modo per creare applicazioni Web abilitate per l'input penna è inserire i Windows Form all'interno di awebpagecon Microsoft Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Controlli Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3abd7dd40bdeed36bff437e76d2e2aeaa64688f89a0d3bafff34ee8314833b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041693"
---
# <a name="web-controls"></a>Controlli Web

Un modo per creare applicazioni Web abilitate per l'input penna è inserire i Windows Form all'interno di awebpagecon Microsoft Internet Explorer. Una buona esercitazione su questa tecnica è disponibile in [Using Windows Forms Controls in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx). I passaggi di base dell'esercitazione sono:

1.  Creare un controllo che eredita da [**System.Windows. Forms.UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).
2.  Creare una pagina HTML con un tag di oggetto che fa riferimento a tale UserControl.
3.  Creare una directory virtuale e impostare le autorizzazioni.
4.  Caricare l'URL della pagina HTML nel browser.

Questa tecnica può essere applicata ai controlli abilitati per l'input penna, esattamente come qualsiasi altro Windows [**Form.**](/dotnet/api/system.windows.forms.control?view=netcore-3.1) In realtà, la tecnica può essere usata con qualsiasi classe in Microsoft .NET Framework. Gli esempi forniti da Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) includono una versione di controllo Web dell'esempio di attestazioni automatica nella sezione Ink Web Samples (Esempi Web ink). In questo esempio viene utilizzato [l'esempio](auto-claims-form-sample.md) di form di attestazioni automatico originale e lo si trasforma in un controllo inserito in una pagina Web. Per altre informazioni sull'abilitazione web di questo esempio, vedere [Ink Web Control Sample](ink-web-control-sample.md).

> [!Note]  
> Quando si distribuisce un'applicazione creata usando .NET sul Web, l'applicazione potrebbe essere interessata dal modello di sicurezza per .NET. Per altre informazioni sul funzionamento della sicurezza con le applicazioni Web abilitate per l'input penna, vedere [Sicurezza e attendibilità.](security-and-trust.md)

 

 

 
