---
description: Viene illustrato come richiamare un comando DDE utilizzando un verbo della shell.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Come associare i verbi ai comandi DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979607"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a><span data-ttu-id="c3fbf-103">Come associare i verbi ai comandi DDE</span><span class="sxs-lookup"><span data-stu-id="c3fbf-103">How to Associate Verbs with DDE Commands</span></span>

<span data-ttu-id="c3fbf-104">La chiamata di un verbo avvia normalmente l'applicazione specificata dalla sottochiave del comando del verbo.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-104">Invoking a verb ordinarily launches the application that is specified by the verb's command subkey.</span></span> <span data-ttu-id="c3fbf-105">Tuttavia, se l'applicazione supporta Dynamic Data Exchange (DDE), è possibile fare in modo che la shell avvii una conversazione DDE.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-105">However, if your application supports Dynamic Data Exchange (DDE), you can instead have the Shell initiate a DDE conversation.</span></span>

<span data-ttu-id="c3fbf-106">Per specificare che la chiamata di un verbo deve avviare una conversazione DDE, attenersi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-106">To specify that invoking a verb should initiate a DDE conversation, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="c3fbf-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c3fbf-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="c3fbf-108">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="c3fbf-108">Step 1:</span></span>

<span data-ttu-id="c3fbf-109">Aggiungere una sottochiave **DDEExec** alla chiave del verbo.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-109">Add a **ddeexec** subkey to the verb's key.</span></span>

### <a name="step-2"></a><span data-ttu-id="c3fbf-110">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="c3fbf-110">Step 2:</span></span>

<span data-ttu-id="c3fbf-111">Impostare il valore predefinito di **DDEExec** sulla stringa di comando DDE.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-111">Set the default value of **ddeexec** to the DDE command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3fbf-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3fbf-112">Remarks</span></span>

<span data-ttu-id="c3fbf-113">La chiave **DDEExec** dispone di tre sottochiavi facoltative che forniscono un certo controllo sul processo DDE:</span><span class="sxs-lookup"><span data-stu-id="c3fbf-113">The **ddeexec** key has three optional subkeys that provide some control over the DDE process:</span></span>

-   <span data-ttu-id="c3fbf-114">**applicazione**.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-114">**application**.</span></span> <span data-ttu-id="c3fbf-115">Impostare il valore predefinito della sottochiave sul nome dell'applicazione da utilizzare per stabilire la conversazione DDE.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-115">Set the default value of this subkey to the application name to be used to establish the DDE conversation.</span></span> <span data-ttu-id="c3fbf-116">Se non è presente alcuna sottochiave dell' **applicazione** , come nome dell'applicazione viene usato il valore predefinito della sottochiave del **comando** del verbo.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-116">If there is no **application** subkey, the default value of the verb's **command** subkey is used as the application name.</span></span>
-   <span data-ttu-id="c3fbf-117">**argomento**.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-117">**topic**.</span></span> <span data-ttu-id="c3fbf-118">Impostare il valore predefinito della sottochiave sul nome dell'argomento della conversazione DDE.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-118">Set the default value of this subkey to the topic name of the DDE conversation.</span></span> <span data-ttu-id="c3fbf-119">Se non è presente alcuna sottochiave dell' **argomento** , viene usato System come nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-119">If there is no **topic** subkey, System is used as the topic name.</span></span>
-   <span data-ttu-id="c3fbf-120">**ifexec**.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-120">**ifexec**.</span></span> <span data-ttu-id="c3fbf-121">Impostare il valore predefinito della sottochiave sul comando DDE da utilizzare se non è possibile avviare la conversazione DDE.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-121">Set the default value of this subkey to the DDE command to be used if DDE conversation cannot be initiated.</span></span> <span data-ttu-id="c3fbf-122">Quando l'avvio ha esito negativo, viene avviata l'applicazione specificata dal valore predefinito della sottochiave del **comando** del verbo.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-122">When initiation fails, the application that is specified by the default value of the verb's **command** subkey is launched.</span></span> <span data-ttu-id="c3fbf-123">Se esiste una chiave **ifexec** , il relativo valore predefinito verrà usato come comando DDE.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-123">If an **ifexec** key exists, its default value will then be used as the DDE command.</span></span> <span data-ttu-id="c3fbf-124">Se non è presente alcuna sottochiave **ifexec** , il valore predefinito della chiave **DDEExec** verrà usato nuovamente come comando DDE.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-124">If there is no **ifexec** subkey, the default value of the **ddeexec** key will be used again as the DDE command.</span></span>

<span data-ttu-id="c3fbf-125">Nell'esempio seguente viene specificato che per richiamare il verbo aperto per il programma. 1 viene avviata una conversazione DDE con un comando DDE aperto ("%1") e un nome applicazione di programma.</span><span class="sxs-lookup"><span data-stu-id="c3fbf-125">The following example specifies that invoking the open verb for MyProgram.1 initiates a DDE conversation with a DDE command of Open("%1") and an application name of MyProgram.</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



