---
description: Un modo per creare applicazioni Web abilitate per l'input penna consiste nell'inserire Windows Form controlli all'interno di awebpagewithin Microsoft Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Controlli Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306704"
---
# <a name="web-controls"></a>Controlli Web

Un modo per creare applicazioni Web abilitate per l'input penna consiste nell'inserire Windows Form controlli all'interno di awebpagewithin Microsoft Internet Explorer. Per un'esercitazione efficace su questa tecnica, vedere [utilizzo di controlli Windows Form in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx). Di seguito sono riportati i passaggi di base dell'esercitazione:

1.  Creare un controllo che erediti da [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).
2.  Creare una pagina HTML con un tag oggetto che fa riferimento a tale UserControl.
3.  Creare una directory virtuale e impostare le autorizzazioni.
4.  Caricare l'URL della pagina HTML nel browser.

Questa tecnica può essere applicata ai controlli abilitati per l'input penna, esattamente come qualsiasi altro [**controllo**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)Windows Form. Infatti, la tecnica può essere usata con qualsiasi classe nel Framework Microsoft .NET. Gli esempi forniti da Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) includono una versione di controllo Web dell'esempio auto Claims nella sezione Ink Web Samples. Questo esempio utilizza l'esempio originale del [modulo Claims automatico](auto-claims-form-sample.md) e lo trasforma in un controllo inserito in una pagina Web. Per ulteriori informazioni sull'abilitazione di questo esempio per il Web, vedere l' [esempio di controllo Web di input penna](ink-web-control-sample.md).

> [!Note]  
> Quando si distribuisce un'applicazione creata con .NET sul Web, l'applicazione potrebbe essere interessata dal modello di sicurezza per .NET. Per ulteriori informazioni sul funzionamento della sicurezza con le applicazioni Web abilitate per l'input penna, vedere [sicurezza e attendibilità](security-and-trust.md).

 

 

 
