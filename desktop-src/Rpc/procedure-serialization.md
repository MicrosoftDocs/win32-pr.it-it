---
title: Serializzazione delle procedure
description: Quando si usa la serializzazione delle procedure, una stored procedure viene etichettata con l'attributo \ Encode \ o \ Decode \. Anziché generare lo stub remoto consueto, il compilatore genera uno stub di serializzazione per la routine.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77696761a9aa5fe1471e9ebf24a57303b15d0ff3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401837"
---
# <a name="procedure-serialization"></a>Serializzazione delle procedure

Quando si utilizza la serializzazione delle procedure, una stored procedure viene contrassegnata con l' \[ attributo [**Encode**](/windows/desktop/Midl/encode) \] o \[ [**Decode**](/windows/desktop/Midl/decode) \] . Anziché generare lo stub remoto consueto, il compilatore genera uno stub di serializzazione per la routine.

Proprio come una procedura remota deve usare un handle di associazione per effettuare una chiamata remota, una procedura di serializzazione deve usare un handle di serializzazione per usare i servizi di serializzazione. Se non si specifica un handle di serializzazione, viene usato un handle implicito predefinito per indirizzare la chiamata. D'altra parte, se viene specificato l'handle di serializzazione, come argomento di [**handle \_**](/windows/desktop/Midl/handle-t) esplicito t della routine o mediante l'attributo \[ [**\_ handle esplicito**](/windows/desktop/Midl/explicit-handle) \] , è necessario passare un handle valido come argomento della chiamata. Per ulteriori informazioni su come creare un handle di serializzazione valido, vedere [handle di serializzazione](serialization-handles.md), [esempi di codifica di buffer fissi](fixed-buffer-serialization.md)ed [esempi di codifica incrementale](examples-of-incremental-encoding.md).

> [!Note]
> Microsoft RPC consente di combinare le procedure remote e di serializzazione in un'unica interfaccia. Tuttavia, prestare attenzione quando si esegue questa operazione.
> 
> Per le procedure remote con handle di associazione impliciti, il compilatore MIDL genera una variabile di handle globale di tipo [**handle \_ t**](/windows/desktop/Midl/handle-t). Le procedure e i tipi con handle di serializzazione implicita utilizzano questa stessa variabile di handle globale.
> 
> Per gli handle impliciti, l'handle implicito globale deve essere impostato su un handle di associazione valido prima di una chiamata remota. L'handle implicito deve essere impostato su un handle di serializzazione valido prima di una chiamata di serializzazione. Pertanto, una routine non può essere sia remota che serializzata. Deve essere uno o l'altro.

 

 

 