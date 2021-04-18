---
title: Oggetti classe COM e CLSID
description: Un server COM viene implementato come classe COM.
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfde2f379c4c7589db4cde283c8c67d720b21d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300549"
---
# <a name="com-class-objects-and-clsids"></a>Oggetti classe COM e CLSID

Un server COM viene implementato come classe COM. Una *classe com* è un'implementazione di un gruppo di interfacce nel codice eseguito quando si interagisce con un oggetto specificato. Esiste una differenza importante tra una classe C++ e una classe COM: in C++, una classe è un tipo, mentre una classe COM è semplicemente una definizione dell'oggetto e non contiene alcun tipo, sebbene un programmatore C++ possa implementarlo utilizzando una classe C++. COM è progettato per consentire l'utilizzo di una classe da applicazioni diverse, incluse le applicazioni scritte senza conoscere l'esistenza di tale classe. Pertanto, il codice della classe per un determinato tipo di oggetto esiste in una libreria collegata dinamica (DLL) o in un'altra applicazione eseguibile (EXE).

Ogni classe COM è identificata da un *CLSID*, un GUID univoco a 128 bit, che deve essere registrato dal server. COM utilizza questo CLSID, alla richiesta di un client, per associare dati specifici alla DLL o al file EXE contenente il codice che implementa la classe, creando in tal modo un'istanza dell'oggetto.

Per i client e i server nello stesso computer, il CLSID del server è sempre necessario per il client. In ogni computer, COM gestisce un database, ovvero utilizza il registro di sistema nelle piattaforme Microsoft Windows e Macintosh, di tutti i CLSID per i server installati nel sistema. Si tratta di un mapping tra ogni CLSID e il percorso della DLL o del file EXE che ospita il codice per il CLSID. COM consulta questo database ogni volta che un client desidera creare un'istanza di una classe COM e utilizzarne i servizi, in modo che il client non debba mai conoscere il percorso assoluto del codice nel computer.

Per i sistemi distribuiti, COM fornisce voci del registro di sistema che consentono a un server remoto di registrarsi per l'uso da un client. Sebbene sia necessario che le applicazioni conoscano solo il CLSID di un server, perché possono basarsi sul Registro di sistema per individuare il server, COM consente ai client di eseguire l'override delle voci del registro di sistema e di specificare i percorsi del server, per sfruttare al meglio la rete. Vedere [individuazione di un oggetto remoto](locating-a-remote-object.md).

Il modo più semplice per creare un'istanza di una classe consiste nell'usare un *oggetto classe* com. Si tratta semplicemente di un oggetto intermedio che supporta funzioni comuni alla creazione di nuove istanze di una determinata classe. La maggior parte degli oggetti classe utilizzati per creare oggetti da un CLSID supporta l'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , un'interfaccia che include il metodo [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) importante. Si implementa un'interfaccia **IClassFactory** per ogni classe di oggetto offerta per la creazione di un'istanza. Per ulteriori informazioni sull'implementazione di **IClassFactory**, vedere [Implementing IClassFactory](implementing-iclassfactory.md).

> [!Note]  
> I server che supportano alcune altre interfacce di class factory personalizzate non devono supportare [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) in modo specifico. Tuttavia, le chiamate alle funzioni di attivazione diverse da [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (ad esempio [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)) richiedono che il server supporti **IClassFactory**.

 

Quando un client vuole creare un'istanza dell'oggetto del server, usa il CLSID dell'oggetto desiderato in una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject). Questa chiamata può essere diretta o implicita tramite una delle funzioni di supporto per la creazione di oggetti. Questa funzione individua il codice associato al CLSID e crea un oggetto classe e fornisce un puntatore all'interfaccia richiesta. (**CoGetClassObject** accetta un parametro *riid* che specifica il puntatore a interfaccia desiderato del client).

> [!Note]  
> COM dispone solo di alcune funzioni sulle quali sono state compilate molte altre. Il più importante di questi è probabilmente [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), che si basa su tutte le funzioni di creazione dell'istanza.

 

Con questo puntatore, il chiamante può creare un'istanza dell'oggetto e recuperare un puntatore a un'interfaccia richiesta nell'oggetto. Si tratta in genere di un'interfaccia di inizializzazione, usata per attivare l'oggetto (inserirlo nello stato di esecuzione), in modo che il client possa eseguire qualsiasi operazione con l'oggetto desiderato. Utilizzando le funzioni di base di COM, il client deve inoltre prestare attenzione a rilasciare tutti i puntatori a oggetti.

Un altro meccanismo per attivare le istanze degli oggetti è tramite il moniker della classe. I moniker della classe sono associati all'oggetto classe della classe per cui sono stati creati. Per ulteriori informazioni, vedere [moniker della classe](class-monikers.md).

COM fornisce diverse funzioni helper che consentono di ridurre il lavoro di creazione di istanze di oggetti. Questi sono descritti in [funzioni helper](instance-creation-helper-functions.md)per la creazione di istanze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 