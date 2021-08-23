---
description: È consigliabile compilare tutte le sottoscrizioni permanenti nello spazio dei \\ nomi della \\ sottoscrizione radice.
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: Implementazione di sottoscrizioni di eventi permanenti tra spazi dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b175f89a4a686aa47818daf3479d521306f6190fb245222c4c21c17ca6470dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757951"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a>Implementazione di sottoscrizioni di eventi permanenti tra spazi dei nomi

È consigliabile compilare tutte le sottoscrizioni permanenti nello spazio dei \\ nomi della \\ sottoscrizione radice. Ciò impedisce la necessità di compilare il consumer permanente in ogni spazio dei nomi usato, il che significa che è presente un solo spazio dei nomi per cercare le sottoscrizioni permanenti. Usare la **proprietà EventNamespace** di [**\_ \_ EventFilter**](--eventfilter.md) per implementare una sottoscrizione tra spazi dei nomi.

Quando si usa [**CommandLineEventConsumer,**](commandlineeventconsumer.md)è importante proteggere l'eseguibile che si sta avviando. Se l'eseguibile non si trova in una posizione sicura o è protetto con un elenco di controllo di accesso sicuro ( ACL), chiunque può sostituire il file eseguibile con uno dei propri. Per altre informazioni sugli ACL, vedere Creazione di un descrittore [di sicurezza per un nuovo oggetto in C++.](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)

L'esempio Managed Object Format codice mof (MoF) seguente illustra una sottoscrizione tra spazi dei nomi.

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

 

 
