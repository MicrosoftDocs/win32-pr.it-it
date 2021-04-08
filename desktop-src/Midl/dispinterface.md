---
title: dispinterface (attributo)
description: L'istruzione dispatch definisce un set di proprietà e metodi sui quali è possibile chiamare IDispatch Invoke.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- attributo dispatch MIDL
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872494"
---
# <a name="dispinterface-attribute"></a>dispinterface (attributo)

L'istruzione **Dispatch** definisce un set di proprietà e metodi su cui è possibile chiamare **IDispatch:: Invoke**. Un'interfaccia dispatch può essere definita elencando in modo esplicito il set di metodi e proprietà supportati (sintassi 1) o elencando una singola interfaccia (sintassi 2).

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attributes* 
</dt> <dd>

Specifica gli attributi che si applicano all'intera **interfaccia dispatch**. Sono accettati gli attributi seguenti: **\[** [**helpstring**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , fileguida **\[** [](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , non **\[** [**estensibile**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** e **\[** [**Version**](version.md) **\]** .

</dd> <dt>

*dispatch-nome* 
</dt> <dd>

Nome con cui l' **interfaccia dispatch** è nota nella libreria dei tipi. Questo nome deve essere univoco all'interno della libreria dei tipi.

</dd> <dt>

*elenco proprietà* 
</dt> <dd>

(Sintassi 1) Elenco facoltativo di proprietà supportate dall'oggetto, dichiarate sotto forma di variabili. Si tratta della forma abbreviata per dichiarare le funzioni di proprietà nell'elenco dei metodi. Per informazioni dettagliate, vedere la sezione commenti.

</dd> <dt>

*elenco di metodi* 
</dt> <dd>

(Sintassi 1) Elenco che comprende un prototipo di funzione per ogni metodo e proprietà nell' **interfaccia dispatch**. In *meth* è possibile visualizzare un numero qualsiasi di definizioni di funzione. Una funzione in *meth* è il formato seguente:

**\[  attributi \]** *returnType MethName tipo paramName ***(*** params * * *);**

Gli attributi seguenti sono accettati in un metodo in un' **interfaccia dispatch**: **\[ helpstring \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** , **\[** [**propputref**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** e **\[** [**vararg**](vararg.md) **\]** . Se viene specificato **\[ \] vararg** , l'ultimo parametro deve essere una matrice sicura di tipo **Variant** .

L'elenco di parametri è un elenco delimitato da virgole, in cui ogni elemento ha il formato seguente:

**\[***attributi***\]**

Il *tipo* può essere qualsiasi tipo dichiarato o incorporato o un puntatore a qualsiasi tipo. Gli attributi nei parametri sono:

**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**Optional**](optional.md) **\]** , **\[ stringa \]**

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

(Sintassi 2) Nome dell'interfaccia da dichiarare come interfaccia IDispatch.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):

1.  Parametri obbligatori (parametri che non dispongono degli \[ \] attributi DefaultValue o \[ Optional \] ),
2.  parametri facoltativi con o senza \[ l' \] attributo DefaultValue,
3.  parametri con l' \[ \] attributo facoltativo e senza l' \[ \] attributo DefaultValue,
4.  \[parametro [**LCID**](lcid.md) \] , se presente,
5.  \[[**retval**](retval.md) \] parametro

Le funzioni di metodo vengono specificate esattamente come descritto nella pagina di riferimento per il [**modulo**](module.md) , ad eccezione del fatto che l' \[ attributo [**entry**](entry.md) \] non è consentito. Si noti che STDOLE32. TLB (STDOLE. È necessario importare TLB nei sistemi a 16 bit perché un' **interfaccia dispatch** eredita da IDispatch.

È possibile dichiarare le proprietà negli elenchi delle proprietà o dei metodi. La dichiarazione delle proprietà nell'elenco delle proprietà non indica il tipo di accesso supportato dalla proprietà (ovvero Get, put o putref). Specificare l' \[ [](readonly.md) \] attributo ReadOnly per le proprietà che non supportano put o putref. Se si dichiarano le funzioni di proprietà nell'elenco dei metodi, le funzioni per una proprietà hanno tutti lo stesso identificatore.

Con la prima sintassi sono necessari i tag Properties: e:. L' \[ attributo [**ID**](id.md) \] è obbligatorio anche per ogni membro. Ad esempio:

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

A differenza dei membri di interfaccia, i membri dell'interfaccia dispatch non possono usare l'attributo [**retval**](retval.md) per restituire un valore oltre a un codice di errore HRESULT. L' \[ [](lcid.md) \] attributo LCID è altrettanto non valido per dispinterfaces, perché IDispatch:: Invoke passa un LCID. Tuttavia, è possibile dichiarare nuovamente un'interfaccia che utilizza questi attributi.

Utilizzando la seconda sintassi, le interfacce che supportano IDispatch e vengono dichiarate in precedenza in uno script FAD possono essere ridichiarate come interfacce IDispatch come indicato di seguito:

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

Nell'esempio precedente vengono dichiarati tutti i membri di Hello e tutti i membri che Hello eredita come supporto IDispatch. In questo caso, se Hello venisse dichiarato in precedenza con \[ \] \[ i membri LCID e retval \] che restituivano HRESULT, MkTypLib rimuoverebbe ogni \[ \] parametro LCID e il tipo restituito HRESULT e invece contrassegnerà il tipo restituito come quello del \[ \] parametro retval.

> [!Note]  
> Lo strumento Mktyplib.exe è obsoleto. Usare invece il compilatore MIDL.

 

Le proprietà e i metodi di un'interfaccia dispatch non fanno parte di VTBL dell'interfaccia dispatch. Di conseguenza, non è possibile usare [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) e [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) per implementare IDispatch:: Invoke. L'interfaccia dispatch viene usata quando un'applicazione deve esporre le funzioni non VTBL esistenti tramite l'automazione. Queste applicazioni possono implementare IDispatch:: Invoke esaminando il parametro dispidMember e chiamando direttamente la funzione corrispondente.

## <a name="examples"></a>Esempi

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**nascosto**](hidden.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**opzionale**](optional.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**nonextensible**](nonextensible.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**limitato**](restricted.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 