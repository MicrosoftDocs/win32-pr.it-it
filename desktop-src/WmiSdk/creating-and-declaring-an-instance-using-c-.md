---
description: È possibile creare un'istanza in C++ tramite l'interfaccia IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Creazione e dichiarazione di un'istanza tramite C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046c8c32944c7b726e09eade2701f8d35c9edb0363635eca2a16f7e3d630799a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568801"
---
# <a name="creating-and-declaring-an-instance-using-c"></a>Creazione e dichiarazione di un'istanza tramite C++

È possibile creare un'istanza in C++ tramite [**l'interfaccia IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

Gli esempi di codice in questo argomento richiedono l'istruzione \# include seguente per la corretta compilazione.


```C++
#include <wbemidl.h>
```



La procedura seguente descrive come creare un'istanza di una classe esistente.

**Per creare un'istanza di una classe esistente**

1.  Recuperare la definizione della classe esistente chiamando i [**metodi IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

    L'esempio di codice seguente illustra come usare i [**metodi GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) e [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) per ottenere un puntatore all'interfaccia [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) che fornisce l'accesso alla definizione della classe.

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

    

2.  Creare la nuova istanza chiamando il [**metodo IWbemClassObject::SpawnInstance.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

    Nell'esempio di codice seguente viene illustrato come creare una nuova istanza di e quindi rilasciare la classe .

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  Impostare i valori per tutte le proprietà che non ereditano i valori definiti per la classe chiamando il metodo [**IWbemClassObject::P ut.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)

    Ogni istanza di una classe eredita tutte le proprietà definite per la classe. È tuttavia possibile specificare valori di proprietà diversi, se si sceglie .

    Se la classe esistente ha una proprietà chiave, è necessario impostare la proprietà su **NULL** o su un valore univoco garantito. Se si imposta la chiave su **NULL** e la chiave è una stringa, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) o [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) genera internamente e assegna un GUID alla chiave. In questo modo, specificando **NULL** per una proprietà chiave è possibile creare un'istanza univoca che non sovrascriverà alcuna istanza precedente.

    Nell'esempio di codice seguente viene illustrato come impostare il [**valore della proprietà Index**](swbemrefreshableitem-index.md) della classe di istanza di esempio.

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

    

4.  Impostare i valori per i qualificatori pertinenti tramite una chiamata a [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).

    Il [**metodo GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) restituisce un puntatore a [**un'interfaccia IWbemQualifierSet,**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) che usa per accedere ai qualificatori per una classe o un'istanza. È possibile specificare valori diversi per un qualificatore definito per la classe se il qualificatore di classe è **EnableOverride**. Non è possibile modificare o eliminare un qualificatore di classe con la proprietà flavor impostata **su DisableOverride**. Per altre informazioni, vedere [Qualifier Flavors](qualifier-flavors.md).

    Come opzione, è anche possibile definire qualificatori aggiuntivi per la classe di istanza. È possibile definire qualificatori aggiuntivi per l'istanza o la proprietà di istanza che non devono essere visualizzati nella dichiarazione di classe.

5.  Salvare l'istanza chiamando il metodo [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

    WMI salva l'istanza nello spazio dei nomi WMI corrente. Di conseguenza, il percorso completo dell'istanza dipende dal nome dello spazio dei nomi, che in genere è l'impostazione predefinita \\ radice. Per questo esempio di codice, il nome completo del percorso sarà \\ \\ . \\ root \\ default:Example.Index="IX100".

    Nell'esempio di codice seguente viene illustrato come salvare un'istanza di .

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

Il salvataggio dell'istanza in WMI blocca diverse proprietà dell'istanza.

In particolare, non è possibile eseguire una delle operazioni seguenti tramite l'API WMI dopo l'esistenza di un'istanza all'interno dell'infrastruttura WMI:

-   Modificare la classe padre della classe a cui appartiene l'istanza.
-   Aggiungere o rimuovere proprietà.
-   Modificare i tipi di proprietà.
-   Aggiungere o rimuovere [**qualificatori chiave**](standard-qualifiers.md) **o** indicizzati.
-   Aggiungere o rimuovere [**qualificatori Singleton,**](standard-wmi-qualifiers.md) **Dynamic** [**o Abstract.**](standard-qualifiers.md)

L'esempio di codice seguente combina gli esempi di codice illustrati nella procedura precedente per illustrare come creare un'istanza usando l'API WMI.


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



 

 



