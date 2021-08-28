---
description: Il percorso di un oggetto istanza descrive la posizione di un'istanza di una determinata classe all'interno di uno spazio dei nomi specifico.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Descrizione del percorso di un oggetto istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a152d68390c899709cfe6041bfa2880482a0d4498dc371aafd4426aef8f14489
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412061"
---
# <a name="describing-an-instance-object-path"></a>Descrizione del percorso di un oggetto istanza

Il percorso di un oggetto istanza descrive la posizione di un'istanza di una determinata classe all'interno di uno spazio dei nomi specifico.

È possibile avere diversi tipi di percorsi di oggetti istanza:

-   Full

    Un percorso completo dell'oggetto istanza aggiunge il nome e il valore della proprietà chiave per la classe a un percorso completo dell'oggetto classe.

    Nell'esempio seguente viene illustrata la definizione del percorso completo dell'oggetto istanza.

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   Relativo

    Un percorso di oggetto relativo fa riferimento a un'istanza che si trova nello spazio dei nomi corrente nel server corrente. Il percorso relativo è costituito dal nome della classe seguito dai nomi e dai valori delle proprietà chiave di questa istanza.

    Nell'esempio seguente viene illustrata la definizione del percorso dell'oggetto istanza relativo.

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   Relativo con una singola chiave

    Per le classi con una sola proprietà designata come chiave, è possibile omettere il nome della proprietà chiave.

    Nell'esempio seguente viene illustrata la definizione del percorso dell'oggetto istanza relativo con una singola chiave.

    ``` syntax
    MyClass="e:"
    ```

-   Relativo con più chiavi

    Usare una virgola per distinguere tra le chiavi di un'istanza con più chiavi.

    Nell'esempio seguente vengono illustrate le definizioni del percorso dell'oggetto istanza relativo con più chiavi.

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   Relativo per una classe singleton

    Il percorso dell'oggetto relativo per una classe singleton è costituito dal nome della classe seguito dalla notazione "=@".

    Nell'esempio seguente viene illustrata la definizione del percorso dell'oggetto istanza relativo per una classe singleton.

    ``` syntax
    MySingletonClass=@
    ```

Nella procedura seguente viene descritto come recuperare un'istanza della classe .

**Per recuperare un'istanza della classe**

1.  Inizializzare una stringa che contiene il percorso dell'oggetto con una chiamata alla [**funzione SysAllocString.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
2.  Inizializzare un oggetto che riceverà l'istanza di .
3.  Recuperare l'oggetto con una chiamata a [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

    Per usare [**GetObjectAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)è necessario implementare [**l'interfaccia IWbemSink.**](swbemsink.md)

L'istruzione include seguente è necessaria per la corretta compilazione del \# codice elencato più avanti in questo argomento.


```C++
#include <wbemidl.h>
```



Nell'esempio di codice seguente viene descritto come recuperare un'istanza della classe utilizzando un percorso di oggetto.


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



Per le istanze di classi che specificano più proprietà come chiave, WMI non richiede un ordinamento specifico delle proprietà chiave nei percorsi degli oggetti. È necessario specificare solo il valore di ognuna delle proprietà nel percorso dell'oggetto.

Nell'esempio di codice seguente vengono descritte due descrizioni chiave equivalenti.

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
