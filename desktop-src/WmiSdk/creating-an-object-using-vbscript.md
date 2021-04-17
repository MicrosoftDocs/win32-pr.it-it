---
description: È possibile creare un oggetto per WMI in Visual Basic Scripting Edition (VBScript) connettendosi a WMI e quindi chiamando CreateObject. Nella tabella seguente sono elencati i metodi dell'API di scripting per WMI che supportano la creazione di oggetti.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Creazione di un oggetto tramite VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485356"
---
# <a name="creating-an-object-using-vbscript"></a><span data-ttu-id="5d7fb-104">Creazione di un oggetto tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="5d7fb-104">Creating an Object Using VBScript</span></span>

<span data-ttu-id="5d7fb-105">È possibile creare un oggetto per WMI in Visual Basic Scripting Edition (VBScript) connettendosi a WMI e quindi chiamando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d7fb-105">You can create an object for WMI in Visual Basic Scripting Edition (VBScript) by connecting to WMI and then calling [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span> <span data-ttu-id="5d7fb-106">Nella tabella seguente sono elencati i metodi dell'API di scripting per WMI che supportano la creazione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="5d7fb-106">The following table lists the methods in the Scripting API for WMI that support object creation.</span></span>



| <span data-ttu-id="5d7fb-107">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="5d7fb-107">Interface</span></span>                                        | <span data-ttu-id="5d7fb-108">ProgID</span><span class="sxs-lookup"><span data-stu-id="5d7fb-108">ProgID</span></span>                             |
|--------------------------------------------------|------------------------------------|
| [<span data-ttu-id="5d7fb-109">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-109">**SWbemDateTime**</span></span>](swbemdatetime.md)           | <span data-ttu-id="5d7fb-110">"WbemScripting. SwbemDateTime"</span><span class="sxs-lookup"><span data-stu-id="5d7fb-110">"WbemScripting.SwbemDateTime"</span></span>      |
| [<span data-ttu-id="5d7fb-111">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-111">**SWbemLocator**</span></span>](swbemlocator.md)             | <span data-ttu-id="5d7fb-112">"WbemScripting. SWbemLocator"</span><span class="sxs-lookup"><span data-stu-id="5d7fb-112">"WbemScripting.SWbemLocator"</span></span>       |
| [<span data-ttu-id="5d7fb-113">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-113">**SWbemLastError**</span></span>](swbemlasterror.md)         | <span data-ttu-id="5d7fb-114">"WbemScripting. SWbem. LastError"</span><span class="sxs-lookup"><span data-stu-id="5d7fb-114">"WbemScripting.SWbem.LastError"</span></span>    |
| [<span data-ttu-id="5d7fb-115">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-115">**SWbemObjectPath**</span></span>](swbemobjectpath.md)       | <span data-ttu-id="5d7fb-116">"WbemScripting. SWbemObjectPath"</span><span class="sxs-lookup"><span data-stu-id="5d7fb-116">"WbemScripting.SWbemObjectPath"</span></span>    |
| [<span data-ttu-id="5d7fb-117">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-117">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md) | <span data-ttu-id="5d7fb-118">"WbemScripting. SWbemNamedValueSet"</span><span class="sxs-lookup"><span data-stu-id="5d7fb-118">"WbemScripting.SWbemNamedValueSet"</span></span> |
| [<span data-ttu-id="5d7fb-119">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-119">**SWbemRefresher**</span></span>](swbemrefresher.md)         | <span data-ttu-id="5d7fb-120">"WbemScripting. SWbemRefresher"</span><span class="sxs-lookup"><span data-stu-id="5d7fb-120">"WbemScripting.SWbemRefresher"</span></span>     |
| [<span data-ttu-id="5d7fb-121">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-121">**SWbemSink**</span></span>](swbemsink.md)                   | <span data-ttu-id="5d7fb-122">"WbemScripting. SWbemSink"</span><span class="sxs-lookup"><span data-stu-id="5d7fb-122">"WbemScripting.SWbemSink"</span></span>          |



 

<span data-ttu-id="5d7fb-123">Nella procedura riportata di seguito viene descritto come creare un oggetto WMI utilizzando VBScript.</span><span class="sxs-lookup"><span data-stu-id="5d7fb-123">The following procedure describes how to create a WMI object using VBScript.</span></span>

<span data-ttu-id="5d7fb-124">**Per creare un oggetto WMI utilizzando VBScript**</span><span class="sxs-lookup"><span data-stu-id="5d7fb-124">**To create a WMI object using VBScript**</span></span>

1.  <span data-ttu-id="5d7fb-125">Connettersi a WMI utilizzando un moniker o un oggetto [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5d7fb-125">Connect to WMI using either a moniker or an [**SWbemLocator**](swbemlocator.md) object.</span></span>

    <span data-ttu-id="5d7fb-126">Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="5d7fb-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

2.  <span data-ttu-id="5d7fb-127">Effettuare una chiamata al metodo [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="5d7fb-127">Make a call to the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method.</span></span>

    <span data-ttu-id="5d7fb-128">Nell'esempio di codice seguente viene illustrato come creare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="5d7fb-128">The following code example shows how to create an object.</span></span>

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    <span data-ttu-id="5d7fb-129">Se si usa un moniker nel passaggio 1, non è necessario chiamare di nuovo [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5d7fb-129">If you use a moniker in Step 1, you do not need to call [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) again.</span></span>

 

 
