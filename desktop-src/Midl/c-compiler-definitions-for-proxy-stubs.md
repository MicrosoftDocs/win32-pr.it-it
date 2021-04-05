---
title: Definizioni del compilatore C per proxy/stub
description: Il file di intestazione Rpcproxy. h include le definizioni di macro seguenti, ognuna delle quali può risultare utile quando si compila un'applicazione COM distribuita. Queste macro vengono richiamate con l'opzione del preprocessore/D (o-D) in fase di compilazione C.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL compilatore MIDL, compilatore C, definizioni per proxy/stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1504c600c3f86a934ab3daa132b041c7310af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045110"
---
# <a name="c-compiler-definitions-for-proxystubs"></a>Definizioni del compilatore C per proxy/stub

Il file di intestazione Rpcproxy. h include le definizioni di macro seguenti, ognuna delle quali può risultare utile quando si compila un'applicazione COM distribuita. Queste macro vengono richiamate con l'opzione del preprocessore [**/d**](-d.md) (o-D) in fase di compilazione C.



| MACRO                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Registra \_ \_ dll proxy                                                                                                                                                                            | Genera funzioni **DllMain**, **DllRegisterServer** e **DllUnregisterServer** per la registrazione automatica di una DLL proxy.                                                                                       |
| \_CLSID proxy =<clsid>                                                                                                                                                                      | Specifica un identificatore di classe per il server. Se questa macro non è definita, il CLSID predefinito è il primo identificatore di interfaccia rilevato dal compilatore MIDL nella specifica IDL per il server proxy/stub. |
| Il \_ CLSID \_ proxy è = {*0x 8hexdigits*, 0x *4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x 2hexdigits, 0x 2hexdigits, 0x 2hexdigits, 0x *2hexdigits*,}} | Specifica il valore dell'identificatore di classe del server in formato esadecimale binario.                                                                                                                                           |



 

Definendo la macro **Register \_ proxy \_ dll** quando si compila dlldata. c, la dll di marshalling del proxy/stub includerà automaticamente le definizioni predefinite per le funzioni **DllMain**, **DllRegisterServer** e **DllUnregisterServer** . È possibile usare queste funzioni per registrare autonomamente la DLL del proxy nel registro di sistema.

Questo codice di registrazione predefinito usa il GUID della prima interfaccia rilevata come CLSID per la registrazione dell'intero server DLL proxy/stub. COM in un secondo momento utilizza questo CLSID per individuare e caricare il server proxy/stub compilato per il marshalling di qualsiasi interfaccia registrata dal server per la gestione. Quando un'applicazione esegue una chiamata al metodo di interfaccia che supera i limiti dei thread, dei processi o dei computer, COM utilizza la voce del registro di sistema Identifier per individuare la voce del registro di sistema CLSID per il server di marshalling del proxy/stub. USA quindi questo CLSID per caricare il server, se non è già caricato, in modo che sia possibile effettuare il marshalling della chiamata di interfaccia.

Utilizzare la macro **proxy \_ CLSID** = <clsid> quando si desidera specificare in modo esplicito il CLSID del server proxy/stub anziché basarsi sul CLSID predefinito. Se, ad esempio, si compila una DLL di marshalling standard come server COM in-process, oppure se è necessario definire una proprietà **DllMain** personalizzata per gestire la \_ connessione al processo dll \_ .

Use **proxy \_ CLSID \_ is**= macro anziché **proxy \_ CLSID** per definire il valore del CLSID nel formato esadecimale binario utilizzato dalla macro del **\_ GUID define** .

Si noti inoltre che quando viene eseguita la funzione **DllRegisterServer** predefinita, viene registrato il server con ThreadingModel = both.

Nell'esempio di makefile seguente vengono usate le macro **Register \_ proxy \_ dll** e **proxy \_ CLSID**= Macros:

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

Per ulteriori informazioni sull'opzione [**/d**](-d.md) preprocessore, vedere la documentazione del compilatore C.

 

 




