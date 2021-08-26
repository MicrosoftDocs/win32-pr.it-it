---
title: Estrazione degli esempi di codice
description: Anche se gli esempi di codice sono suddivisi in una serie di lezioni di esercitazione, i raggruppamenti di esempio appropriati possono essere facilmente estratti dalla raccolta.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67093f4cfbbfab2a3c1681462627f02b504124ed15d1483b9f9d91ec5551d0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034951"
---
# <a name="extracting-the-code-samples"></a>Estrazione degli esempi di codice

Anche se gli esempi di codice sono suddivisi in una serie di lezioni di esercitazione, i raggruppamenti di esempio appropriati possono essere facilmente estratti dalla raccolta. La maggior parte delle singole directory di esempio è destinata a funzionare in combinazione con almeno un'altra directory di esempio. Gli esempi relativi ai componenti sono costituiti da una coppia client e server, con il server che richiede l'uso dell'utilità di esempio REGISTER. Ecco un riepilogo dei raggruppamenti di esempio e come estrarre ogni gruppo come unità compilabile. Per ogni raggruppamento di esempio, copiare il contenuto delle directory visualizzate. La \[ directory di \] destinazione padre visualizzata non richiede contenuto dal ramo degli esempi. Tuttavia, i menu della Guida negli esempi in esecuzione presuppongono che l'esercitazione appropriata .HTM file della Guida si trovi in questa directory di \[ destinazione \] padre.

Per l'applicazione READTUT Win32:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

Per lo scheletro dell'applicazione EXE Win32:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

Per lo scheletro di DLL Win32:

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

Per gli esempi client/server del componente DLL in-process di base:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

Per gli esempi client/server del componente concesso in licenza:

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

Per gli esempi di client/server locali out-of-process:

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

Per gli esempi client/server del modello di apartment:

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

Per gli esempi di client/server DCOM (Distributed COM):

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

Per gli esempi di client/server per il threading libero:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

Per gli esempi di client/server dell'oggetto COM collegabile:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

Per gli esempi di client/server di archiviazione strutturata:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

Per gli esempi di client/server dell'oggetto persistente:

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

 

 




