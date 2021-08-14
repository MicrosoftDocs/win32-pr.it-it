---
description: Le query di dati sono istruzioni WQL che richiedono istanze di classi. Per eseguire una query sui dati, le applicazioni chiamano il metodo IWbemServices::ExecQuery o IWbemServices::ExecQueryAsync.
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Richiesta dei dati dell'istanza della classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332ff8b5ba0aae7d1ac33fb8faba6340bbd795401fa81a52ea9c21abc4fde2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316288"
---
# <a name="requesting-class-instance-data"></a>Richiesta dei dati dell'istanza della classe

Le query di dati sono istruzioni WQL che richiedono istanze di classi. Per eseguire una query sui dati, le applicazioni chiamano il metodo [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) o [**IWbemServices::ExecQueryAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)

Le istruzioni seguenti vengono usate per eseguire query sui dati:

-   [SELECT](select-statement-for-data-queries.md)
-   [ASSOCIATORI DI](associators-of-statement.md)
-   [RIFERIMENTI DI](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

L'istruzione SELECT WQL è l'istruzione Structured Query Language (SQL) standard per il recupero di informazioni, con alcune restrizioni ed estensioni specifiche di WQL. Anche se SQL'istruzione SELECT viene in genere usata nell'ambiente di database per recuperare colonne specifiche dalle tabelle, l'istruzione WQL SELECT viene usata in WMI per recuperare istanze di una singola classe. WQL non supporta le query in più classi.

Le istruzioni ASSOCIATORS OF e REFERENCES OF sono specifiche di WQL e non fanno parte delle istruzioni SQL. L'istruzione ASSOCIATORS OF recupera tutte le istanze di classe associate a una determinata istanza della classe di origine e REFERENCES OF recupera tutte le istanze che fanno riferimento a una determinata istanza di origine. Le associazioni sono rappresentate da istanze di una [classe di associazione](declaring-an-association-class.md).

 

 



