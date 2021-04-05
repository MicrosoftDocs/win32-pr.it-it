---
title: Configurazione dei limiti TTL
description: Un client può richiedere un valore TTL per una voce compresa tra 1 e 31557600, ovvero da 1 secondo a 1 anno.
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configurazione dei limiti TTL AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707195"
---
# <a name="configuration-of-ttl-limits"></a>Configurazione dei limiti TTL

Un client può richiedere un valore TTL per una voce compresa tra 1 e 31557600, ovvero da 1 secondo a 1 anno. Questo intervallo di valori di attributo verrà applicato dai valori degli attributi **RangeLower** e **rangeUpper** nella definizione **attributeSchema** per l'attributo **entryTTL** . In base allo standard RFC 2589, non è necessario che i server di directory accettino questo valore e potrebbe restituire un valore TTL diverso al client. I client devono essere in grado di utilizzare questo valore dettato dal server come periodo di aggiornamento del client (CRP), che determina la frequenza con cui il client dovrà eseguire l'operazione di aggiornamento sulla voce dinamica.

Active Directory Domain Services offrire agli amministratori la possibilità di configurare i valori TTL predefiniti e minimi per una foresta. Il valore TTL predefinito è quello che verrà assegnato a una voce dinamica appena creata se non viene specificato in modo esplicito una durata (TTL). Il valore TTL minimo eseguirà l'override di qualsiasi valore TTL specificato dal client inferiore al minimo configurato. Non è necessario fornire alcun valore TTL massimo configurabile perché un valore massimo verrà imposto dal valore dell'attributo **rangeUpper** nell'oggetto **attributeSchema** . Consentendo agli amministratori di configurare questi valori, è possibile impostare i valori TTL che imporrà un traffico di aggiornamento basso o, all'altra estrema, fornire una directory altamente aggiornata.

I valori predefiniti per i due parametri TTL configurabili saranno i seguenti:

-   Valore TTL predefinito = 86400 secondi (1 giorno)
-   Valore TTL minimo = 900 secondi (15 minuti)

I parametri TTL configurabili verranno archiviati come voci AVA (Assertion value Assertion) nel formato "<nome-valore>=<value>"nell'attributo **ms-DS-Other-Settings** dell'oggetto NTDS-Service fornito dal DN seguente nella partizione di configurazione:


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



La sintassi AVA esatta, per i due parametri TTL configurabili, è la seguente, in cui NNNN è espresso in secondi:


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



Questi valori possono essere impostati da un amministratore tramite l'utilità da riga di comando Ntdsutil.

 

 




