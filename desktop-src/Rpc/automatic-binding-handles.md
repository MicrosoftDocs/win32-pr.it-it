---
title: Handle di associazione automatici
description: Gli handle di associazione automatici sono utili quando l'applicazione non richiede un server specifico e quando non è necessario mantenere le informazioni sullo stato tra il client e il server.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b619b17e44e79e623bcffa84f4938d1278a7d146d6de90547cd833e1bf091167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023441"
---
# <a name="automatic-binding-handles"></a>Handle di associazione automatici

Gli handle di associazione automatici sono utili quando l'applicazione non richiede un server specifico e quando non è necessario mantenere le informazioni sullo stato tra il client e il server. Quando si usa un handle di associazione automatico, non è necessario scrivere codice dell'applicazione client per gestire l'associazione e gli handle. È sufficiente specificare l'uso dell'handle di associazione automatico nel file di configurazione dell'applicazione (ACF). Lo stub definisce quindi l'handle e gestisce l'associazione.

Ad esempio, un'operazione di timestamp può essere implementata usando un handle automatico. Non fa alcuna differenza per l'applicazione client il server che fornisce il timestamp perché può accettare l'ora da qualsiasi server disponibile.

> [!Note]  
> Gli handle automatici non sono supportati per la piattaforma Macintosh.

 

È possibile specificare l'uso di handle automatici includendo \[ [**l'attributo \_ di handle**](/windows/desktop/Midl/auto-handle) \] automatico nel file ACF. L'esempio di timestamp usa l'ACF seguente:

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

Quando acf non include altri attributi handle e quando le procedure remote non usano handle espliciti, il compilatore MIDL usa gli handle automatici per impostazione predefinita. Usa anche gli handle automatici come impostazione predefinita quando acf non è presente.

Le procedure remote vengono specificate nel file IDL. L'handle automatico non deve essere visualizzato come argomento della procedura remota. Esempio:

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

Il vantaggio dell'handle automatico è che lo sviluppatore non deve scrivere codice per gestire l'handle. Gli stub gestiscono automaticamente l'associazione. Questo è significativamente diverso dall'esempio [Hello, World](tutorial.md), in cui il client gestisce l'handle primitivo implicito definito in ACF e deve chiamare diverse funzioni di run-time per stabilire l'handle di associazione.

 

 