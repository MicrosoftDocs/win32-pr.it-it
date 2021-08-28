---
title: Configurazione dei limiti TTL
description: Un client può richiedere un valore TTL per una voce compresa tra 1 e 31557600 (ovvero da 1 secondo a 1 anno).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configurazione di TTL Limits AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2786258d060ef4261dcd9fbfad359c71f2dbaeb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881607"
---
# <a name="configuration-of-ttl-limits"></a>Configurazione dei limiti TTL

Un client può richiedere un valore TTL per una voce compresa tra 1 e 31557600 (ovvero da 1 secondo a 1 anno). Questo intervallo di valori di attributo verrà applicato dai valori degli attributi **rangeLower** e **rangeUpper** nella definizione **attributeSchema** per l'attributo **entryTTL.** In base a RFC 2589, non è necessario che i server di directory accettino questo valore e potrebbero restituire un valore TTL diverso al client. I client devono essere in grado di usare questo valore determinato dal server come periodo di aggiornamento client (CRP) che regola la frequenza con cui il client dovrà eseguire l'operazione di aggiornamento sulla voce dinamica.

Active Directory Domain Services agli amministratori la possibilità di configurare i valori TTL predefiniti e minimi per una foresta. Il valore TTL predefinito è quello che verrà assegnato a una voce dinamica appena creata se non viene specificato in modo esplicito un TTL. Il valore TTL minimo eseguirà l'override di qualsiasi valore TTL specificato dal client inferiore al valore minimo configurato. Non è necessario specificare alcun valore TTL massimo configurabile perché verrà imposto un valore massimo dal valore dell'attributo **rangeUpper** **nell'oggetto attributeSchema.** Consentire agli amministratori di configurare questi valori consentirà loro di impostare valori TTL che implichino un traffico di aggiornamento basso o, al contrario, forniranno una directory altamente aggiornata.

I valori predefiniti per i due parametri TTL configurabili saranno i seguenti:

-   Valore TTL predefinito = 86400 secondi (1 giorno)
-   Valore TTL minimo = 900 secondi (15 minuti)

I parametri TTL configurabili verranno archiviati come voci AVA (asserzione del valore dell'attributo) nel formato " value-name value " nell'attributo &lt; &gt; = &lt; &gt; **ms-DS-Other-Impostazioni** dell'oggetto NTDS-Service specificato dal DN seguente nella partizione di configurazione:


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



La sintassi esatta dell'AVA, per i due parametri TTL configurabili, è la seguente, dove NNNN è espresso in secondi:


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



Questi valori possono essere impostati da un amministratore tramite l'utilità della riga di comando ntdsutil.

 

 




