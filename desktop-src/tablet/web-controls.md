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
# <a name="web-controls"></a><span data-ttu-id="483f1-103">Controlli Web</span><span class="sxs-lookup"><span data-stu-id="483f1-103">Web Controls</span></span>

<span data-ttu-id="483f1-104">Un modo per creare applicazioni Web abilitate per l'input penna consiste nell'inserire Windows Form controlli all'interno di awebpagewithin Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="483f1-104">One way to create ink-enabled Web applications is to put Windows Forms controls inside awebpagewithin Microsoft Internet Explorer.</span></span> <span data-ttu-id="483f1-105">Per un'esercitazione efficace su questa tecnica, vedere [utilizzo di controlli Windows Form in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span><span class="sxs-lookup"><span data-stu-id="483f1-105">A good tutorial on this technique can be found at [Using Windows Forms Controls in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span></span> <span data-ttu-id="483f1-106">Di seguito sono riportati i passaggi di base dell'esercitazione:</span><span class="sxs-lookup"><span data-stu-id="483f1-106">The basic steps in the tutorial are:</span></span>

1.  <span data-ttu-id="483f1-107">Creare un controllo che erediti da [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="483f1-107">Create a control that inherits from [**System.Windows.Forms.UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span></span>
2.  <span data-ttu-id="483f1-108">Creare una pagina HTML con un tag oggetto che fa riferimento a tale UserControl.</span><span class="sxs-lookup"><span data-stu-id="483f1-108">Create an HTML page with an object tag that refers to that UserControl.</span></span>
3.  <span data-ttu-id="483f1-109">Creare una directory virtuale e impostare le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="483f1-109">Create a virtual directory and set permissions.</span></span>
4.  <span data-ttu-id="483f1-110">Caricare l'URL della pagina HTML nel browser.</span><span class="sxs-lookup"><span data-stu-id="483f1-110">Load the URL of the HTML page into the browser.</span></span>

<span data-ttu-id="483f1-111">Questa tecnica può essere applicata ai controlli abilitati per l'input penna, esattamente come qualsiasi altro [**controllo**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)Windows Form.</span><span class="sxs-lookup"><span data-stu-id="483f1-111">This technique can be applied to ink-enabled controls, just like any other Windows Forms [**Control**](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="483f1-112">Infatti, la tecnica può essere usata con qualsiasi classe nel Framework Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="483f1-112">In fact, the technique can be used with any class in the Microsoft .NET Framework.</span></span> <span data-ttu-id="483f1-113">Gli esempi forniti da Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) includono una versione di controllo Web dell'esempio auto Claims nella sezione Ink Web Samples.</span><span class="sxs-lookup"><span data-stu-id="483f1-113">The samples provided by the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) include a Web control version of the Auto Claims sample in the Ink Web Samples section.</span></span> <span data-ttu-id="483f1-114">Questo esempio utilizza l'esempio originale del [modulo Claims automatico](auto-claims-form-sample.md) e lo trasforma in un controllo inserito in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="483f1-114">This example takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span> <span data-ttu-id="483f1-115">Per ulteriori informazioni sull'abilitazione di questo esempio per il Web, vedere l' [esempio di controllo Web di input penna](ink-web-control-sample.md).</span><span class="sxs-lookup"><span data-stu-id="483f1-115">For more information about Web-enabling this sample, see the [Ink Web Control Sample](ink-web-control-sample.md).</span></span>

> [!Note]  
> <span data-ttu-id="483f1-116">Quando si distribuisce un'applicazione creata con .NET sul Web, l'applicazione potrebbe essere interessata dal modello di sicurezza per .NET.</span><span class="sxs-lookup"><span data-stu-id="483f1-116">When you deploy an application created by using .NET over the Web, the application may be affected by security model for .NET.</span></span> <span data-ttu-id="483f1-117">Per ulteriori informazioni sul funzionamento della sicurezza con le applicazioni Web abilitate per l'input penna, vedere [sicurezza e attendibilità](security-and-trust.md).</span><span class="sxs-lookup"><span data-stu-id="483f1-117">For more information about how security works with ink-enabled Web applications, see [Security and Trust](security-and-trust.md).</span></span>

 

 

 
