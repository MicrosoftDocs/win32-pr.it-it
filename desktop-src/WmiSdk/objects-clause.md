---
description: La clausola OBJECTs della macro del tipo di notifica enumera il set di oggetti associati all'oggetto notifica.
ms.assetid: 0cb4776f-aae2-452d-9472-caf6d28fb870
ms.tgt_platform: multiple
title: Clausola OBJECTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e25848e0fc98ca79ef96e25423ba7872296e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225859"
---
# <a name="objects-clause"></a>Clausola OBJECTs

La clausola OBJECTs della macro del [tipo di notifica](notification-type-macro.md) enumera il set di oggetti associati all'oggetto notifica.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Quando si esegue il mapping a classi CIM, si applicano le regole seguenti:

-   Ogni membro della clausola OBJECTs viene mappato a una proprietà della definizione di classe CIM. Il descrittore di oggetto del membro esegue il mapping Verbatim al nome della proprietà CIM. Ad esempio, **ifindex** viene convertito in **ifindex**.
-   Ogni proprietà CIM generata dal processo di mapping contiene il qualificatore **VarBindIndex** .

    **VarBindIndex** è un qualificatore obbligatorio **UInt32** che descrive la posizione dell'oggetto come appare nella clausola Objects del [tipo trap](trap-type-macro.md) o della macro del [tipo di notifica](notification-type-macro.md) . Il valore integer specifica anche la posizione della proprietà così come viene visualizzato nell'elenco di associazioni di variabili di SNMPv1 o SNMPv2C TRAP PDU (protocollo Data Unit), rispettivamente. Poiché le prime due associazioni di variabili sono sempre TimeStamp e identificazione, qualsiasi variabile aggiuntiva è numerata dopo il valore 2.

    Quando la classe di evento CIM viene generata da una macro di [tipo trap](trap-type-macro.md) SNMPv1, il qualificatore **VarBindIndex** ha un valore iniziale pari a 1 per la prima variabile nell'elenco delle associazioni di variabili.

    Quando la classe di evento CIM viene generata da una macro del [tipo di notifica](notification-type-macro.md) SNMPv2c, il qualificatore **VarBindIndex** ha un valore iniziale di 3 per la prima variabile nell'elenco delle associazioni di variabili.

Quando si esegue il mapping di una classe CIM incapsulata, ogni membro della clausola OBJECTs viene mappato a una proprietà CIM che riflette il nome, il tipo e il valore dell'oggetto MIB corrispondente. Le procedure di mapping utilizzate sono specificate negli argomenti seguenti:

-   [Clausola SYNTAX](syntax-clause.md)
-   [Macro convenzione testuale](textual-convention-macro.md)
-   [Clausole ACCESS e MAX-ACCESS](access-and-max-access-clauses.md)

Quando si utilizza una classe CIM riferente, ogni membro della clausola OBJECTs viene mappato come segue:

-   Ogni membro della clausola OBJECTs esegue il mapping a una singola proprietà della classe CIM. La proprietà è fortemente tipizzata come oggetto incorporato.
-   La classe dell'oggetto incorporato viene generata tramite la procedura standard di mapping degli oggetti. Per ulteriori informazioni, vedere [macro di tipo di oggetto](object-type-macro.md). Ad esempio, **iftable** esegue il mapping a una classe incorporata denominata **SNMP \_ RFC1213 \_ MIB \_ iftable**.
-   Vengono create istanze di oggetti incorporati di un oggetto della classe referente per i valori associati alle associazioni variabili di una PDU TRAP. Ogni oggetto incorporato contiene valori per ogni proprietà con chiave dell'oggetto e il valore della proprietà nell'associazione di variabili di cui è in corso il mapping.

 

 



