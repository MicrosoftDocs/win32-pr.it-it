---
description: Windows Image Acquisition (WIA) fornisce oggetti di automazione da utilizzare nei linguaggi di scripting, ad esempio Microsoft JScript e il software di sviluppo Microsoft Visual Basic Scripting Edition (VBScript) e linguaggi di programmazione di alto livello, ad esempio Microsoft Visual Basic Development System.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modello di scripting WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307306"
---
# <a name="wia-scripting-model"></a><span data-ttu-id="bc5fc-103">Modello di scripting WIA</span><span class="sxs-lookup"><span data-stu-id="bc5fc-103">WIA Scripting Model</span></span>

<span data-ttu-id="bc5fc-104">Windows Image Acquisition (WIA) fornisce oggetti di automazione da utilizzare nei linguaggi di scripting, ad esempio Microsoft JScript e il software di sviluppo Microsoft Visual Basic Scripting Edition (VBScript) e linguaggi di programmazione di alto livello, ad esempio Microsoft Visual Basic Development System.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-104">Windows Image Acquisition (WIA) provides automation objects for use in scripting languages, such as Microsoft JScript and Microsoft Visual Basic Scripting Edition (VBScript) development software, and high-level programming languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="bc5fc-105">Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="bc5fc-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="bc5fc-106">Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="bc5fc-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="bc5fc-107">Nella tabella seguente vengono descritti gli oggetti di scripting WIA e il modo in cui vengono utilizzati.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-107">The following table describes WIA scripting objects and how they are used.</span></span> 

| <span data-ttu-id="bc5fc-108">Oggetto</span><span class="sxs-lookup"><span data-stu-id="bc5fc-108">Object</span></span>                                | <span data-ttu-id="bc5fc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc5fc-109">Description</span></span>                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc5fc-110">**WIA**</span><span class="sxs-lookup"><span data-stu-id="bc5fc-110">**Wia**</span></span>](-wia-wia.md)               | <span data-ttu-id="bc5fc-111">Oggetto di scripting WIA di primo livello.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-111">The top-level WIA scripting object.</span></span> <span data-ttu-id="bc5fc-112">Usare l'oggetto [**WIA**](-wia-wia.md) per enumerare e connettersi ai dispositivi e per gestire gli eventi del dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-112">Use the [**Wia**](-wia-wia.md) object to enumerate and connect to devices, and to handle hardware device events.</span></span>                                        |
| [<span data-ttu-id="bc5fc-113">**DeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="bc5fc-113">**DeviceInfo**</span></span>](-wia-deviceinfo.md) | <span data-ttu-id="bc5fc-114">L'oggetto [**deviceInfo**](-wia-deviceinfo.md) fornisce l'accesso alle informazioni sulle proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-114">The [**DeviceInfo**](-wia-deviceinfo.md) object provides access to information about device properties.</span></span>                                                                                     |
| [<span data-ttu-id="bc5fc-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bc5fc-115">**Item**</span></span>](-wia-item.md)             | <span data-ttu-id="bc5fc-116">Questo oggetto rappresenta gli elementi WIA del dispositivo, del file e della cartella.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-116">This object represents WIA device, file, and folder items.</span></span> <span data-ttu-id="bc5fc-117">Un dispositivo hardware WIA, le relative immagini o i letti di analisi sono rappresentati come albero gerarchico di oggetti [**elemento**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="bc5fc-117">A WIA hardware device and its images or scanning beds is represented as a hierarchical tree of [**Item**](-wia-item.md) objects.</span></span> |



 

<span data-ttu-id="bc5fc-118">Sia l'oggetto [**deviceInfo**](-wia-deviceinfo.md) che l'oggetto [**Item**](-wia-item.md) sono associati agli oggetti della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-118">Both the [**DeviceInfo**](-wia-deviceinfo.md) object and the [**Item**](-wia-item.md) object are associated with collection objects.</span></span> <span data-ttu-id="bc5fc-119">Per informazioni sull'utilizzo di oggetti Collection, vedere Using WIA Collection Objects.</span><span class="sxs-lookup"><span data-stu-id="bc5fc-119">For information about using collection objects, see Using WIA Collection Objects.</span></span>

<span data-ttu-id="bc5fc-120">Negli argomenti seguenti vengono illustrate le informazioni generali sull'utilizzo del modello di scripting WIA:</span><span class="sxs-lookup"><span data-stu-id="bc5fc-120">The following topics cover general information about using the WIA scripting model:</span></span>

-   [<span data-ttu-id="bc5fc-121">Convenzioni della sintassi</span><span class="sxs-lookup"><span data-stu-id="bc5fc-121">Syntax Conventions</span></span>](-wia-syntax-conventions.md)
-   [<span data-ttu-id="bc5fc-122">Utilizzo di oggetti Collection WIA</span><span class="sxs-lookup"><span data-stu-id="bc5fc-122">Using WIA Collection Objects</span></span>](-wia-using-wia-collection-objects.md)
-   [<span data-ttu-id="bc5fc-123">Definizioni di costanti della proprietà WIA</span><span class="sxs-lookup"><span data-stu-id="bc5fc-123">WIA Property Constant Definitions</span></span>](-wia-wia-property-constant-definitions.md)

 

 
