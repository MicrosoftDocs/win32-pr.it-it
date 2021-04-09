---
description: Gli sviluppatori possono estendere l'infrastruttura WMI sviluppando provider WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Creazione di provider WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058345"
---
# <a name="creating-wmi-providers"></a><span data-ttu-id="c7cfc-103">Creazione di provider WMI</span><span class="sxs-lookup"><span data-stu-id="c7cfc-103">Creating WMI Providers</span></span>

<span data-ttu-id="c7cfc-104">Gli sviluppatori possono estendere l'infrastruttura WMI sviluppando provider WMI.</span><span class="sxs-lookup"><span data-stu-id="c7cfc-104">Developers can extend the WMI infrastructure by developing WMI providers.</span></span> <span data-ttu-id="c7cfc-105">I provider WMI sono oggetti COM che implementano un set specificato di interfacce e, fino a poco tempo, sono sempre implementate in C++.</span><span class="sxs-lookup"><span data-stu-id="c7cfc-105">WMI providers are COM objects that implement a specified set of interfaces and, until recently, were always implemented in C++.</span></span> <span data-ttu-id="c7cfc-106">È ora possibile utilizzare linguaggi gestiti come C# per implementare i provider WMI.</span><span class="sxs-lookup"><span data-stu-id="c7cfc-106">You can now use managed languages like C# to implement WMI providers.</span></span> <span data-ttu-id="c7cfc-107">La versione 3,5 di .NET Framework ha introdotto il framework delle estensioni del provider WMI che lo rende possibile.</span><span class="sxs-lookup"><span data-stu-id="c7cfc-107">Version 3.5 of the .NET framework introduced the WMI Provider Extensions framework that makes this possible.</span></span> <span data-ttu-id="c7cfc-108">Per ulteriori informazioni sulla creazione di provider WMI mediante tale Framework, vedere l'articolo relativo alla [scrittura di provider WMI associati mediante l'estensione WMI.NET del Provider 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c7cfc-108">To learn more about creating WMI providers by using that framework, read the article, [Writing coupled WMI providers using WMI.NET Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="c7cfc-109">È inoltre possibile creare un provider utilizzando Windows Management Infrastructure (MI), la versione di nuova generazione di WMI.</span><span class="sxs-lookup"><span data-stu-id="c7cfc-109">You can also create a provider using Windows Management Infrastructure (MI), the next-generation version of WMI.</span></span> <span data-ttu-id="c7cfc-110">Per ulteriori informazioni, vedere [How to implement a mi provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="c7cfc-110">For more information, see [How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span></span>

 

<span data-ttu-id="c7cfc-111">Nella tabella seguente viene descritto il contenuto di questa sezione.</span><span class="sxs-lookup"><span data-stu-id="c7cfc-111">The following table describes the contents in this section.</span></span>



| <span data-ttu-id="c7cfc-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="c7cfc-112">Topic</span></span>                                                      | <span data-ttu-id="c7cfc-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7cfc-113">Description</span></span>                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="c7cfc-114">Invio di dati a WMI</span><span class="sxs-lookup"><span data-stu-id="c7cfc-114">Providing Data to WMI</span></span>](providing-data-to-wmi.md)         | <span data-ttu-id="c7cfc-115">Viene fornita una panoramica dei passaggi necessari per la creazione di un provider WMI.</span><span class="sxs-lookup"><span data-stu-id="c7cfc-115">Provides an overview of the steps involved in creating a WMI provider.</span></span>         |
| [<span data-ttu-id="c7cfc-116">Sviluppo di un provider WMI</span><span class="sxs-lookup"><span data-stu-id="c7cfc-116">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md) | <span data-ttu-id="c7cfc-117">Descrive le attività che è necessario eseguire durante la creazione di diversi tipi di provider WMI.</span><span class="sxs-lookup"><span data-stu-id="c7cfc-117">Describes tasks you must perform when creating various types of WMI providers.</span></span> |



 

 

 
