---
title: Compilazione e registrazione di una DLL proxy
description: Se si sceglie il marshalling proxy/stub per l'applicazione, i file con estensione c e h generati da MIDL devono essere compilati e collegati per creare una DLL proxy e tale DLL deve essere immessa nel Registro di sistema in modo che i client possano individuare le interfacce.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634cb7a17551a4b7925d0be3065c71037cc1d7ae8bf28c10fcdaee74771c302e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048849"
---
# <a name="building-and-registering-a-proxy-dll"></a>Compilazione e registrazione di una DLL proxy

Se si sceglie il marshalling proxy/stub per l'applicazione, i file con estensione c e h generati da MIDL devono essere compilati e collegati per creare una DLL proxy e tale DLL deve essere immessa nel Registro di sistema in modo che i client possano individuare le interfacce. Il file dlldata.c generato da MIDL contiene le routine necessarie e altre informazioni per compilare e registrare una DLL proxy/stub.

Il primo passaggio per la compilazione della DLL consiste nello scrivere un file di definizione del modulo per il linker, come illustrato nell'esempio seguente:

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

In alternativa, è possibile specificare queste funzioni esportate nella riga di comando LINK del makefile.

Le funzioni esportate vengono dichiarate in Rpcproxy.h, incluso in Dlldata.c, e le implementazioni predefinite fanno parte della libreria di runtime RPC. COM usa queste funzioni per creare un class factory, scaricare le DLL (dopo aver verificato che non esistano oggetti o blocchi), recuperare informazioni sulla DLL proxy e per autoregistrare e annullare la registrazione della DLL proxy. Per sfruttare queste funzioni predefinite, è necessario richiamare l'opzione Cpreprocessor /D (o -D) quando si compilano i file Dlldata.c e Example p.c, come illustrato nel \_ makefile seguente:

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJS) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

Se non si specificano queste definizioni del preprocessore in fase di compilazione, queste funzioni non vengono definite automaticamente. Ovvero, le macro in Rpcproxy.c non si espandono fino a nulla. È necessario averli definiti in modo esplicito in un altro file di origine, il cui modulo verrebbe incluso anche nel collegamento e nella compilazione finali nella riga di comando del compilatore C.

Quando viene definita la DLL REGISTER PROXY, Rpcproxy.h fornisce un controllo di compilazione condizionale aggiuntivo con \_ \_ \_ CLSID PROXY=*guid,* \_ CLSID PROXY IS= \_ valore \_ esplicito di guid e ENTRY PREFIX= stringa di prefisso . Queste definizioni di macro sono descritte in modo più dettagliato in Definizioni del compilatore [C per proxy/stub](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) nella Guida per programmatori MIDL.

## <a name="manually-registering-the-proxy-dll"></a>Registrazione manuale della DLL del proxy

Se per qualche motivo non è possibile usare le routine di registrazione stub proxy predefinite, è possibile registrare manualmente la DLL aggiungendo le voci seguenti al Registro di sistema, usando Regedt32.exe.

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Definizioni del compilatore C per proxy/stub](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Registrazione automatica](self-registration.md)
</dt> </dl>

 

 
