---
title: Regole per l'implementazione di QueryInterface
description: Regole per l'implementazione di QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0d0df2d0382c670ed6f4a323f55dcdd1b187430282abe6699da186e574e390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047869"
---
# <a name="rules-for-implementing-queryinterface"></a>Regole per l'implementazione di QueryInterface

Esistono tre regole principali che regolano l'implementazione [**del metodo IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) in un oggetto COM:

-   Gli oggetti devono avere un'identità.
-   Il set di interfacce in un'istanza di oggetto deve essere statico.
-   Deve essere possibile eseguire correttamente una query per qualsiasi interfaccia su un oggetto da qualsiasi altra interfaccia.

## <a name="objects-must-have-identity"></a>Gli oggetti devono avere un'identità

Per qualsiasi istanza di oggetto specificata, una chiamata a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) con IID \_ IUnknown deve sempre restituire lo stesso valore del puntatore fisico. In questo modo è possibile chiamare **QueryInterface** su due interfacce qualsiasi e confrontare i risultati per determinare se puntano alla stessa istanza di un oggetto.

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>Il set di interfacce in un'istanza di oggetto deve essere statico

Il set di interfacce accessibili in un oggetto tramite [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) deve essere statico, non dinamico. In particolare, se **QueryInterface** restituisce S OK per un IID specificato una sola volta, non deve mai restituire E NOINTERFACE nelle chiamate successive sullo stesso oggetto. Se QueryInterface restituisce E NOINTERFACE per un \_ \_ determinato IID,  le chiamate successive per lo stesso IID sullo stesso oggetto non devono mai restituire \_ S \_ OK.

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>Deve essere possibile eseguire correttamente una query per qualsiasi interfaccia su un oggetto da qualsiasi altra interfaccia

In altri modi, dato il codice seguente:

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

Si applicano le regole seguenti:

-   Se si dispone di un puntatore a un'interfaccia su un oggetto, una chiamata simile alla seguente a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per la stessa interfaccia deve avere esito positivo:

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   Se una chiamata a [**QueryInterface per un**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) secondo puntatore a interfaccia ha esito positivo, anche una chiamata a **QueryInterface** da tale puntatore per la prima interfaccia deve avere esito positivo. Se pB è stato ottenuto correttamente, anche gli elementi seguenti devono avere esito positivo:

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   Qualsiasi interfaccia deve essere in grado di eseguire una query per qualsiasi altra interfaccia su un oggetto. Se pB è stato ottenuto correttamente e si esegue correttamente una query per una terza interfaccia (IC) usando tale puntatore, è anche necessario essere in grado di eseguire correttamente una query per IC usando il primo puntatore, pA. In questo caso, la sequenza seguente deve avere esito positivo:

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

Le implementazioni dell'interfaccia devono mantenere un contatore dei riferimenti ai puntatori in sospeso a tutte le interfacce in un determinato oggetto. È consigliabile usare **un intero senza segno** per il contatore.

Se un client deve sapere che le risorse sono state liberate, deve usare un metodo in un'interfaccia dell'oggetto con semantica di livello superiore prima di chiamare [**IUnknown::Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso e implementazione di IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 