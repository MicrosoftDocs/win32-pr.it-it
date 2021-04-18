---
description: 'Le query sui dati sono istruzioni WQL che richiedono istanze di classi. Per eseguire una query di dati, le applicazioni chiamano il metodo IWbemServices:: ExecQuery o IWbemServices:: ExecQueryAsync.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Richiesta di dati dell'istanza di classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32df053ae1267f396978d98271f57f174ea6bf0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318536"
---
# <a name="requesting-class-instance-data"></a>Richiesta di dati dell'istanza di classe

Le query sui dati sono istruzioni WQL che richiedono istanze di classi. Per eseguire una query di dati, le applicazioni chiamano il metodo [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) o [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .

Per eseguire query sui dati, vengono utilizzate le istruzioni seguenti:

-   [SELECT](select-statement-for-data-queries.md)
-   [ASSOCIATORI DI](associators-of-statement.md)
-   [RIFERIMENTI DI](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

L'istruzione di selezione WQL è l'istruzione Structured Query Language standard (SQL) per il recupero di informazioni, con alcune restrizioni ed estensioni specifiche di WQL. Sebbene l'istruzione SQL SELECT venga in genere utilizzata nell'ambiente di database per recuperare colonne specifiche dalle tabelle, in WMI viene utilizzata l'istruzione di selezione WQL per recuperare le istanze di una singola classe. WQL non supporta le query su più classi.

Gli ASSOCIATOri di e i riferimenti di istruzioni sono specifici di WQL e non fanno parte di SQL standard. L'ASSOCIAZIONErs OF Statement recupera tutte le istanze di classe associate a una particolare istanza della classe di origine e i riferimenti di recupera tutte le istanze che fanno riferimento a una particolare istanza di origine. Le associazioni sono rappresentate da istanze di una [classe di associazione](declaring-an-association-class.md).

 

 



