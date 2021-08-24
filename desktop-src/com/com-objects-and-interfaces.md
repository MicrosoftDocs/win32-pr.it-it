---
title: Interfacce e oggetti COM
description: Interfacce e oggetti COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a663b5d6e5966422927e37f1501924bf8ec8921210c9d38765153dc0d80fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501551"
---
# <a name="com-objects-and-interfaces"></a>Interfacce e oggetti COM

COM è una tecnologia che consente agli oggetti di interagire tra i limiti dei processi e dei computer con la facilità con cui si trova all'interno di un singolo processo. COM consente questa operazione specificando che l'unico modo per modificare i dati associati a un oggetto è tramite *un'interfaccia* sull'oggetto. Quando questo termine viene usato in questa documentazione, si riferisce a un'implementazione nel codice di un'interfaccia COM conforme a binaria associata a un oggetto.

COM usa la parola *interfaccia* in senso diverso da quello in genere usato nella programmazione Visual C++. Un'interfaccia C++ fa riferimento a tutte le funzioni supportate da una classe e che i client di un oggetto possono chiamare per interagire con essa. Un'interfaccia COM fa riferimento a un gruppo predefinito di funzioni correlate implementate da una classe COM, ma un'interfaccia specifica non rappresenta necessariamente tutte le funzioni supportate dalla classe.

Fare riferimento  a un oggetto che implementa un'interfaccia significa che l'oggetto usa codice che implementa ogni metodo dell'interfaccia e fornisce puntatori COM conformi a binari a tali funzioni alla libreria COM. COM rende quindi disponibili tali funzioni a qualsiasi client che richiede un puntatore all'interfaccia, se il client si trova all'interno o all'esterno del processo che implementa tali funzioni.

Per altre informazioni, vedere i seguenti argomenti:

-   [Interfacce e implementazioni di interfacce](interfaces-and-interface-implementations.md)
-   [Puntatori a interfaccia e interfacce](interface-pointers-and-interfaces.md)
-   [Ereditarietà di interfaccia e IUnknown](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce](interfaces.md)
</dt> </dl>

 

 




