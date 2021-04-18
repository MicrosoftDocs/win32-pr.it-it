---
description: È possibile creare un'istanza di in C++ tramite l'interfaccia IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Creazione e dichiarazione di un'istanza con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316571"
---
# <a name="creating-and-declaring-an-instance-using-c"></a>Creazione e dichiarazione di un'istanza con C++

È possibile creare un'istanza di in C++ tramite l'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

Gli esempi di codice in questo argomento richiedono la \# compilazione corretta dell'istruzione include seguente.


```C++
#include <wbemidl.h>
```



Nella procedura riportata di seguito viene descritto come creare un'istanza di una classe esistente.

**Per creare un'istanza di una classe esistente**

1.  Recuperare la definizione della classe esistente chiamando il metodo [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

    Nell'esempio di codice seguente viene illustrato come utilizzare i metodi [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) e [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) per ottenere un puntatore all'interfaccia [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) che fornisce l'accesso alla definizione della classe.

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  Creare la nuova istanza di chiamando il metodo [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .

    Nell'esempio di codice seguente viene illustrato come creare una nuova istanza di e quindi rilasciare la classe.

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  Impostare i valori per tutte le proprietà che non ereditano i valori definiti per la classe chiamando il metodo [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    Ogni istanza di una classe eredita tutte le proprietà definite per la classe. Tuttavia, se si sceglie, è possibile specificare valori di proprietà diversi.

    Se la classe esistente ha una proprietà chiave, è necessario impostare la proprietà su **null** o su un valore univoco garantito. Se si imposta la chiave su **null** e la chiave è una stringa, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) o [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) genera internamente e assegna un GUID alla chiave. In questo modo, se si specifica **null** per una proprietà chiave, è possibile creare un'istanza univoca che non sovrascrive alcuna istanza precedente.

    Nell'esempio di codice seguente viene illustrato come impostare il valore della proprietà [**index**](swbemrefreshableitem-index.md) della classe di istanza di esempio.

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  Impostare i valori per i qualificatori rilevanti tramite una chiamata a [**IWbemClassObject:: GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).

    Il metodo [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) restituisce un puntatore a un'interfaccia [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , che usa per accedere ai qualificatori per una classe o un'istanza. È possibile specificare valori diversi per un qualificatore definito per la classe se la versione del qualificatore di classe è **EnableOverride**. Non è possibile modificare o eliminare un qualificatore di classe con la versione di Flavor impostata su **DisableOverride**. Per altre informazioni, vedere [tipi di qualificatori](qualifier-flavors.md).

    Facoltativamente, è anche possibile definire qualificatori aggiuntivi per la classe dell'istanza. È possibile definire qualificatori aggiuntivi per la proprietà dell'istanza o dell'istanza che non devono essere visualizzati nella dichiarazione della classe.

5.  Salvare l'istanza chiamando il metodo [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .

    WMI Salva l'istanza nello spazio dei nomi WMI corrente. Di conseguenza, il percorso completo dell'istanza dipende dallo spazio dei nomi, che in genere è l' \\ impostazione predefinita radice. Per questo esempio di codice, il nome del percorso completo sarà \\ \\ . \\ \\impostazione predefinita radice: example. index = "IX100".

    Nell'esempio di codice seguente viene illustrato come salvare un'istanza di.

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

Il salvataggio dell'istanza in WMI blocca diverse proprietà dell'istanza di.

In particolare, non è possibile eseguire le operazioni seguenti tramite l'API WMI dopo l'esistenza di un'istanza nell'infrastruttura WMI:

-   Modificare la classe padre della classe a cui appartiene l'istanza.
-   Aggiungere o rimuovere proprietà.
-   Modificare i tipi di proprietà.
-   Aggiungere o rimuovere la [**chiave**](standard-qualifiers.md) o i qualificatori **indicizzati** .
-   Aggiungere o rimuovere qualificatori [**singleton**](standard-wmi-qualifiers.md), **dinamici** o [**astratti**](standard-qualifiers.md) .

Nell'esempio di codice seguente vengono combinati gli esempi di codice illustrati nella procedura precedente per illustrare come creare un'istanza di tramite l'API WMI.


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



