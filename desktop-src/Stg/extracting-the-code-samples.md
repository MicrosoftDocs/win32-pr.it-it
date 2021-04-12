---
title: Estrazione degli esempi di codice
description: Sebbene gli esempi di codice siano divisi in una serie di lezioni di esercitazione, è possibile estrarre facilmente i raggruppamenti di esempio appropriati dalla raccolta.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395718"
---
# <a name="extracting-the-code-samples"></a>Estrazione degli esempi di codice

Sebbene gli esempi di codice siano divisi in una serie di lezioni di esercitazione, è possibile estrarre facilmente i raggruppamenti di esempio appropriati dalla raccolta. La maggior parte delle singole directory di esempio è concepita per funzionare insieme ad almeno un'altra directory di esempio. Gli esempi correlati ai componenti sono costituiti da una coppia client e server, con il server che richiede l'uso dell'utilità di registrazione di esempio. Ecco un riepilogo dei raggruppamenti di esempio e come estrarre ogni gruppo come unità compilabile. Per ogni raggruppamento di esempio, copiare il contenuto delle directory visualizzate. La \[ \] directory di destinazione padre visualizzata non richiede alcun contenuto dal branch degli esempi. Tuttavia, i menu della guida negli esempi in esecuzione presuppongono che l'esercitazione appropriata. I file della Guida HTM si trovano in questa \[ directory di destinazione padre \] .

Per l'applicazione Win32 READTUT:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

Per l'applicazione Win32 EXE Skeleton:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

Per lo scheletro della DLL Win32:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

Per gli esempi di oggetti COM di base:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

Per gli esempi client/server del componente DLL di base in-process:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

Per gli esempi client/server del componente con licenza:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

Per gli esempi di marshalling standard:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

Per gli esempi client/server locali out-of-process:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

Per gli esempi client/server del modello di Apartment:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

Per gli esempi client/server DCOM (Distributed COM):

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

Per gli esempi client/server di threading gratuiti:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

Per gli esempi client/server di oggetti COM collegabili:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

Per gli esempi client/server di archiviazione strutturata:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

Per gli esempi client/server di oggetti permanenti:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

Per gli esempi client/server di sicurezza DCOM:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




