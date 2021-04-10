---
description: Il metodo consigliato per creare una nuova classe di base WMI per un provider WMI è in un file di Managed Object Format (MOF).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Creazione di una classe di base WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968369"
---
# <a name="creating-a-wmi-base-class"></a>Creazione di una classe di base WMI

Il metodo consigliato per creare una nuova classe di base WMI per un provider WMI è in un file di Managed Object Format (MOF). È inoltre possibile creare una classe di base utilizzando l' [API com per WMI](com-api-for-wmi.md). Sebbene sia possibile creare una classe base o derivata nello script, senza che un provider fornisca dati alla classe e alle relative sottoclassi, la classe non è utile.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Creazione di una classe di base utilizzando MOF](#creating-a-base-class-using-mof)
-   [Creazione di una classe base con C++](#creating-a-base-class-with-c)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-base-class-using-mof"></a>Creazione di una classe di base utilizzando MOF

Le classi WMI si basano in genere sull'ereditarietà. Prima di creare una classe di base, controllare le classi Common Information Model (CIM) disponibili da Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).

Se molte classi derivate utilizzeranno le stesse proprietà, inserire queste proprietà e questi metodi nella classe di base. Il numero massimo di proprietà che è possibile definire in una classe WMI è 1024.

Quando si crea una classe base, osservare l'elenco seguente di linee guida per i nomi delle classi:

-   Usare lettere maiuscole e minuscole.
-   Inizia un nome di classe con una lettera.
-   Non usare un carattere di sottolineatura iniziali o finali.
-   Definire tutti i caratteri rimanenti come lettere, cifre o caratteri di sottolineatura.
-   Usare una convenzione di denominazione coerente.

    Sebbene non sia necessario, una convenzione di denominazione corretta per una classe è due componenti Uniti da un carattere di sottolineatura. Quando possibile, un nome di fornitore deve costituire la prima metà del nome e un nome di classe descrittivo deve essere la seconda parte.

> [!Note]  
> Non è possibile modificare le classi durante l'esecuzione dei provider. È necessario arrestare l'attività, modificare la classe e quindi riavviare il servizio di gestione Windows. Il rilevamento di una modifica di classe non è attualmente possibile.

 

In MOF creare una classe base chiamandola con la parola chiave **Class** , ma non indicando una classe padre.

**Per creare una classe di base utilizzando il codice MOF**

1.  Usare la parola chiave **Class** con il nome della nuova classe, seguita da una coppia di parentesi graffe e da un punto e virgola. Aggiungere le proprietà e i metodi per la classe tra parentesi graffe. Viene fornito l'esempio di codice seguente.

    Nell'esempio di codice riportato di seguito viene illustrato come definire una classe di base.

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    Nell'esempio di codice seguente viene illustrata una definizione non corretta di una classe di base.

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  Aggiungere i [*qualificatori*](gloss-q.md) di classe prima della parola chiave Class per modificare la modalità di utilizzo della classe. Posizionare i qualificatori tra parentesi quadre. Per ulteriori informazioni sui qualificatori per la modifica delle classi, vedere [qualificatori WMI](wmi-qualifiers.md). Utilizzare il qualificatore **astratto** per indicare che non è possibile creare direttamente un'istanza di questa classe. Le classi astratte vengono spesso usate per definire le proprietà o i metodi che verranno usati da diverse classi derivate. Per ulteriori informazioni, vedere [creazione di una classe derivata](creating-a-derived-class.md).

    Nell'esempio di codice seguente viene definita la classe come astratta e viene definito il provider che fornirà i dati. La versione del qualificatore **ToClass** indica che le informazioni [*nel qualificatore*](gloss-f.md) del **provider** sono ereditate dalle classi derivate.

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  Aggiungere le proprietà e i metodi della classe all'interno di parentesi quadre prima del nome della proprietà o del metodo. Per ulteriori informazioni, vedere [aggiunta di una proprietà](adding-a-property.md) e [creazione di un metodo](creating-a-method.md). È possibile modificare queste proprietà e metodi usando i qualificatori MOF. Per ulteriori informazioni, vedere [aggiunta di un qualificatore](adding-a-qualifier.md).

    Nell'esempio di codice riportato di seguito viene illustrato come modificare proprietà e metodi con qualificatori MOF.

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  Salvare il file MOF con estensione MOF.
5.  Registrare la classe con WMI eseguendo [**Mofcomp.exe**](mofcomp.md) sul file.

    **mofcomp.exe** *newmof. mof*

    Se non si usa l'opzione **-N** o lo \# [**spazio dei nomi pragma**](pragma-namespace.md) del comando per il preprocessore per specificare uno spazio dei nomi, le classi MOF compilate verranno archiviate nello \\ spazio dei nomi predefinito radice nel repository. Per ulteriori informazioni, vedere [**mofcomp**](mofcomp.md).

Nell'esempio di codice seguente vengono combinati gli esempi di codice MOF descritti nella procedura precedente e viene illustrato come creare una classe di base nello \\ spazio dei nomi CIMV2 radice utilizzando MOF.

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

Per ulteriori informazioni, vedere [creazione di una classe derivata](creating-a-derived-class.md) per un esempio di classe dinamica derivata da questa classe di base.

## <a name="creating-a-base-class-with-c"></a>Creazione di una classe base con C++

La creazione di una classe di base tramite l'API WMI è principalmente una serie di comandi put che definiscono la classe e registrano la classe con WMI. Lo scopo principale di questa API è quello di consentire alle applicazioni client di creare classi di base. Tuttavia, è anche possibile fare in modo che un provider usi questa API per creare una classe di base. Se, ad esempio, si ritiene che il codice MOF per il provider non verrà installato correttamente, è possibile indicare al provider di creare automaticamente le classi corrette nel repository WMI. Per ulteriori informazioni sui provider, vedere [scrittura di un provider di classi](writing-a-class-provider.md).

> [!Note]  
> Non è possibile modificare le classi durante l'esecuzione dei provider. È necessario arrestare l'attività, modificare la classe e quindi riavviare il servizio di gestione Windows. Il rilevamento di una modifica di classe non è attualmente possibile.

 

Il codice richiede che il riferimento seguente venga compilato correttamente.


```C++
#include <wbemidl.h>
```



È possibile creare una nuova classe di base a livello di codice usando l' [API com per WMI](com-api-for-wmi.md).

**Per creare una nuova classe base con l'API WMI**

1.  Recuperare una definizione per la nuova classe chiamando il metodo [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) con il parametro *strObjectPath* impostato su un valore **null** .

    Nell'esempio di codice seguente viene illustrato come recuperare una definizione per una nuova classe.

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  Definire un nome per la classe impostando la proprietà di sistema della **\_ \_ classe** con una chiamata al metodo [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    Nell'esempio di codice seguente viene illustrato come assegnare un nome alla classe impostando la proprietà di sistema della **\_ \_ classe** .

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  Creare la proprietà o le proprietà chiave chiamando [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Nell'esempio di codice riportato di seguito viene illustrato come creare la proprietà [**index**](swbemrefreshableitem-index.md) , etichettata come proprietà chiave nel passaggio 4.

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  Alleghi il qualificatore standard della [**chiave**](standard-qualifiers.md) alla proprietà chiave chiamando prima il metodo [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) e quindi il metodo [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .

    Nell'esempio di codice seguente viene illustrato come aggiungere il qualificatore standard della [**chiave**](standard-qualifiers.md) alla proprietà della chiave.

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  Creare altre proprietà della classe con [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Nell'esempio di codice seguente viene descritto come creare proprietà aggiuntive.

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  Registrare la nuova classe chiamando [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Poiché non è possibile definire chiavi e indici dopo la registrazione di una nuova classe, verificare di aver definito tutte le proprietà prima di chiamare [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Nell'esempio di codice seguente viene illustrato come registrare una nuova classe.

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

Nell'esempio di codice seguente vengono combinati gli esempi di codice illustrati nella procedura precedente e viene illustrato come creare una classe di base utilizzando l'API WMI.


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una classe](creating-a-class.md)
</dt> </dl>

 

 



