---
description: Una raccolta SNMP esegue il mapping a una classe CIM e gli elementi di una raccolta vengono mappati alle proprietà di una classe CIM. Tutte le definizioni di classi CIM generate devono essere derivate dalla classe SnmpObjectType.
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
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309882"
---
# <a name="snmp-collections"></a>Raccolte SNMP

Una raccolta SNMP esegue il mapping a una classe CIM e gli elementi di una raccolta vengono mappati alle proprietà di una classe CIM. Tutte le definizioni di classi CIM generate devono essere derivate dalla classe **SnmpObjectType** .

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Le definizioni di classe seguenti controllano tutte le definizioni delle classi generate:

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

Quando si esegue il mapping di raccolte SNMP a classi CIM, si applicano le regole seguenti. Se non diversamente specificato, queste regole si applicano alle raccolte scalari e di tabella:

-   Il processo di mapping genera i nomi delle classi CIM concatenando "SNMP \_ ", il nome dell'identità del modulo MIB, " \_ " e il descrittore di oggetto della raccolta.

    Ad esempio: il **sistema** si traduce in **SNMP \_ RFC1213 \_ MIB \_ System**, mentre **iftable** si traduce in **SNMP \_ RFC1213 \_ MIB \_ iftable**.

-   In tutti i casi, i trattini (-) negli identificatori MIB SNMP vengono mappati ai caratteri di sottolineatura ( \_ ) nei nomi di classe CIM.
-   I conflitti di denominazione possono verificarsi a causa di un nome CIM senza distinzione tra maiuscole e minuscole. Se si verifica un conflitto di denominazione, il provider sceglie una delle definizioni di gruppo in conflitto e ignora le definizioni rimanenti.
-   Il nome di identità del modulo MIB che contiene la raccolta è mappato al nome del **modulo \_** qualificatore della classe CIM.
-   L'identificatore di oggetto della raccolta fabbricata viene mappato al gruppo di qualificatori della classe CIM **\_ ObjectID**.
-   L'elenco di importazioni del modulo MIB (ottenuto dalla definizione della macro **Module-Identity** ) viene mappato alle **\_ importazioni del modulo** qualificatore di classe CIM. Questo qualificatore contiene un elenco delimitato da virgole di nomi di moduli.

 

 



