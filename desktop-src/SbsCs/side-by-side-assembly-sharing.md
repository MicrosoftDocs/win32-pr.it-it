---
description: Nella figura seguente viene illustrato come due applicazioni potrebbero condividere un assembly usando il metodo tradizionale di condivisione degli assembly.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Condivisione di assembly side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59dcfbb40040b51fc2e17d3707d4a76c7ea5ddadf1806e41b7a7fbd81860ae15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141816"
---
# <a name="side-by-side-assembly-sharing"></a>Condivisione di assembly side-by-side

Nella figura seguente viene illustrato come due applicazioni potrebbero condividere un assembly usando il metodo tradizionale di condivisione degli assembly. Un problema con la condivisione di assembly tradizionale si verifica quando un'applicazione installa una versione di un assembly, in genere una DLL, che non è compatibile con le versioni precedenti. L'applicazione appena installata funziona, ma le applicazioni che dipendono dalla versione precedente della DLL potrebbero non funzionare più.

![Rappresentazione di due applicazioni che condividono un assembly](images/sxs1.png)

L'applicazione isolata e la soluzione di assembly side-by-side consentono l'esecuzione di versioni diverse dello stesso assembly Win32 contemporaneamente nello stesso sistema senza conflitti. Specificando la versione dell'assembly side-by-side che l'applicazione deve usare, gli sviluppatori possono garantire che la configurazione testata verrà sempre duplicata nel computer dell'utente. La condivisione side-by-side è illustrata nella figura seguente.

![implementazione della condivisione di assembly side-by-side](images/sxs2.png)

Per altre informazioni, vedere [Informazioni sulle applicazioni isolate e sugli assembly side-by-side.](about-isolated-applications-and-side-by-side-assemblies.md)

 

 



