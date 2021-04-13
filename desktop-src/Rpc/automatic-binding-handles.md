---
title: Handle di binding automatici
description: Gli handle di binding automatici sono utili quando l'applicazione non richiede un server specifico e quando non è necessario mantenere le informazioni sullo stato tra il client e il server.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338782"
---
# <a name="automatic-binding-handles"></a>Handle di binding automatici

Gli handle di binding automatici sono utili quando l'applicazione non richiede un server specifico e quando non è necessario mantenere le informazioni sullo stato tra il client e il server. Quando si usa un handle di binding automatico, non è necessario scrivere codice dell'applicazione client per gestire l'associazione e gli handle. è sufficiente specificare l'uso dell'handle di binding automatico nel file di configurazione dell'applicazione (ACF). Lo stub definisce quindi l'handle e gestisce l'associazione.

Ad esempio, un'operazione timestamp può essere implementata usando un handle automatico. Non fa alcuna differenza per l'applicazione client che il server fornisce al timestamp perché può accettare l'ora da qualsiasi server disponibile.

> [!Note]  
> Gli handle automatici non sono supportati per la piattaforma Macintosh.

 

È possibile specificare l'uso di handle automatici includendo l' \[ attributo [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] in ACF. Nell'esempio relativo al timestamp viene usato il seguente ACF:

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

Quando ACF non include altri attributi di handle e quando le procedure remote non usano handle espliciti, il compilatore MIDL usa gli handle automatici per impostazione predefinita. USA anche handle automatici come impostazione predefinita quando l'ACF non è presente.

Le procedure remote vengono specificate nel file IDL. L'handle automatico non deve essere visualizzato come argomento della procedura remota. Ad esempio:

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

Il vantaggio dell'handle automatico è che lo sviluppatore non deve scrivere codice per gestire l'handle; gli stub gestiscono automaticamente l'associazione. Questo è significativamente diverso dall' [esempio Hello, World](tutorial.md), in cui il client gestisce l'handle primitivo implicito definito in ACF e deve chiamare diverse funzioni di run-time per stabilire l'handle di associazione.

 

 