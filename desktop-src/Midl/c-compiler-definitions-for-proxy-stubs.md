---
title: Definizioni del compilatore C per proxy/stub
description: Il file di intestazione Rpcproxy.h include le definizioni di macro seguenti, ognuna delle quali può risultare utile quando si compila un'applicazione COM distribuita. Queste macro vengono richiamate con l'opzione del preprocessore /D (o -D) in fase di compilazione C.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL del compilatore MIDL, compilatore C, definizioni per proxy/stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f12b9fd1e2688545137dba870816c1765102ce3593d09ea3cb062bd8250c7c28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807836"
---
# <a name="c-compiler-definitions-for-proxystubs"></a>Definizioni del compilatore C per proxy/stub

Il file di intestazione Rpcproxy.h include le definizioni di macro seguenti, ognuna delle quali può risultare utile quando si compila un'applicazione COM distribuita. Queste macro vengono richiamate con l'opzione del preprocessore [**/D**](-d.md) (o -D) in fase di compilazione C.



| MACRO                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REGISTRARE \_ LA \_ DLL PROXY                                                                                                                                                                            | Genera **le funzioni DllMain**, **DllRegisterServer** e **DllUnregisterServer** per la registrazione automatica di una DLL proxy.                                                                                       |
| \_CLSID PROXY=<clsid>                                                                                                                                                                      | Specifica un identificatore di classe per il server. Se questa macro non è definita, il CLSID predefinito è il primo identificatore di interfaccia rilevato dal compilatore MIDL nella specifica IDL per il server Proxy/Stub. |
| CLSID PROXY \_ \_ IS={0x *8hexdigits,* 0x *4hexdigits*,0x *4hexdigits,*{0x *2hexdigits**,0x 2hexdigits, 0xdigits,* 0x *2hexdigits*,0x *2hexdigits,* 0x *2hexdigits*,0x *2hexdigits,* 0x *2hexdigits*,0x *2hexdigits*,}} | Specifica il valore dell'identificatore di classe del server in formato esadecimale binario.                                                                                                                                           |



 

Definendo la macro **REGISTER \_ PROXY \_ DLL** durante la compilazione di Dlldata.c, la DLL di marshalling proxy/stub includerà automaticamente le definizioni predefinite per le funzioni **DllMain**, **DllRegisterServer** e **DllUnregisterServer.** È possibile usare queste funzioni per registrare automaticamente la DLL proxy nel Registro di sistema.

Questo codice di registrazione predefinito usa il GUID della prima interfaccia rilevata come CLSID per la registrazione dell'intero server DLL proxy/stub. COM usa successivamente questo CLSID per individuare e caricare il server proxy/stub compilato per il marshalling di una delle interfacce che il server deve gestire. Quando un'applicazione effettua una chiamata al metodo di interfaccia che attraversa i limiti di thread, processi o computer, COM usa la voce del Registro di sistema dell'identificatore di interfaccia per individuare la voce del Registro di sistema CLSID per il server di marshalling proxy/stub. Usa quindi questo CLSID per caricare il server (se non è già caricato) in modo che sia possibile effettuare il marshalling della chiamata di interfaccia.

Usare la macro **\_ PROXY CLSID** quando si vuole specificare in modo esplicito il CLSID del server proxy/stub anziché basarsi sul = <clsid> CLSID predefinito. Ad esempio, se si compila una DLL di marshalling standard come server COM in-process o se è necessario definire una **dllmain** personalizzata per gestire DLL \_ PROCESS \_ ATTACH.

Usare **PROXY \_ CLSID \_ IS**= macro anziché **\_ CLSID PROXY** per definire il valore del CLSID nel formato esadecimale binario utilizzato dalla macro DEFINE **\_ GUID.**

Si noti inoltre che quando viene eseguita la funzione **DllRegisterServer** predefinita, il server viene registrato con ThreadingModel=Both.

L'esempio di makefile seguente usa **le macro REGISTER PROXY \_ \_ DLL** e **PROXY \_ CLSID**= :

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

Per altre informazioni [**sull'opzione del preprocessore /D,**](-d.md) vedere la documentazione del compilatore C.

 

 




