---
description: La creazione di una classe derivata in WMI è molto simile alla creazione di una classe di base. Come per una classe di base, è necessario prima definire la classe derivata e quindi registrare la classe derivata con WMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Creazione di una classe derivata WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cddc2b381346b2765e836bb3606cc06845280c41a7505b872098f383ac0409c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374871"
---
# <a name="creating-a-wmi-derived-class"></a>Creazione di una classe derivata WMI

La creazione di una classe derivata in WMI è molto simile alla creazione di una classe di base. Come per una classe di base, è necessario prima definire la classe derivata e quindi registrare la classe derivata con WMI. La differenza principale è che è prima necessario individuare la classe padre da cui si vuole derivare. Per altre informazioni, vedere [Scrittura di un provider di classi e](writing-a-class-provider.md) Scrittura di un provider di [istanze.](writing-an-instance-provider.md)

Il modo consigliato per creare classi per un provider è nei file Managed Object Format (MOF). Diverse classi derivate correlate tra loro devono essere raggruppate in un file MOF, insieme a tutte le classi di base da cui derivano proprietà o metodi. Se si posiziona ogni classe in un file MOF separato, ogni file deve essere compilato prima che il provider possa funzionare correttamente.

Dopo aver creato la classe, è necessario eliminare tutte le istanze della classe prima di poter eseguire una delle attività seguenti nella classe derivata:

-   Modificare la classe padre della classe derivata.
-   Aggiungere o rimuovere proprietà.
-   Modificare i tipi di proprietà.
-   Aggiungere o rimuovere [**qualificatori**](key-qualifier.md) chiave **o** indicizzati.
-   Aggiungere o rimuovere [**qualificatori Singleton,**](standard-wmi-qualifiers.md) **Dynamic** [**o Abstract.**](standard-qualifiers.md)

> [!Note]  
> Per aggiungere, rimuovere o modificare una proprietà o un qualificatore, chiamare [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) o [**SWbemObject.Put \_**](swbemobject-put-.md) e impostare il parametro flag su "force mode". Il [**qualificatore Abstract**](standard-qualifiers.md) può essere usato solo se la classe padre è astratta.

 

Quando si dichiara la classe derivata, osservare le regole e le restrizioni seguenti:

-   La classe padre della classe derivata deve esistere già.

    La dichiarazione della classe padre può essere visualizzata nello stesso file MOF della classe derivata o in un file diverso. Se la classe padre è sconosciuta, il compilatore genera un errore di run-time.

-   Una classe derivata può avere una sola classe padre.

    WMI non supporta l'ereditarietà multipla. Tuttavia, una classe padre può avere molte classi derivate.

-   È possibile definire indici per le classi derivate, ma WMI non usa questi indici.

    Pertanto, la specifica di un indice in una classe derivata non migliora le prestazioni delle query per le istanze della classe derivata. È possibile migliorare le prestazioni di una query in una classe derivata specificando proprietà indicizzate per la classe padre della classe derivata.

-   Le definizioni delle classi derivate possono essere più complesse e possono includere funzionalità quali alias, qualificatori e tipi di qualificatori.

    Per altre informazioni, vedere [Creazione di un alias e](creating-an-alias.md) Aggiunta di un [qualificatore.](adding-a-qualifier.md)

-   Se si vuole modificare un qualificatore, modificare il valore predefinito di una proprietà della classe base o digitare più fortemente una proprietà di riferimento o oggetto incorporato di una classe di base, è necessario dichiarare nuovamente l'intera classe di base.
-   Il numero massimo di proprietà che è possibile definire in una classe WMI è 1024.

> [!Note]  
> Le classi non possono essere modificate durante l'esecuzione dei provider. È necessario arrestare l'attività, modificare la classe e quindi riavviare il Windows Management. Il rilevamento di una modifica della classe non è attualmente possibile.

 

Come per la classe di base, l'uso più comune di questa tecnica sarà da parte delle applicazioni client. Tuttavia, un provider può anche creare una classe derivata. Per altre informazioni, vedere [Creazione di una classe di base e](creating-a-base-class.md) Scrittura di un provider di [classi.](writing-a-class-provider.md)

L'esempio di codice in questo argomento richiede la corretta \# compilazione dell'istruzione include seguente.


```C++
#include <wbemidl.h>
```



La procedura seguente descrive come creare una classe derivata usando C++.

**Per creare una classe derivata usando C++**

1.  Individuare la classe di base con una chiamata a [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

    Nell'esempio di codice seguente viene illustrato come individuare la classe di base Example.

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

    

2.  Creare un oggetto derivato dalla classe di base con una chiamata a [**IWbemClassObject::SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).

    Nell'esempio di codice seguente viene illustrato come creare un oggetto classe derivata.

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  Definire un nome per la classe impostando la proprietà di sistema **\_ \_ CLASS** con una chiamata al metodo [**IWbemClassObject::P ut.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)

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

    

4.  Creare proprietà aggiuntive con [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Nell'esempio di codice seguente viene illustrato come creare proprietà aggiuntive.

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  Salvare la nuova classe chiamando [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Nell'esempio di codice seguente viene illustrato come salvare la nuova classe derivata.

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

Nell'esempio di codice seguente vengono combinati gli esempi di codice illustrati nella procedura precedente per descrivere come creare una classe derivata usando l'API WMI.


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



La procedura seguente descrive come definire una classe derivata usando il codice MOF.

**Per definire una classe derivata usando il codice MOF**

1.  Definire la classe derivata con la parola chiave **Class,** seguita dal nome della classe derivata e dal nome della classe padre separati da due punti.

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

    Per altre informazioni, vedere [Compilazione di file MOF.](compiling-mof-files.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una classe](creating-a-class.md)
</dt> </dl>

 

 



