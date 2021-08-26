---
title: Serializzazione delle procedure
description: Quando si usa la serializzazione di routine, una routine viene etichettata con l'attributo \ encode\ o \ decode\. Anziché generare lo stub remoto consueto, il compilatore genera uno stub di serializzazione per la routine.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023b514aa5a2e5be1b937a3989c3446bcc6e61c76f885381ce257286b5c625b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018951"
---
# <a name="procedure-serialization"></a>Serializzazione delle procedure

Quando si usa la serializzazione di routine, una routine viene etichettata con \[ [**l'attributo di**](/windows/desktop/Midl/encode) \] codifica o \[ [**decodifica.**](/windows/desktop/Midl/decode) \] Anziché generare lo stub remoto consueto, il compilatore genera uno stub di serializzazione per la routine.

Proprio come una procedura remota deve usare un handle di associazione per effettuare una chiamata remota, una procedura di serializzazione deve usare un handle di serializzazione per usare i servizi di serializzazione. Se non viene specificato un handle di serializzazione, per indirizzare la chiamata viene usato un handle implicito predefinito. D'altra parte, se viene specificato l'handle di serializzazione, come argomento [**t dell'handle \_**](/windows/desktop/Midl/handle-t) esplicito della routine o usando l'attributo handle esplicito, è necessario passare un handle valido come argomento della \[ [**\_**](/windows/desktop/Midl/explicit-handle) \] chiamata. Per altre informazioni su come creare un handle di serializzazione valido, vedere [Handle](serialization-handles.md)di serializzazione , [Esempi](fixed-buffer-serialization.md)di codifica del buffer fisso ed Esempi di [codifica incrementale](examples-of-incremental-encoding.md).

> [!Note]
> Microsoft RPC consente di mixare le procedure remote e di serializzazione in un'unica interfaccia. Tuttavia, prestare attenzione quando si esegue questa operazione.
> 
> Per le procedure remote con handle di associazione implicita, il compilatore MIDL genera una variabile di handle globale di tipo [**handle \_ t**](/windows/desktop/Midl/handle-t). Le routine e i tipi con handle di serializzazione implicita usano la stessa variabile di handle globale.
> 
> Per gli handle impliciti, l'handle implicito globale deve essere impostato su un handle di associazione valido prima di una chiamata remota. L'handle implicito deve essere impostato su un handle di serializzazione valido prima di una chiamata di serializzazione. Pertanto, una routine non può essere sia remota che serializzata. Deve essere uno o l'altro.

 

 

 