---
description: Si consiglia di compilare tutte le sottoscrizioni permanenti nello \\ \\ spazio dei nomi della sottoscrizione radice.
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: Implementazione delle sottoscrizioni di eventi permanenti tra spazi dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52771e40d4dfb036354c3b37b562b32edd3034ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315220"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a><span data-ttu-id="f276d-103">Implementazione delle sottoscrizioni di eventi permanenti tra spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="f276d-103">Implementing Cross-Namespace Permanent Event Subscriptions</span></span>

<span data-ttu-id="f276d-104">Si consiglia di compilare tutte le sottoscrizioni permanenti nello \\ \\ spazio dei nomi della sottoscrizione radice.</span><span class="sxs-lookup"><span data-stu-id="f276d-104">It is recommended that all permanent subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="f276d-105">In questo modo si impedisce la necessità di compilare il consumer permanente in ogni spazio dei nomi utilizzato, il che significa che è presente un solo spazio dei nomi per la ricerca di sottoscrizioni permanenti.</span><span class="sxs-lookup"><span data-stu-id="f276d-105">This prevents the need to compile the permanent consumer into each namespace being used, which means that there is only one namespace to look for permanent subscriptions.</span></span> <span data-ttu-id="f276d-106">Usare la proprietà **EventNamespace** di [**\_ \_ EventFilter**](--eventfilter.md) per implementare una sottoscrizione tra più spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f276d-106">Use the **EventNamespace** property of [**\_\_EventFilter**](--eventfilter.md) to implement a cross-namespace subscription.</span></span>

<span data-ttu-id="f276d-107">Quando si usa [**CommandLineEventConsumer**](commandlineeventconsumer.md), è importante proteggere l'eseguibile che si sta avviando.</span><span class="sxs-lookup"><span data-stu-id="f276d-107">When using the [**CommandLineEventConsumer**](commandlineeventconsumer.md), it is important to secure the executable you are launching.</span></span> <span data-ttu-id="f276d-108">Se il file eseguibile non si trova in un percorso sicuro o protetto con un elenco di controllo di accesso (ACL) sicuro, chiunque può sostituire il file eseguibile con uno dei propri.</span><span class="sxs-lookup"><span data-stu-id="f276d-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), anyone can replace your executable with one of their own.</span></span> <span data-ttu-id="f276d-109">Per ulteriori informazioni sugli ACL, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="f276d-109">For more information about ACLs, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="f276d-110">Nell'esempio di codice seguente Managed Object Format (MOF) viene illustrata una sottoscrizione tra più spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f276d-110">The following Managed Object Format (MOF) code example shows a cross-namespace subscription.</span></span>

``` syntax
#pragma namespace("\\root\\subscription")

instance of __EventFilter as $FLT
{
  Name = "Filter";
  Query = "SELECT * FROM __InstanceModificationEvent "
          "WHERE TargetInstance ISA \"Win32_LocalTime\" "
          "AND TargetInstance.Hour = 8 "
          "AND TargetInstance.Minute = 0 "
          "AND TargetInstance.Second = 0 "
          "AND TargetInstance.DayOfWeek = 6";
  QueryLanguage = "WQL";
  EventNamespace = "root\\cimv2";
};

instance of CommandLineEventConsumer as $CONS
{
  ExecutablePath = "cmd.exe";
  ShowWindowCommand = 7;
  RunInteractively = true;
};

instance of __FilterToConsumerBinding
{
  Consumer = $CONS;
  Filter = $FLT;
};
```

 

 
