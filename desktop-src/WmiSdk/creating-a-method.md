---
description: Per creare un metodo WMI, definire i parametri di input e output per il metodo.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Creazione di un metodo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689f69518f440e7c1983a92fbf86877c5c6dd2149ce2b31b8459aa08b9e94c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612531"
---
# <a name="creating-a-wmi-method"></a>Creazione di un metodo WMI

Per creare un metodo WMI, definire i parametri di input e output per il metodo. I parametri di input e output sono rappresentati da una classe di sistema WMI [**\_ \_ speciale PARAMETERS.**](--parameters.md) Per altre informazioni, vedere [Chiamata di un metodo e](calling-a-method.md) Scrittura di un provider di [metodi](writing-a-method-provider.md).

In questo argomento vengono illustrate le sezioni seguenti:

-   [Creazione di un metodo della classe WMI in MOF](#creating-a-wmi-class-method-in-mof)
-   [Creazione di un metodo della classe WMI in C++](#creating-a-wmi-class-method-in-c)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a>Creazione di un metodo della classe WMI in MOF

In WMI, i metodi del provider sono in genere azioni distinte correlate all'oggetto rappresentato dalla classe . Anziché modificare il valore di una proprietà per eseguire un'azione, è necessario creare un metodo. Ad esempio, è possibile abilitare o disabilitare un centro informazioni di rete (NIC) rappresentato da [**\_ NetworkAdapter Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter) usando i metodi [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) e [**Disable.**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) Sebbene queste azioni possano essere rappresentate come proprietà di lettura/scrittura, la progettazione consigliata è la creazione di un metodo. In alternativa, se si vuole rendere visibile uno stato o un valore per la classe, l'approccio consigliato consiste nel creare una proprietà di lettura/scrittura anziché un metodo. In **Win32 \_ NetworkAdapter** la **proprietà NetEnabled** rende visibile lo stato della scheda, ma le modifiche tra gli stati vengono eseguite dai metodi **Enable** **o Disable.**

Le dichiarazioni di classe possono includere la dichiarazione di uno o più metodi. È possibile scegliere di ereditare i metodi di una classe padre o implementare i propri metodi. Se si sceglie di implementare metodi personalizzati, è necessario dichiarare il metodo e contrassegnare il metodo con tag di qualificatore specifici.

La procedura seguente descrive come dichiarare un metodo in una classe che non eredita da una classe di base.

**Per dichiarare un metodo**

1.  Definire il nome del metodo tra le parentesi graffe di una dichiarazione di classe, seguite da eventuali qualificatori.

    Nell'esempio di codice seguente viene descritta la sintassi per un metodo .

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  Al termine, inserire il Managed Object Format (MOF) nel repository WMI con una chiamata al compilatore MOF.

    Per altre informazioni, vedere [Compilazione di file MOF](compiling-mof-files.md).

Nell'elenco seguente vengono definiti gli elementi della dichiarazione del metodo .

<dl> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)
</dt> <dd>

Collega un provider specifico alla descrizione della classe. Il valore del [**qualificatore Provider**](/windows/desktop/api/Provider/nl-provider-provider) è il nome del provider, che indica a WMI dove risiede il codice che supporta il metodo. Un provider deve anche contrassegnare con **il qualificatore Dynamic** qualsiasi classe con istanze dinamiche. Al contrario, non usare il **qualificatore Dynamic** per contrassegnare una classe che contiene un'istanza statica con **metodi implementati.**

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementato**
</dt> <dd>

Dichiara che verrà implementato un metodo, anziché ereditare l'implementazione del metodo dalla classe padre. Per impostazione predefinita, WMI propaga l'implementazione della classe padre a una classe derivata, a meno che la classe derivata non fornisce un'implementazione. L'omissione del qualificatore **Implemented** indica che il metodo non ha alcuna implementazione in tale classe. Se si ridecla un metodo senza il qualificatore **Implemented,** WMI presuppone comunque che non si implementerà tale metodo e richiama l'implementazione del metodo della classe padre quando viene chiamato. Di conseguenza, ridichiare un metodo in una classe derivata senza associare il qualificatore **Implemented** è utile solo quando si aggiunge o rimuove un qualificatore da o verso il metodo.

</dd> <dt>

<span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>Returntype
</dt> <dd>

Descrive il valore restituito dal metodo. Il valore restituito per un metodo deve essere un oggetto booleano, numerico, **CHAR,** **STRING,** [DATETIME](datetime.md)o schema. È anche possibile dichiarare il tipo restituito [come VOID,](void.md)a indicare che il metodo non restituisce nulla. Tuttavia, non è possibile dichiarare una matrice come tipo di valore restituito.

</dd> <dt>

<span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>Methodname
</dt> <dd>

Definisce il nome del metodo. Ogni metodo deve avere un nome univoco. WMI non consente l'esistenza di due metodi con lo stesso nome e firme diverse in una classe o all'interno di una gerarchia di classi. Di conseguenza, non è anche possibile eseguire l'overload di un metodo .

</dd> <dt>

<span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>Parameterdirection
</dt> <dd>

Contiene qualificatori che descrivono se un parametro è un parametro di input, un parametro di output o entrambi. Non usare più volte lo stesso nome di parametro come parametro di input o più volte come parametro di output. Se lo stesso nome di parametro viene visualizzato con entrambi i qualificatori [**In**](standard-qualifiers.md) e **Out,** la funzionalità è concettualmente la stessa dell'uso dei qualificatori **In**, **Out** in un singolo parametro. Tuttavia, quando si usano dichiarazioni separate, i parametri di input e di output devono essere esattamente gli stessi in tutti gli altri aspetti, inclusi il numero e il tipo di qualificatori [**ID,**](standard-wmi-qualifiers.md) e il qualificatore deve essere lo stesso e dichiarato in modo esplicito per entrambi. È consigliabile usare i qualificatori **In**, **Out** all'interno di una singola dichiarazione di parametro.

</dd> <dt>

<span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**
</dt> <dd>

Contiene il [**qualificatore ID**](standard-wmi-qualifiers.md) che identifica in modo univoco la posizione di ogni parametro all'interno della sequenza di parametri nel metodo . Per impostazione predefinita, il compilatore MOF contrassegna automaticamente i parametri con un **qualificatore ID.** Il compilatore contrassegna il primo parametro con un valore pari a 0 (zero), il secondo parametro un valore pari a 1 (uno) e così via. Se necessario, è possibile indicare in modo esplicito la sequenza ID nel codice MOF.

</dd> <dt>

<span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>Parametertype
</dt> <dd>

Descrive il tipo di dati che il metodo può accettare. È possibile definire un tipo di parametro come qualsiasi valore di dati MOF, incluso una matrice, un oggetto schema o un riferimento. Quando si usa una matrice come parametro, usare la matrice come non associata o con una dimensione esplicita.

</dd> <dt>

<span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>Parametername
</dt> <dd>

Contiene il nome del parametro. È anche possibile scegliere di definire il valore predefinito del parametro a questo punto. I parametri privi di valori iniziali rimangono non assegnati.

</dd> </dl>

L'esempio di codice seguente descrive l'elenco di parametri e i qualificatori.

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

L'esempio di codice seguente descrive come usare una matrice in un parametro MOF.

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

L'esempio di codice seguente descrive l'uso di un oggetto schema come parametro e valore restituito.

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

L'esempio di codice seguente descrive come includere due riferimenti: uno a un'istanza della classe [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e l'altro a un'istanza di un tipo di oggetto sconosciuto.

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

## <a name="creating-a-wmi-class-method-in-c"></a>Creazione di un metodo della classe WMI in C++

La procedura seguente descrive come creare un metodo della classe WMI a livello di codice.

**Per creare un metodo della classe WMI a livello di codice**

1.  Creare la classe a cui appartiene il metodo.

    Prima di creare il metodo è necessario disporre di una classe in cui inserire il metodo .

2.  Recuperare due classi figlio della [**\_ \_ classe di**](--parameters.md) sistema PARAMETERS usando [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

    Usare la prima classe figlio per descrivere i parametri in e la seconda per descrivere i parametri out. Se necessario, è possibile eseguire un singolo recupero seguito da una chiamata al metodo [**IWbemClassObject::Clone.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)

3.  Scrivere i parametri in nella prima classe e i parametri out nella seconda classe, usando una o più chiamate a [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Quando si descrivono i parametri di un metodo, osservare le regole e le restrizioni seguenti:

    -   Considerare i parametri in, out come voci separate, una nell'oggetto che contiene i parametri in e una nell'oggetto che \[ \] contiene i parametri out.
    -   Oltre ai \[ qualificatori in, \] out, i qualificatori rimanenti devono essere esattamente gli stessi.
    -   Specificare i [**qualificatori ID,**](standard-wmi-qualifiers.md) a partire da 0 (zero), uno per ogni parametro.

        L'ordine dei parametri di input o di output viene stabilito dal valore del qualificatore [**ID**](standard-wmi-qualifiers.md) in ogni parametro. Tutti gli argomenti di input devono precedere qualsiasi argomento di output. La modifica dell'ordine dei parametri di input e di output del metodo durante l'aggiornamento di un provider di metodi esistente può causare l'esito negativo delle applicazioni che chiamano il metodo . Aggiungere nuovi parametri di input alla fine dei parametri esistenti anziché inserirli nella sequenza già stabilita.

        Assicurarsi di non lasciare spazi vuoti nella sequenza di [**qualificatori ID.**](standard-wmi-qualifiers.md)

    -   Inserire il valore restituito nella classe out-parameters come proprietà denominata **ReturnValue**.

        Identifica la proprietà come valore restituito del metodo . Il tipo CIM di questa proprietà è il tipo restituito del metodo. Se il metodo ha un tipo restituito void, non dispone di una **proprietà ReturnValue.** Inoltre, la **proprietà ReturnValue** non può avere un [**qualificatore ID**](standard-wmi-qualifiers.md) come gli argomenti del metodo. L'assegnazione di **un qualificatore ID** **alla proprietà ReturnValue** genera un errore WMI.

    -   Esprimere tutti i valori dei parametri predefiniti per la proprietà nella classe .

4.  Inserire entrambi gli oggetti [**\_ \_ PARAMETERS**](--parameters.md) nella classe padre con una chiamata a [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

    Una singola chiamata a [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) può inserire entrambi [**\_ \_ gli oggetti PARAMETERS**](--parameters.md) nella classe .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una classe](creating-a-class.md)
</dt> </dl>

 

 
