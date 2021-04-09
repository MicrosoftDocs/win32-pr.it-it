---
title: Compilazione e collegamento
description: Il makefile seguente mostra le dipendenze tra i file necessari per compilare le applicazioni client e server e collegarle alla libreria di runtime RPC e alla libreria di runtime C standard.
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- RPC, attività, compilazione e collegamento di procedure remote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1991e39cc028c01066cd8f13344765787374fa08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955532"
---
# <a name="compiling-and-linking"></a>Compilazione e collegamento

Il makefile seguente mostra le dipendenze tra i file necessari per compilare le applicazioni client e server e collegarle alla libreria di runtime RPC e alla libreria di runtime C standard.

Questo Makefile può essere usato per creare applicazioni client e server dal codice sorgente in questa esercitazione. Gli stub e le intestazioni mostrati sono stati generati con MIDL versione 2,0. I comandi e gli argomenti del compilatore e del linker possono essere diversi per la configurazione del computer. Per ulteriori informazioni, vedere la documentazione del compilatore.

``` syntax
#makefile for helloc.exe and hellos.exe
#link refers to the linker
#conflags refers to flags for console applications
#conlibs refers to libraries for console applications
 
!include <ntwin32.mak>
 
all : helloc hellos
 
# Make the client side application helloc
helloc : helloc.exe
helloc.exe : helloc.obj hello_c.obj
    $(link) $(linkdebug) $(conflags) -out:helloc.exe \
        helloc.obj hello_c.obj \
        rpcrt4.lib $(conlibs)
 
# helloc main program
helloc.obj : helloc.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# helloc stub
hello_c.obj : hello_c.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# Make the server side application
hellos : hellos.exe
hellos.exe : hellos.obj hellop.obj hello_s.obj
    $(link) $(linkdebug) $(conflags) -out:hellos.exe \
        hellos.obj hello_s.obj hellop.obj \
        rpcrt4.lib $(conlibsmt)
 
# hello server main program
hellos.obj : hellos.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# remote procedures
hellop.obj : hellop.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# hellos stub file
hello_s.obj : hello_s.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# Stubs and header file from the IDL file
hello.h hello_c.c hello_s.c : hello.idl hello.acf
    midl hello.idl
```

 

 




