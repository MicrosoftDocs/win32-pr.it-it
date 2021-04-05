---
title: Oggetti e interfacce COM
description: Oggetti e interfacce COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707786"
---
# <a name="com-objects-and-interfaces"></a>Oggetti e interfacce COM

COM è una tecnologia che consente agli oggetti di interagire tra i confini dei processi e dei computer con la stessa facilità con cui avviene all'interno di un singolo processo. COM consente di specificare che l'unico modo per modificare i dati associati a un oggetto consiste nell'usare un' *interfaccia* sull'oggetto. Quando questo termine viene usato in questa documentazione, si riferisce a un'implementazione nel codice di un'interfaccia conforme a binari COM associata a un oggetto.

COM usa l' *interfaccia* di Word in un senso diverso da quello usato in genere nella programmazione Visual C++. Un'interfaccia C++ fa riferimento a tutte le funzioni supportate da una classe e che i client di un oggetto possono chiamare per interagire con esso. Un'interfaccia COM fa riferimento a un gruppo predefinito di funzioni correlate implementate da una classe COM, ma un'interfaccia specifica non rappresenta necessariamente tutte le funzioni supportate dalla classe.

Il riferimento a un oggetto che *implementa* un'interfaccia significa che l'oggetto utilizza codice che implementa ogni metodo dell'interfaccia e fornisce puntatori conformi a binari com a tali funzioni alla libreria com. COM rende quindi tali funzioni disponibili a qualsiasi client che chiede un puntatore all'interfaccia, indipendentemente dal fatto che il client si trovi all'interno o all'esterno del processo che implementa tali funzioni.

Per altre informazioni, vedere i seguenti argomenti:

-   [Interfacce e implementazioni di interfaccia](interfaces-and-interface-implementations.md)
-   [Puntatori a interfaccia e interfacce](interface-pointers-and-interfaces.md)
-   [IUnknown ed ereditarietà dell'interfaccia](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce](interfaces.md)
</dt> </dl>

 

 




