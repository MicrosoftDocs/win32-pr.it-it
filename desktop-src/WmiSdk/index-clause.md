---
description: Specifica una chiave per selezionare una riga univoca in una raccolta scalare o di tabella.
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: Clausola INDEX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca4478164839412238f59d9771aa9c96417c4055390cb4599edbb40b0e6b4a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318743"
---
# <a name="index-clause"></a>Clausola INDEX

La clausola INDEX specifica una chiave per selezionare una riga univoca in una raccolta scalare o di tabella. Il provider SNMP esegue il mapping a un tipo diverso di classe CIM a seconda del tipo di tabella utilizzata dal dispositivo SNMP. Poiché una chiave può essere più di un tipo di oggetto, il provider usa regole di mapping diverse a seconda del tipo di oggetto all'interno della chiave. Per altre informazioni, vedere [Tipi di dati della clausola INDEX](#index-clause-data-types).

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

Una raccolta scalare esegue il mapping a una classe singleton CIM, ad esempio una classe che può avere una sola istanza. Poiché non è necessario identificare in modo univoco un'istanza da un'altra, una classe singleton non designa una o più proprietà come chiave. Classi generate da raccolte scalari:

-   Non contengono **qualificatori di** proprietà Key.
-   Contenere il qualificatore di classe CIM standard **Singleton**, che è di **tipo Bool**.

Una raccolta di tabelle esegue il mapping a una classe CIM che può avere più di un'istanza. Di conseguenza, la definizione della classe CIM deve contenere almeno una proprietà che definisce la chiave dell'oggetto. una proprietà che identifica in modo univoco un'istanza della classe . La clausola INDEX della macro [OBJECT-TYPE](object-type-macro.md) di una raccolta di tabelle specifica il set di proprietà chiave della raccolta. Si applicano le regole di mapping seguenti:

-   Il qualificatore CIM **Key,** di **tipo Bool,** definisce una proprietà della chiave.
-   L'ordinamento delle informazioni INDEX all'interno della raccolta di tabelle definisce l'ordinamento delle chiavi all'interno della definizione della classe CIM.

    L'ordine delle chiavi **del qualificatore \_** CIM definisce l'ordinamento delle chiavi. Questo qualificatore è un valore intero senza segno a 32 bit che, ai fini della sintassi del qualificatore MOF, deve essere convertito in un intero con segno a 32 bit usando l'operazione a complemento a due.

Attualmente, il mapping della clausola SNMPv2C INDEX non gestisce l'uso del **qualificatore IMPLIED.** In questo caso non viene generata una definizione di classe CIM.

## <a name="index-clause-data-types"></a>Tipi di dati della clausola INDEX

Data la flessibilità della clausola INDEX all'interno della macro [OBJECT-TYPE,](object-type-macro.md) la specifica delle proprietà con chiave non è semplice. È invece necessario considerare le possibilità che la clausola INDEX possa contenere uno o più dei tipi di dati seguenti:

-   Valore **indexobject accessibile internamente**

    Il **valore indexobject** è un valore denominato che fa riferimento a una definizione di oggetto MIB visualizzata nella riga concettuale della stessa tabella che contiene la clausola INDEX. La definizione dell'oggetto MIB a cui si fa riferimento nella clausola INDEX esegue il mapping a una proprietà chiave della definizione della classe CIM.

-   Valore **indexobject accessibile esternamente**

    In questo caso, **indexobject** è un valore denominato che fa riferimento a una definizione di oggetto MIB visualizzata nella riga concettuale di una tabella diversa.

-   Valore **indextype accessibile**

    Il **valore indextype** è un tipo denominato che fa riferimento a uno dei tipi di dati **seguenti: INTEGER,** **OCTET STRING,** **OBJECT IDENTIFIER,** **NetworkAddress** o **IpAddress.** Se la clausola INDEX contiene un riferimento di tipo MIB, si applicano le regole di mapping seguenti:

    -   L'oggetto MIB a cui si fa riferimento esegue il mapping a una proprietà chiave della definizione della classe CIM. La sintassi del tipo è basata sul **valore indextype** specificato, che esegue il mapping ai qualificatori di proprietà CIM usando le procedure standard di mapping della [clausola SYNTAX.](syntax-clause.md)
    -   Il processo di mapping genera un nome di proprietà univoco concatenando il descrittore dell'oggetto tabella MIB, un carattere di sottolineatura ( ) e l'ordine di classificazione del valore indextype della clausola \_ INDEX.  Ad esempio, il nome della proprietà per il terzo **indextype** componente della tabella MIB **enterpriseIfTable** è **enterpriseIfTable \_ 3**.
    -   La proprietà CIM viene annotata con il **qualificatore Virtual \_ Key.** Questo qualificatore specifica che il provider SNMP deve calcolare il valore della proprietà in base al superset di informazioni sull'istanza associato a tutte le definizioni di oggetto MIB accessibili nella definizione di classe.
    -   La definizione della classe CIM deve contenere almeno **\_** una proprietà a cui non è associato un qualificatore di chiave virtuale. La mancata specifica di questa proprietà invalida la definizione della classe.

-   Sottotipo a lunghezza fissa

    Quando la clausola INDEX di una raccolta di tabelle SNMP contiene un tipo supportato da SNMP sottotipo come OCTET STRING a lunghezza fissa, è necessario usare il qualificatore di proprietà CIM Lunghezza fissa per specificare questo valore. **\_**

 

 



