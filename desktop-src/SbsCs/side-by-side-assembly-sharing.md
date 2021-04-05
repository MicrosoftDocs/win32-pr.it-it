---
description: Nella figura seguente viene illustrato il modo in cui due applicazioni possono condividere un assembly utilizzando il metodo tradizionale di condivisione degli assembly.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Condivisione di assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968303"
---
# <a name="side-by-side-assembly-sharing"></a>Condivisione di assembly affiancati

Nella figura seguente viene illustrato il modo in cui due applicazioni possono condividere un assembly utilizzando il metodo tradizionale di condivisione degli assembly. Un problema con la condivisione di assembly tradizionale si verifica quando un'applicazione installa una versione di un assembly, in genere una DLL, che non è compatibile con le versioni precedenti. L'applicazione appena installata funziona, ma le applicazioni che dipendono dalla versione precedente della DLL potrebbero non funzionare più.

![rappresentazione di due applicazioni che condividono un assembly](images/sxs1.png)

L'applicazione isolata e la soluzione assembly side-by-side consentono l'esecuzione contemporanea di versioni diverse dello stesso assembly Win32 nello stesso sistema senza conflitti. Specificando la versione dell'assembly affiancata che l'applicazione deve utilizzare, gli sviluppatori possono garantire che la configurazione testata venga sempre duplicata nel computer dell'utente. La condivisione affiancata è illustrata nella figura seguente.

![implementazione della condivisione di assembly side-by-side](images/sxs2.png)

Per ulteriori informazioni, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](about-isolated-applications-and-side-by-side-assemblies.md).

 

 



