---
description: Un consumer logico è un'istanza di una classe di consumer di eventi permanenti.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Creazione di un consumer logico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317570"
---
# <a name="creating-a-logical-consumer"></a><span data-ttu-id="7f36d-103">Creazione di un consumer logico</span><span class="sxs-lookup"><span data-stu-id="7f36d-103">Creating a Logical Consumer</span></span>

<span data-ttu-id="7f36d-104">Un consumer logico è un'istanza di una classe di consumer di eventi permanenti.</span><span class="sxs-lookup"><span data-stu-id="7f36d-104">A logical consumer is an instance of a permanent event consumer class.</span></span> <span data-ttu-id="7f36d-105">Lo scopo principale di un consumer logico è fornire al consumer fisico i parametri per le attività eseguite dal consumer fisico.</span><span class="sxs-lookup"><span data-stu-id="7f36d-105">The main purpose of a logical consumer is to provide the physical consumer with the parameters for the activities the physical consumer performs.</span></span> <span data-ttu-id="7f36d-106">Per altre informazioni, vedere [creazione di una nuova classe di consumer di eventi permanenti](creating-a-new-permanent-event-consumer-class.md).</span><span class="sxs-lookup"><span data-stu-id="7f36d-106">For more information, see [Creating a New Permanent Event Consumer Class](creating-a-new-permanent-event-consumer-class.md).</span></span> <span data-ttu-id="7f36d-107">Il consumer permanente deve avere lo stesso [**CreatorSID**](--eventconsumer.md) nelle istanze consumer, Filter e binding.</span><span class="sxs-lookup"><span data-stu-id="7f36d-107">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="7f36d-108">Per altre informazioni, vedere [ricezione di eventi](receiving-events-securely.md)in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="7f36d-108">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span> <span data-ttu-id="7f36d-109">Per un esempio dell'uso di un consumer logico, vedere [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md), che mostra l'uso della classe consumer standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per configurare un consumer permanente.</span><span class="sxs-lookup"><span data-stu-id="7f36d-109">For an example of using a logical consumer, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md), which shows the use of the standard consumer class [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to configure a permanent consumer.</span></span>

<span data-ttu-id="7f36d-110">Nella procedura riportata di seguito viene descritto come creare un consumer logico.</span><span class="sxs-lookup"><span data-stu-id="7f36d-110">The following procedure describes how to create a logical consumer.</span></span>

<span data-ttu-id="7f36d-111">**Per creare un consumer logico**</span><span class="sxs-lookup"><span data-stu-id="7f36d-111">**To create a logical consumer**</span></span>

1.  <span data-ttu-id="7f36d-112">Creare un'istanza della classe consumer permanente.</span><span class="sxs-lookup"><span data-stu-id="7f36d-112">Create an instance of your permanent consumer class.</span></span>
2.  <span data-ttu-id="7f36d-113">Inserire le proprietà dell'istanza con i parametri dell'azione che il consumer fisico deve eseguire.</span><span class="sxs-lookup"><span data-stu-id="7f36d-113">Fill the properties of the instance with the parameters of the action you want the physical consumer to perform.</span></span>

<span data-ttu-id="7f36d-114">Nell'esempio di codice MOF riportato di seguito viene descritto un consumer logico che contiene uno script.</span><span class="sxs-lookup"><span data-stu-id="7f36d-114">The following MOF code example describes a logical consumer that contains a script.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="7f36d-115">Dopo aver creato il consumer logico, è necessario collegare ogni filtro a un filtro eventi per assegnare l'azione a un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="7f36d-115">After you create the logical consumer, you must then link each filter to an event filter to assign the action to a particular event.</span></span> <span data-ttu-id="7f36d-116">Per ulteriori informazioni, vedere [creazione di un filtro eventi](creating-an-event-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7f36d-116">For more information, see [Creating an Event Filter](creating-an-event-filter.md).</span></span>

 

 



