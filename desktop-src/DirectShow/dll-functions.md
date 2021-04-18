---
description: In questo argomento viene descritto come implementare un componente come libreria di collegamento dinamico (DLL) in Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funzioni DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303747"
---
# <a name="dll-functions"></a>Funzioni DLL

In questo argomento viene descritto come implementare un componente come libreria di collegamento dinamico (DLL) in Microsoft DirectShow.

Una DLL deve implementare le funzioni seguenti in modo che sia possibile registrarla, annullarne la registrazione e caricarla in memoria.

-   [*DllMain*](/windows/desktop/Dlls/dllmain): il punto di ingresso della dll. Il nome *DllMain* è un segnaposto per il nome della funzione definita dalla libreria. L'implementazione di DirectShow usa il nome **DllEntryPoint**. Per ulteriori informazioni, vedere Platform SDK.
-   [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): crea un'istanza di class factory. Descritto nelle sezioni precedenti.
-   [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): esegue una query per determinare se la dll può essere scaricata in modo sicuro.
-   [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): crea le voci del registro di sistema per la dll.
-   [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): rimuove le voci del registro di sistema per la dll.

Di queste, le prime tre sono implementate da DirectShow. Se il modello Factory fornisce una funzione di inizializzazione nella variabile membro [**\_ lpfnInit m**](cfactorytemplate-m-lpfninit.md) , tale funzione viene chiamata dall'interno della funzione del punto di ingresso della dll. Per ulteriori informazioni su quando il sistema chiama la funzione del punto di ingresso della DLL, vedere [*DllMain*](/windows/desktop/Dlls/dllmain).

È necessario implementare [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), ma DirectShow fornisce una funzione denominata [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) che esegue le operazioni necessarie. Il componente può semplicemente eseguire il wrapping di questa funzione, come illustrato nell'esempio seguente:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



Tuttavia, all'interno di [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) è possibile personalizzare il processo di registrazione in base alle esigenze. Se la DLL contiene un filtro, potrebbe essere necessario eseguire alcune operazioni aggiuntive. Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).

Nel file di definizione del modulo (con estensione def) esportare tutte le funzioni DLL eccetto la funzione del punto di ingresso. Di seguito è riportato un esempio di file con estensione def:


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



È possibile registrare la DLL utilizzando l'utilità Regsvr32.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una DLL di filtro DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
