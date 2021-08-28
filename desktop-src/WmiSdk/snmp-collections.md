---
description: Una raccolta SNMP esegue il mapping a una classe CIM e gli elementi di una raccolta vengono mappati alle proprietà di una classe CIM. Tutte le definizioni di classe CIM generate devono essere derivate dalla classe SnmpObjectType.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: Raccolte SNMP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df4926ab89a6bb9a936fe5bdb27f921699bbe90a528842d81de96d8049412940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315305"
---
# <a name="snmp-collections"></a>Raccolte SNMP

Una raccolta SNMP esegue il mapping a una classe CIM e gli elementi di una raccolta vengono mappati alle proprietà di una classe CIM. Tutte le definizioni di classe CIM generate devono essere derivate dalla **classe SnmpObjectType.**

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Configurazione dell'ambiente SNMP WMI.](setting-up-the-wmi-snmp-environment.md)

 

Le definizioni di classe seguenti padre di tutte le definizioni di classe generate:

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a>Commenti

Le regole seguenti si applicano quando si esegue il mapping delle raccolte SNMP alle classi CIM. Se non diversamente specificato, queste regole si applicano sia alle raccolte scalari che alle raccolte di tabelle:

-   Il processo di mapping genera nomi di classe CIM concatenando "SNMP", il nome dell'identità del modulo MIB, " " e il descrittore di oggetto \_ \_ della raccolta.

    Ad esempio: **system** converte in **SNMP \_ RFC1213 \_ MIB \_ system**, **mentre ifTable** converte in **SNMP \_ RFC1213 \_ MIB \_ ifTable**.

-   In tutti i casi, i trattini (-) negli identificatori MIB SNMP vengono mappati ai caratteri di sottolineatura ( \_ ) nei nomi di classe CIM.
-   I conflitti di denominazione possono verificarsi a causa della distinzione tra maiuscole e minuscole dei nomi CIM. Se si verifica un conflitto di denominazione, il provider sceglie una delle definizioni di gruppo in conflitto e ignora le definizioni rimanenti.
-   Nome dell'identità del modulo MIB che contiene la raccolta mappa al qualificatore di classe CIM **Nome \_ modulo**.
-   L'identificatore di oggetto della raccolta fabbricata viene mappato al qualificatore di classe CIM **Group \_ Objectid**.
-   L'elenco delle importazioni del modulo MIB (ottenuto dalla definizione della macro **MODULE-IDENTITY)** viene mappato al modulo qualificatore di classe CIM **\_ importa**. Questo qualificatore contiene un elenco delimitato da virgole di nomi di moduli.

 

 



