---
description: Le query dello schema sono istruzioni WQL che richiedono definizioni di classe e informazioni sulle associazioni dello schema.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Recupero di definizioni di classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131011"
---
# <a name="retrieving-class-definitions"></a>Recupero di definizioni di classe

Le query dello schema sono istruzioni WQL che richiedono definizioni di classe e informazioni sulle [associazioni dello schema](schema-associations.md). I provider di classi utilizzano query dello schema nelle istanze della classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) per specificare le classi supportate durante la registrazione con WMI. Le query dello schema vengono inserite nelle proprietà **ResultSetQueries**, **ReferencedSetQueries** e **UnsupportedQueries** dell'istanza di **\_ \_ ClassProviderRegistration** .

Le query di schema sono simili alle query di dati perché supportano le istruzioni WQL seguenti:

-   [SELECT](select-statement-for-schema-queries.md)
-   [ASSOCIATORI DI](schema-associations.md)
-   [RIFERIMENTI DI](schema-associations.md)
-   [ISA](isa-operator-for-schema-queries.md)

Una query di schema è simile a un [riferimento della query di](references-of-statement.md) dati che specifica la parola chiave **ClassDefsOnly** . in altre parole, restituisce un set di risultati di oggetti di definizione di classe anziché le istanze effettive delle classi di associazione. Tuttavia, i riferimenti di restituiscono le definizioni della classe solo se sono presenti istanze. Una query di schema restituisce le definizioni delle classi se le istanze sono presenti o meno.

 

 



