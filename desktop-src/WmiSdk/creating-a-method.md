---
description: Per creare un metodo WMI, definire i parametri di input e output per il metodo.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Creazione di un metodo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2489a5dd4e97ed6c8d26eeb292c45fa66901cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233469"
---
# <a name="creating-a-wmi-method"></a>Creazione di un metodo WMI

Per creare un metodo WMI, definire i parametri di input e output per il metodo. I parametri di input e output sono rappresentati da uno speciale [**\_ \_ parametro**](--parameters.md)della classe di sistema WMI. Per ulteriori informazioni, vedere la pagina relativa alla [chiamata a un metodo](calling-a-method.md) e alla [scrittura di un provider di metodi](writing-a-method-provider.md).

Le sezioni seguenti sono illustrate in questo argomento:

-   [Creazione di un metodo di classe WMI in MOF](#creating-a-wmi-class-method-in-mof)
-   [Creazione di un metodo di classe WMI in C++](#creating-a-wmi-class-method-in-c)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a>Creazione di un metodo di classe WMI in MOF

In WMI i metodi del provider sono in genere azioni distinte correlate all'oggetto rappresentato dalla classe. Anziché modificare il valore di una proprietà per eseguire un'azione, è necessario creare un metodo. Ad esempio, è possibile abilitare o disabilitare un Network Information Center (NIC) rappresentato da [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) usando i metodi [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) e [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) . Anche se queste azioni possono essere rappresentate come proprietà di lettura/scrittura, la progettazione consigliata consiste nel creare un metodo. In alternativa, se si desidera rendere visibile uno stato o un valore per la classe, l'approccio consigliato consiste nel creare una proprietà di lettura/scrittura anziché un metodo. In **Win32 \_ NetworkAdapter** la proprietà **NetEnabled** rende visibile lo stato dell'adapter, ma le modifiche tra gli Stati vengono eseguite dai metodi **Enable** o **Disable** .

Le dichiarazioni di classe possono includere la dichiarazione di uno o più metodi. È possibile scegliere di ereditare i metodi di una classe padre o implementarne uno personalizzato. Se si sceglie di implementare metodi personalizzati, è necessario dichiarare il metodo e contrassegnare il metodo con tag di qualificatore specifici.

Nella procedura riportata di seguito viene descritto come dichiarare un metodo in una classe che non eredita da una classe base.

**Per dichiarare un metodo**

1.  Definire il nome del metodo tra le parentesi graffe di una dichiarazione di classe, seguito da tutti i qualificatori.

    Nell'esempio di codice seguente viene illustrata la sintassi di un metodo.

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  Al termine, inserire il codice di Managed Object Format (MOF) nel repository WMI con una chiamata al compilatore MOF.

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

Nell'elenco seguente vengono definiti gli elementi della dichiarazione di metodo.

<dl> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)
</dt> <dd>

Collega un provider specifico alla descrizione della classe. Il valore del qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) è il nome del provider, che indica a WMI dove risiede il codice che supporta il metodo. Un provider deve inoltre contrassegnare con il qualificatore **dinamico** qualsiasi classe che dispone di istanze dinamiche. Al contrario, non usare il qualificatore **dinamico** per contrassegnare una classe che contiene un'istanza statica con i metodi **implementati** .

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementato**
</dt> <dd>

Dichiara che viene implementato un metodo, anziché ereditare l'implementazione del metodo dalla classe padre. Per impostazione predefinita, WMI propaga l'implementazione della classe padre a una classe derivata a meno che la classe derivata non fornisca un'implementazione. L'omissione del qualificatore **implementato** indica che il metodo non dispone di alcuna implementazione in tale classe. Se si dichiara di nuovo un metodo senza il qualificatore **implementato** , WMI presuppone comunque che non si implementi il metodo e richiama l'implementazione del metodo della classe padre quando viene chiamato. Di conseguenza, la ridichiarazione di un metodo in una classe derivata senza l'associazione del qualificatore **implementato** risulta utile solo quando si aggiunge o rimuove un qualificatore a o dal metodo.

</dd> <dt>

<span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType
</dt> <dd>

Descrive il valore restituito dal metodo. Il valore restituito per un metodo deve essere un oggetto booleano, numerico, **char**, **String**, [DateTime](datetime.md)o schema. È anche possibile dichiarare il tipo restituito come [void](void.md), a indicare che il metodo non restituisce alcun valore. Tuttavia, non è possibile dichiarare una matrice come tipo di valore restituito.

</dd> <dt>

<span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName
</dt> <dd>

Definisce il nome del metodo. Ogni metodo deve avere un nome univoco. WMI non consente l'esistenza di due metodi con lo stesso nome e firme diverse in una classe o in una gerarchia di classi. Di conseguenza, non è possibile eseguire l'overload di un metodo.

</dd> <dt>

<span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection
</dt> <dd>

