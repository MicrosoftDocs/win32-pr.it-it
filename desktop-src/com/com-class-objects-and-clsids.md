---
title: Oggetti classe COM e CLSID
description: Un server COM viene implementato come classe COM.
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6bcd00f886d3a754a44658e669189d28fd2fa121248b667ba2a3928b626f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550625"
---
# <a name="com-class-objects-and-clsids"></a>Oggetti classe COM e CLSID

Un server COM viene implementato come classe COM. Una *classe COM* è un'implementazione di un gruppo di interfacce nel codice eseguito ogni volta che si interagisce con un determinato oggetto. Esiste un'importante distinzione tra una classe C++ e una classe COM: in C++, una classe è un tipo, mentre una classe COM è semplicemente una definizione dell'oggetto e non contiene alcun tipo, anche se un programmatore C++ potrebbe implementarla usando una classe C++. COM è progettato per consentire l'uso di una classe da parte di applicazioni diverse, incluse le applicazioni scritte senza conoscere l'esistenza di tale classe specifica. Pertanto, il codice della classe per un determinato tipo di oggetto esiste in una libreria collegata dinamica (DLL) o in un'altra applicazione eseguibile (EXE).

Ogni classe COM è identificata da un *CLSID*, un GUID univoco a 128 bit, che il server deve registrare. COM usa questo CLSID, su richiesta di un client, per associare dati specifici alla DLL o al file EXE contenente il codice che implementa la classe , creando così un'istanza dell'oggetto .

Per i client e i server nello stesso computer, il CLSID del server è tutto il client necessario. In ogni computer, COM gestisce un database (usa il Registro di sistema nelle piattaforme Microsoft Windows e Macintosh) di tutti i CLSID per i server installati nel sistema. Si tratta di un mapping tra ogni CLSID e il percorso della DLL o del file EXE che ospita il codice per tale CLSID. COM consulta questo database ogni volta che un client desidera creare un'istanza di una classe COM e usarne i servizi, in modo che il client non deve mai conoscere la posizione assoluta del codice nel computer.

Per i sistemi distribuiti, COM fornisce voci del Registro di sistema che consentono a un server remoto di registrarsi per l'uso da parte di un client. Anche se le applicazioni devono conoscere solo il CLSID di un server, poiché possono basarsi sul Registro di sistema per individuare il server, COM consente ai client di eseguire l'override delle voci del Registro di sistema e di specificare i percorsi del server, per sfruttare appieno la rete. Vedere [Individuazione di un oggetto remoto.](locating-a-remote-object.md)

Il modo di base per creare un'istanza di una classe è tramite un oggetto *classe* COM . Si tratta semplicemente di un oggetto intermedio che supporta funzioni comuni alla creazione di nuove istanze di una determinata classe. La maggior parte degli oggetti di classe usati per creare oggetti da un CLSID supporta [**l'interfaccia IClassFactory,**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) un'interfaccia che include il metodo [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) importante. Si implementa **un'interfaccia IClassFactory** per ogni classe di oggetto di cui è possibile creare un'istanza. Per altre informazioni sull'implementazione di **IClassFactory,** vedere [Implementazione di IClassFactory.](implementing-iclassfactory.md)

> [!Note]  
> I server che supportano altre interfacce class factory non sono necessari per supportare [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) in modo specifico. Tuttavia, le chiamate a funzioni di attivazione diverse [**da CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (ad esempio [**CoCreateInstanceEx)**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)richiedono che il server **supporti IClassFactory.**

 

Quando un client vuole creare un'istanza dell'oggetto del server, usa il CLSID dell'oggetto desiderato in una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject). Questa chiamata può essere diretta o implicita tramite una delle funzioni helper di creazione di oggetti. Questa funzione individua il codice associato al CLSID, crea un oggetto classe e fornisce un puntatore all'interfaccia richiesta. (**CoGetClassObject** accetta un *parametro riid* che specifica il puntatore di interfaccia desiderato del client.

> [!Note]  
> COM ha solo alcune funzioni su cui molte delle altre sono compilate. Il più importante di questi è probabilmente [**CoGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)che si trova alla base di tutte le funzioni di creazione dell'istanza.

 

Con questo puntatore, il chiamante può creare un'istanza dell'oggetto e recuperare un puntatore a un'interfaccia richiesta sull'oggetto. Si tratta in genere di un'interfaccia di inizializzazione, usata per attivare l'oggetto (impostarlo sullo stato di esecuzione) in modo che il client possa eseguire qualsiasi operazione con l'oggetto che desidera. Usando le funzioni di base di COM, il client deve anche fare attenzione a rilasciare tutti i puntatori a oggetti.

Un altro meccanismo per attivare le istanze dell'oggetto è tramite il moniker della classe . I moniker di classe vengono associati all'oggetto classe della classe per cui vengono creati. Per altre informazioni, vedere [Moniker di classe.](class-monikers.md)

COM fornisce diverse funzioni helper che riducono il lavoro di creazione di istanze di oggetti. Queste informazioni sono descritte in [Funzioni helper per la creazione di istanze.](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 