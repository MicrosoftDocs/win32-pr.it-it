---
description: La creazione di una classe derivata in WMI è molto simile alla creazione di una classe di base. Come per una classe base, è innanzitutto necessario definire la classe derivata e quindi registrare la classe derivata con WMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Creazione di una classe derivata WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310400"
---
# <a name="creating-a-wmi-derived-class"></a>Creazione di una classe derivata WMI

La creazione di una classe derivata in WMI è molto simile alla creazione di una classe di base. Come per una classe base, è innanzitutto necessario definire la classe derivata e quindi registrare la classe derivata con WMI. La differenza principale consiste nel fatto che è necessario innanzitutto individuare la classe padre da cui si desidera eseguire la derivazione. Per ulteriori informazioni, vedere [scrittura di un provider di classi](writing-a-class-provider.md) e [scrittura di un provider di istanze](writing-an-instance-provider.md).

Il metodo consigliato per creare classi per un provider è nei file Managed Object Format (MOF). Diverse classi derivate che sono correlate tra loro devono essere raggruppate in un file MOF, insieme a tutte le classi di base da cui derivano le proprietà o i metodi. Se si posiziona ogni classe in un file MOF separato, è necessario compilare ogni file prima che il provider possa funzionare correttamente.

Dopo aver creato la classe, è necessario eliminare tutte le istanze della classe prima di poter eseguire una delle attività seguenti sulla classe derivata:

-   Modificare la classe padre della classe derivata.
-   Aggiungere o rimuovere proprietà.
-   Modificare i tipi di proprietà.
-   Aggiungere o rimuovere la [**chiave**](key-qualifier.md) o i qualificatori **indicizzati** .
-   Aggiungere o rimuovere qualificatori [**singleton**](standard-wmi-qualifiers.md), **dinamici** o [**astratti**](standard-qualifiers.md) .

> [!Note]  
> Per aggiungere, rimuovere o modificare una proprietà o un qualificatore, chiamare [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) o [**SWbemObject. \_ put**](swbemobject-put-.md) e impostare il parametro del flag su "Force Mode". Il qualificatore [**astratto**](standard-qualifiers.md) può essere utilizzato solo se la classe padre è astratta.

 

Quando si dichiara la classe derivata, osservare le regole e le restrizioni seguenti:

-   La classe padre della classe derivata deve esistere già.

    La dichiarazione della classe padre può comparire nello stesso file MOF della classe derivata o in un file diverso. Se la classe padre è sconosciuta, il compilatore genera un errore di run-time.

-   Una classe derivata può avere una sola classe padre.

    WMI non supporta l'ereditarietà multipla. Tuttavia, una classe padre può avere molte classi derivate.

-   È possibile definire gli indici per le classi derivate, ma WMI non utilizza questi indici.

    Pertanto, la specifica di un indice in una classe derivata non migliora le prestazioni delle query per le istanze della classe derivata. È possibile migliorare le prestazioni di una query su una classe derivata specificando le proprietà indicizzate per la classe padre della classe derivata.

-   Le definizioni delle classi derivate possono essere più complesse e possono includere caratteristiche quali alias, qualificatori e versioni di qualificatori.

    Per ulteriori informazioni, vedere [creazione di un alias](creating-an-alias.md) e [aggiunta di un qualificatore](adding-a-qualifier.md).

-   Se si desidera modificare un qualificatore, modificare il valore predefinito di una proprietà della classe base o digitare più fortemente un riferimento o una proprietà dell'oggetto incorporato di una classe di base, è necessario dichiarare di nuovo l'intera classe di base.
-   Il numero massimo di proprietà che è possibile definire in una classe WMI è 1024.

> [!Note]  
> Non è possibile modificare le classi durante l'esecuzione dei provider. È necessario arrestare l'attività, modificare la classe e quindi riavviare il servizio di gestione Windows. Il rilevamento di una modifica di classe non è attualmente possibile.

 

Come per la classe di base, l'uso più comune di questa tecnica è costituito dalle applicazioni client. Tuttavia, un provider può anche creare una classe derivata. Per ulteriori informazioni, vedere [creazione di una classe di base](creating-a-base-class.md) e [scrittura di un provider di classi](writing-a-class-provider.md).

Nell'esempio di codice in questo argomento è richiesta la \# compilazione corretta dell'istruzione include seguente.


```C++
#include <wbemidl.h>
```



Nella procedura riportata di seguito viene descritto come creare una classe derivata mediante C++.

**Per creare una classe derivata con C++**

1.  Individuare la classe di base con una chiamata a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

    Nell'esempio di codice riportato di seguito viene illustrato come individuare la classe base di esempio.

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  Creare un oggetto derivato dalla classe base con una chiamata a [**IWbemClassObject:: SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).

    Nell'esempio di codice seguente viene illustrato come creare un oggetto di classe derivata.

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  Definire un nome per la classe impostando la proprietà di sistema della **\_ \_ classe** con una chiamata al metodo [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    Nell'esempio di codice seguente viene illustrato come assegnare un nome alla classe derivata.

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  Creare proprietà aggiuntive con [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Nell'esempio di codice seguente viene illustrato come creare proprietà aggiuntive.

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  Salvare la nuova classe chiamando [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Nell'esempio di codice seguente viene illustrato come salvare la nuova classe derivata.

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

Nell'esempio di codice seguente vengono combinati gli esempi di codice illustrati nella procedura precedente per descrivere come creare una classe derivata utilizzando l'API WMI.


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



Nella procedura riportata di seguito viene descritto come definire una classe derivata utilizzando il codice MOF.

**Per definire una classe derivata utilizzando il codice MOF**

1.  Definire la classe derivata con la parola chiave **Class** , seguita dal nome della classe derivata e il nome della classe padre separata da due punti.

    Nell'esempio di codice seguente viene descritta un'implementazione di una classe derivata.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  Al termine, compilare il codice MOF con il compilatore MOF.

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una classe](creating-a-class.md)
</dt> </dl>

 

 



