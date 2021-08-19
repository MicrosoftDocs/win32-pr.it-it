---
description: Questo argomento descrive come implementare un componente come libreria a collegamento dinamico (DLL) in Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funzioni DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8c10951c63e14656fa967693145444c5d5fbffd96a2b11fa9ae4201ac89ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821085"
---
# <a name="dll-functions"></a>Funzioni DLL

Questo argomento descrive come implementare un componente come libreria a collegamento dinamico (DLL) in Microsoft DirectShow.

Una DLL deve implementare le funzioni seguenti in modo che possa essere registrata, annullata e caricata in memoria.

-   [*DllMain:*](/windows/desktop/Dlls/dllmain)punto di ingresso DLL. Il nome *DllMain* è un segnaposto per il nome della funzione definita dalla libreria. L DirectShow'implementazione usa il nome **DllEntryPoint**. Per altre informazioni, vedere Platform SDK.
-   [**DllGetClassObject:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject)crea un'class factory predefinita. Descritto nelle sezioni precedenti.
-   [**DllCanUnloadNow:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)esegue una query per determinare se la DLL può essere scaricata in modo sicuro.
-   [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): crea voci del Registro di sistema per la DLL.
-   [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): rimuove le voci del Registro di sistema per la DLL.

Di questi, i primi tre vengono implementati da DirectShow. Se il modello factory fornisce una funzione di inizializzazione nella variabile membro [**m \_ lpfnInit,**](cfactorytemplate-m-lpfninit.md) tale funzione viene chiamata dall'interno della funzione del punto di ingresso della DLL. Per altre informazioni su quando il sistema chiama la funzione del punto di ingresso DLL, vedere [*DllMain*](/windows/desktop/Dlls/dllmain).

È necessario [**implementare DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer,**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)ma DirectShow fornisce una funzione denominata [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) che esegue le operazioni necessarie. Il componente può semplicemente eseguire il wrapping di questa funzione, come illustrato nell'esempio seguente:


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



Tuttavia, [**all'interno di DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) è possibile personalizzare il processo di registrazione in base alle esigenze. Se la DLL contiene un filtro, potrebbe essere necessario eseguire alcune operazioni aggiuntive. Per altre informazioni, vedere [Come registrare DirectShow filtri](how-to-register-directshow-filters.md).

Nel file di definizione del modulo (def) esportare tutte le funzioni DLL ad eccezione della funzione del punto di ingresso. Di seguito è riportato un file def di esempio:


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



È possibile registrare la DLL usando l'Regsvr32.exe comando.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una DLL DirectShow filtro](how-to-create-a-dll.md)
</dt> </dl>

 

 