Contiene qualificatori che descrivono se un parametro è un parametro di input, un parametro di output o entrambi. Non usare lo stesso nome di parametro più di una volta come parametro di input o più di una volta come parametro di output. Se viene visualizzato lo stesso nome di parametro con i qualificatori [**in**](standard-qualifiers.md) e **out** , la funzionalità è concettualmente analoga all'uso di qualificatori **in**, **out** per un singolo parametro. Tuttavia, quando si usano dichiarazioni separate, i parametri di input e di output devono essere esattamente gli stessi in tutti gli altri aspetti, inclusi il numero e il tipo di qualificatori [**ID**](standard-wmi-qualifiers.md) , e il qualificatore deve essere lo stesso e dichiarato in modo esplicito per entrambi. Si consiglia vivamente di utilizzare i qualificatori **in**, **out** all'interno di una singola dichiarazione di parametro.

</dd> <dt>

<span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**
</dt> <dd>

Contiene il qualificatore [**ID**](standard-wmi-qualifiers.md) che identifica in modo univoco la posizione di ogni parametro all'interno della sequenza di parametri nel metodo. Per impostazione predefinita, il compilatore MOF contrassegna automaticamente i parametri con un qualificatore **ID** . Il compilatore contrassegna il primo parametro con un valore pari a 0 (zero), il secondo parametro un valore 1 (uno) e così via. Se necessario, è possibile dichiarare in modo esplicito la sequenza di ID nel codice MOF.

</dd> <dt>

<span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType
</dt> <dd>

Descrive il tipo di dati che il metodo può accettare. È possibile definire un tipo di parametro come qualsiasi valore di dati MOF, tra cui una matrice, un oggetto dello schema o un riferimento. Quando si usa una matrice come parametro, usare la matrice come Unbound o con dimensioni esplicite.

</dd> <dt>

<span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName
</dt> <dd>

Contiene il nome del parametro. A questo punto è anche possibile scegliere di definire il valore predefinito del parametro. I parametri privi di valori iniziali rimangono non assegnati.

</dd> </dl>

Nell'esempio di codice seguente vengono descritti i qualificatori e l'elenco dei parametri.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare una matrice in un parametro MOF.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

Nell'esempio di codice riportato di seguito viene descritto l'utilizzo di un oggetto dello schema come parametro e valore restituito.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

Nell'esempio di codice seguente viene descritto come includere due riferimenti: uno a un'istanza della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e l'altro a un'istanza di un tipo di oggetto sconosciuto.

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a>Creazione di un metodo di classe WMI in C++

Nella procedura seguente viene descritto come creare un metodo di classe WMI a livello di programmazione.

**Per creare un metodo di classe WMI a livello di codice**

1.  Creare la classe a cui apparterrà il metodo.

    Prima di creare il metodo, è necessario innanzitutto disporre di una classe in cui inserire il metodo.

2.  Recuperare due classi figlio della classe di sistema [**\_ \_ Parameters**](--parameters.md) usando [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

    Usare la prima classe figlio per descrivere i parametri in e la seconda per descrivere i parametri out. Se necessario, è possibile eseguire un singolo recupero seguito da una chiamata al metodo [**IWbemClassObject:: Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) .

3.  Scrivere i parametri in nella prima classe e i parametri out per la seconda classe, usando una o più chiamate a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Quando si descrivono i parametri per un metodo, osservare le regole e le restrizioni seguenti:

    -   Trattare i \[ parametri in, out \] come voci separate, uno nell'oggetto che contiene i parametri in e uno nell'oggetto che contiene i parametri out.
    -   Ad eccezione di, i qualificatori \[ \] rimanenti devono essere esattamente gli stessi.
    -   Specificare i qualificatori [**ID**](standard-wmi-qualifiers.md) , a partire da 0 (zero), uno per ogni parametro.

        L'ordine dei parametri di input o output viene stabilito dal valore del qualificatore [**ID**](standard-wmi-qualifiers.md) per ogni parametro. Tutti gli argomenti di input devono precedere qualsiasi argomento di output. La modifica dell'ordine dei parametri di input e output del metodo durante l'aggiornamento di un provider di metodi esistente può causare errori nelle applicazioni che chiamano il metodo. Aggiungere nuovi parametri di input alla fine dei parametri esistenti anziché inserirli nella sequenza già stabilita.

        Assicurarsi di non lasciare vuoti nella sequenza di qualificatore [**ID**](standard-wmi-qualifiers.md) .

    -   Inserire il valore restituito nella classe out-parameters come proprietà denominata **returnValue**.

        Identifica la proprietà come valore restituito del metodo. Il tipo CIM di questa proprietà è il tipo restituito del metodo. Se il metodo ha un tipo restituito void, non deve essere presente alcuna proprietà **returnValue** . Inoltre, la proprietà **returnValue** non può avere un qualificatore [**ID**](standard-wmi-qualifiers.md) come gli argomenti del metodo. L'assegnazione di un qualificatore **ID** alla proprietà **returnValue** genera un errore WMI.

    -   Esprimere tutti i valori di parametro predefiniti per la proprietà nella classe.

4.  Inserire entrambi gli oggetti [**\_ \_ Parameters**](--parameters.md) nella classe padre con una chiamata a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

    Una singola chiamata a [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) può inserire entrambi gli oggetti [**\_ \_ Parameters**](--parameters.md) nella classe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una classe](creating-a-class.md)
</dt> </dl>

 

 
