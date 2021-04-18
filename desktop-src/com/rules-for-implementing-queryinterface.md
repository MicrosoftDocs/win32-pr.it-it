---
title: Regole per l'implementazione di QueryInterface
description: Regole per l'implementazione di QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300501"
---
# <a name="rules-for-implementing-queryinterface"></a>Regole per l'implementazione di QueryInterface

Esistono tre regole principali che regolano l'implementazione del metodo [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) su un oggetto com:

-   Gli oggetti devono avere Identity.
-   Il set di interfacce in un'istanza di oggetto deve essere statico.
-   Deve essere possibile eseguire una query corretta per qualsiasi interfaccia di un oggetto da qualsiasi altra interfaccia.

## <a name="objects-must-have-identity"></a>Gli oggetti devono avere identità

Per ogni istanza di oggetto specificata, una chiamata a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) con IID \_ IUnknown deve sempre restituire lo stesso valore del puntatore fisico. In questo modo è possibile chiamare **QueryInterface** su due interfacce e confrontare i risultati per determinare se puntano alla stessa istanza di un oggetto.

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>Il set di interfacce in un'istanza di oggetto deve essere statico

Il set di interfacce accessibili in un oggetto tramite [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) deve essere statico e non dinamico. In particolare, se **QueryInterface** restituisce \_ un valore OK per un determinato IID una volta, non deve mai restituire E \_ nointerface sulle chiamate successive sullo stesso oggetto. Se **QueryInterface** restituisce e \_ nointerface per un determinato IID, le chiamate successive per lo stesso IID sullo stesso oggetto non devono mai restituire S \_ OK.

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>Deve essere possibile eseguire query correttamente per qualsiasi interfaccia di un oggetto da qualsiasi altra interfaccia

Ovvero, dato il codice seguente:

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

si applicano le regole seguenti:

-   Se si dispone di un puntatore a un'interfaccia su un oggetto, una chiamata come la seguente a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per la stessa interfaccia deve avere esito positivo:

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   Se una chiamata a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per un secondo puntatore di interfaccia ha esito positivo, anche una chiamata a **QueryInterface** da tale puntatore per la prima interfaccia deve avere esito positivo. Se pB è stato ottenuto correttamente, è necessario che venga eseguita anche la seguente operazione:

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   Qualsiasi interfaccia deve essere in grado di eseguire query per qualsiasi altra interfaccia in un oggetto. Se pB è stato ottenuto correttamente ed è stata eseguita una query per una terza interfaccia (IC) usando tale puntatore, è necessario anche essere in grado di eseguire query correttamente per IC usando il primo puntatore, pA. In questo caso, la sequenza seguente deve avere esito positivo:

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

Le implementazioni dell'interfaccia devono mantenere un contatore dei riferimenti di puntatore in attesa a tutte le interfacce su un oggetto specificato. Usare un **unsigned integer** per il contatore.

Se un client deve tenere presente che le risorse sono state liberate, deve usare un metodo in un'interfaccia nell'oggetto con una semantica di livello superiore prima di chiamare [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso e implementazione di IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 