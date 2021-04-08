---
title: Compilazione e registrazione di una DLL proxy
description: Se è stato scelto il marshalling del proxy/stub per l'applicazione, i file. c e. h generati da MIDL devono essere compilati e collegati per creare una DLL proxy e tale DLL deve essere inserita nel registro di sistema in modo che i client possano individuare le interfacce.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b0dcd28359172ff2f90391d44a66f8f51a4cbf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730514"
---
# <a name="building-and-registering-a-proxy-dll"></a>Compilazione e registrazione di una DLL proxy

Se è stato scelto il marshalling del proxy/stub per l'applicazione, i file. c e. h generati da MIDL devono essere compilati e collegati per creare una DLL proxy e tale DLL deve essere inserita nel registro di sistema in modo che i client possano individuare le interfacce. Il file generato da MIDL dlldata. c contiene le routine e altre informazioni necessarie per compilare e registrare una DLL proxy/stub.

Il primo passaggio nella creazione della DLL consiste nel scrivere un file di definizione del modulo per il linker, come illustrato nell'esempio seguente:

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

In alternativa, è possibile specificare queste funzioni esportate nella riga di comando del collegamento del makefile.

Le funzioni esportate sono dichiarate in Rpcproxy. h, che dlldata. c include e le implementazioni predefinite fanno parte della libreria di runtime RPC. COM utilizza queste funzioni per creare un class factory, scaricare le dll (dopo aver verificato che non esistano oggetti o blocchi), recuperare informazioni sulla DLL proxy e registrare e annullare la registrazione della DLL del proxy. Per sfruttare i vantaggi di queste funzioni predefinite, è necessario richiamare l'opzione Cpreprocessor/D (o-D) quando si compilano i file dlldata. c e \_ p. c di esempio, come illustrato nel makefile seguente:

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
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(ORIXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

Se non si specificano queste definizioni per il preprocessore in fase di compilazione, queste funzioni non vengono definite automaticamente. (Ovvero, le macro in Rpcproxy. c si espandono su Nothing). È necessario che siano stati definiti in modo esplicito in un altro file di origine, il cui modulo verrebbe incluso anche nel collegamento e nella compilazione finali nella riga di comando del compilatore C.

Quando \_ \_ si definisce la dll del proxy di registrazione, Rpcproxy. h fornisce un ulteriore controllo di compilazione condizionale con proxy \_ CLSID =*GUID*, il \_ CLSID proxy \_ è =*valore esplicito GUID* e \_ prefisso voce =*stringa prefisso*. Queste definizioni di macro sono descritte più dettagliatamente nelle [definizioni del compilatore C per proxy/stub](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in MIDL Programmer ' s Guide.

## <a name="manually-registering-the-proxy-dll"></a>Registrazione manuale della DLL proxy

Se per qualche motivo non è possibile usare le routine di registrazione stub proxy predefinite, è possibile registrare manualmente la DLL aggiungendo le voci seguenti al registro di sistema, usando Regedt32.exe.

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

 

 