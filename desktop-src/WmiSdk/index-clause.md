---
description: Specifica una chiave per la selezione di una riga univoca in una raccolta scalare o tabella.
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: Clausola INDEX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 915cbe1c4bf1da5ccd7fbab881770722b70bc53c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131922"
---
# <a name="index-clause"></a>Clausola INDEX

La clausola INDEX specifica una chiave per selezionare una riga univoca in una raccolta scalare o tabella. Il provider SNMP esegue il mapping a un tipo diverso di classe CIM a seconda del tipo di tabella utilizzato dal dispositivo SNMP. Poiché una chiave può essere costituita da più di un tipo di oggetto, il provider Usa regole di mapping diverse a seconda del tipo di oggetto all'interno della chiave. Per ulteriori informazioni, vedere [tipi di dati della clausola index](#index-clause-data-types).

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Una raccolta scalare esegue il mapping a una classe singleton CIM, ovvero una classe che può avere una sola istanza. Poiché non è necessario identificare in modo univoco un'istanza da un'altra, una classe singleton non designa una o più proprietà come chiave. Classi generate da raccolte scalari:

-   Non contengono qualificatori di proprietà **chiave** .
-   Contengono il **singleton** del qualificatore della classe CIM standard, che è di tipo **bool**.

Una raccolta di tabelle è mappata a una classe CIM che può avere più di un'istanza. Di conseguenza, la definizione della classe CIM deve contenere almeno una proprietà che definisce la chiave dell'oggetto. ovvero una proprietà che identifica in modo univoco un'istanza della classe. La clausola INDEX della macro di [tipo oggetto](object-type-macro.md) di una raccolta di tabelle specifica il set di proprietà chiave della raccolta. Si applicano le seguenti regole di mapping:

-   La **chiave** di qualificatore CIM, Type **bool**, definisce una proprietà chiave.
-   L'ordinamento delle informazioni sull'indice all'interno della raccolta di tabelle definisce l'ordinamento delle chiavi all'interno della definizione della classe CIM.

    L' **\_ ordine** delle chiavi qualificatore CIM definisce l'ordinamento delle chiavi. Questo qualificatore è un valore intero senza segno a 32 bit che, ai fini della sintassi del qualificatore MOF, deve essere convertito in un valore integer a 32 bit con segno usando l'operazione di complemento a due.

Attualmente, il mapping della clausola SNMPv2C INDEX non gestisce l'utilizzo del qualificatore **implicito** . In questo caso non viene generata una definizione di classe CIM.

## <a name="index-clause-data-types"></a>Tipi di dati della clausola INDEX

A causa della flessibilità della clausola INDEX all'interno della macro del [tipo di oggetto](object-type-macro.md) , la specifica delle proprietà con chiave non è semplice. È invece opportuno prendere in considerazione la possibilità che la clausola INDEX includa uno o più dei tipi di dati seguenti:

-   Valore **indexobject** accessibile internamente

    Il valore **indexobject** è un valore denominato che fa riferimento a una definizione di oggetto MIB visualizzata nella riga concettuale della stessa tabella che contiene la clausola index. La definizione dell'oggetto MIB a cui viene fatto riferimento nella clausola INDEX è mappata a una proprietà chiave della definizione di classe CIM.

-   Valore **indexobject** accessibile esternamente

    In questo caso, **indexobject** è un valore denominato che fa riferimento a una definizione di oggetto MIB visualizzata nella riga concettuale di una tabella diversa.

-   Valore **IndexType** accessibile

    Il **valore IndexType** è un tipo denominato che fa riferimento a uno dei tipi di dati seguenti: **Integer**, **stringa ottetto**, **identificatore oggetto**, **networkAddress** o **IPAddress**. Se la clausola INDEX contiene un riferimento di tipo MIB, verranno applicate le regole di mapping seguenti:

    -   L'oggetto MIB a cui si fa riferimento viene mappato a una proprietà chiave della definizione di classe CIM. La relativa sintassi del tipo è basata sul valore **IndexType** specificato, che esegue il mapping ai qualificatori di proprietà CIM usando le procedure di mapping della [clausola della sintassi](syntax-clause.md) standard.
    -   Il processo di mapping genera un nome di proprietà univoco concatenando il descrittore di oggetti della tabella MIB, un carattere di sottolineatura ( \_ ) e l'ordine di pertinenza del valore **IndexType** della clausola index. Ad esempio, il nome della proprietà per il terzo componente **IndexType** della tabella MIB **enterpriseIfTable** è **enterpriseIfTable \_ 3**.
    -   La proprietà CIM viene annotata con il qualificatore della **\_ chiave virtuale** . Questo qualificatore specifica che il provider SNMP deve calcolare il valore della proprietà in base al superset delle informazioni sull'istanza associate a tutte le definizioni di oggetti MIB accessibili nella definizione della classe.
    -   La definizione della classe CIM deve contenere almeno una proprietà a cui non è associato un qualificatore di **\_ chiave virtuale** . non è possibile specificare questa proprietà per invalidare la definizione della classe.

-   Sottotipo a lunghezza fissa

    Quando la clausola INDEX di una raccolta di tabelle SNMP contiene un tipo supportato da SNMP, sottoposto a una stringa di ottetto a lunghezza fissa, è necessario utilizzare la **\_ lunghezza fissa** del qualificatore di proprietà CIM per specificare questo valore.

 

 



