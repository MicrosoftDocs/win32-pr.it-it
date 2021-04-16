---
title: Self-Registration
description: La registrazione automatica è il mezzo standard attraverso il quale un modulo server può creare un pacchetto delle proprie operazioni del registro di sistema, sia di registrazione che di annullamento della registrazione, nel modulo stesso.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474355"
---
# <a name="self-registration"></a>Self-Registration

Poiché il software dei componenti continua a crescere come mercato, saranno presenti più istanze in cui un utente ottiene un nuovo componente software come singolo modulo DLL o EXE, ad esempio quando Scarica un nuovo componente da un servizio online o ne riceve uno da un amico su un disco floppy. In questi casi, non è pratico richiedere all'utente di eseguire una lunga procedura di installazione o programma di installazione. Oltre ai problemi relativi alle licenze, che vengono gestiti tramite [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), una procedura di installazione crea in genere le voci del registro di sistema necessarie per l'esecuzione corretta di un componente nel contesto com e OLE.

La registrazione automatica è il mezzo standard attraverso il quale un modulo server può creare un pacchetto delle proprie operazioni del registro di sistema, sia di registrazione che di annullamento della registrazione, nel modulo stesso. Quando viene usato con le licenze gestite tramite [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), un server può diventare un modulo completamente autonomo senza necessità di programmi di installazione esterni o file reg.

Qualsiasi modulo di registrazione automatica, DLL o EXE, deve prima includere una stringa "OleSelfRegister" nella sezione [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) della relativa risorsa di informazioni sulla versione, come illustrato di seguito.

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

L'esistenza di questi dati consente a qualsiasi parte interessata, ad esempio un'applicazione che desidera integrare questo nuovo componente, di determinare se il server supporta la registrazione automatica senza dover prima caricare la DLL o EXE.

Se il server è incluso in un modulo DLL, è necessario che la DLL esporti le funzioni [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Qualsiasi applicazione che desidera indicare al server di registrarsi, ovvero tutti i relativi CLSID e ID della libreria dei tipi, può ottenere un puntatore a **DllRegisterServer** tramite la funzione [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) . In **DllRegisterServer**, la dll crea tutte le voci del registro di sistema necessarie, archiviando il percorso corretto della dll per tutte le voci [InprocServer32](inprocserver32.md) o [InprocHandler32](inprochandler32.md) .

Quando un'applicazione desidera rimuovere il componente dal sistema, è necessario annullare la registrazione del componente chiamando [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). All'interno di questa chiamata, il server rimuove esattamente le voci create in precedenza in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver). Il server non deve rimuovere in modo cieco tutte le voci per le relative classi perché altri software potrebbero avere archiviato voci aggiuntive, ad esempio una chiave [Treats](treatas.md) .

Se il server è incluso in un modulo EXE, l'applicazione che vuole registrare il server avvia il server EXE con l'argomento della riga di comando **/regserver** o **-regserver** (senza distinzione tra maiuscole e minuscole). Se l'applicazione vuole annullare la registrazione del server, avvia il file EXE con l'argomento della riga di comando **l'opzione/unregserver** o **-unregserver**. Il file EXE con registrazione automatica rileva questi argomenti della riga di comando e richiama le stesse operazioni di una DLL all'interno di [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), rispettivamente, registrando il percorso del modulo in [LocalServer32](localserver32.md) anziché **InprocServer32** o **InprocHandler32**.

Il server deve registrare il percorso completo del percorso di installazione del modulo DLL o EXE per le rispettive chiavi **InprocServer32**, **InprocHandler32** e **LocalServer32** nel registro di sistema. Il percorso del modulo è facilmente ottenibile tramite la funzione [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazione come applicazione di servizio](installing-as-a-service-application.md)
</dt> <dt>

[Registrazione di una classe durante l'installazione](registering-a-class-at-installation.md)
</dt> <dt>

[Registrazione di un server EXE in esecuzione](registering-a-running-exe-server.md)
</dt> <dt>

[Registrazione di oggetti nella tabella ROT](registering-objects-in-the-rot.md)
</dt> </dl>

 

 