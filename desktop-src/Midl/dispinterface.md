---
title: dispinterface (attributo)
description: L'istruzione dispatchinterface definisce un set di proprietà e metodi su cui è possibile chiamare IDispatch Invoke.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- Attributo dispinterface MIDL
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3df65adc3bfa486907df0465f2fca5a1427f6d0b1eb89b5c02e6f199be71e9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384668"
---
# <a name="dispinterface-attribute"></a>dispinterface (attributo)

**L'istruzione dispatchinterface** definisce un set di proprietà e metodi su cui è possibile chiamare **IDispatch::Invoke**. Un'interfaccia dispatch può essere definita elencando in modo esplicito il set di metodi e proprietà supportati (sintassi 1) o elencando una singola interfaccia (sintassi 2).

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

Specifica gli attributi applicabili all'intera **interfaccia dispatch.** Sono accettati gli attributi seguenti: **\[** [**helpstring**](helpstring.md) **\]** , **\[** [**helpcontext**](helpcontext.md) **\]** , **\[** [**helpfile**](helpfile.md), **\]** **\[** [**hidden**](hidden.md) **\]** , **\[** [**nonextensible**](nonextensible.md), **\]** **\[** [**oleautomation**](oleautomation.md), **\]** **\[** [**restricted**](restricted.md), **\]** **\[** [**uuid**](uuid.md)e **\]** **\[** [**version**](version.md) **\]** .

</dd> <dt>

*dispinterface-name* 
</dt> <dd>

Nome con cui **l'interfaccia dispatch** è nota nella libreria dei tipi. Questo nome deve essere univoco all'interno della libreria dei tipi.

</dd> <dt>

*property-list* 
</dt> <dd>

(Sintassi 1) Elenco facoltativo di proprietà supportate dall'oggetto , dichiarato sotto forma di variabili. Questa è la forma breve per dichiarare le funzioni di proprietà nell'elenco dei metodi. Per informazioni dettagliate, vedere la sezione relativa ai commenti.

</dd> <dt>

*method-list* 
</dt> <dd>

(Sintassi 1) Elenco che comprende un prototipo di funzione per ogni metodo e proprietà **nell'interfaccia dispatch.** Qualsiasi numero di definizioni di funzione può essere visualizzato in *methlist*. Una funzione in *methlist* ha il formato seguente:

**\[**_attributi_ *_\]_* *returntype methname type paramname***(**_params_*_);_*

Gli attributi seguenti vengono accettati in un metodo in un'interfaccia **dispatch:** **\[ helpstring \]**, **\[ helpcontext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md), **\]** **\[** [**propputref**](propputref.md), **\]** **\[** [**string**](string.md)e **\]** **\[** [**vararg**](vararg.md) **\]** . Se **\[ si \] specifica vararg,** l'ultimo parametro deve essere una matrice sicura di **tipo VARIANT.**

L'elenco di parametri è un elenco delimitato da virgole, di cui ogni elemento ha il formato seguente:

**\[**_Attributi_*_\]_*

Il *tipo* può essere qualsiasi tipo dichiarato o predefinito o un puntatore a qualsiasi tipo. Gli attributi nei parametri sono:

**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**optional**](optional.md) **\]** , **\[ string \]**

</dd> <dt>

*interface-name* 
</dt> <dd>

(Sintassi 2) Nome dell'interfaccia da dichiarare come interfaccia IDispatch.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):

1.  Parametri obbligatori (parametri che non hanno il \[ valore predefinito o attributi \] \[ \] facoltativi),
2.  parametri facoltativi con o senza \[ l'attributo \] defaultvalue,
3.  parametri con \[ l'attributo \] facoltativo e senza \[ l'attributo \] defaultvalue,
4.  \[[**Parametro lcid,**](lcid.md) \] se presente,
5.  \[[**retval**](retval.md) \] Parametro

Le funzioni di metodo vengono specificate esattamente come descritto nella pagina di riferimento per [**il modulo,**](module.md) ad eccezione del fatto che l'attributo \[ [**entry**](entry.md) \] non è consentito. Si noti che STDOLE32. TLB (STDOLE. TLB nei sistemi a 16 bit) deve essere importato, perché **un'interfaccia dispatch** eredita da IDispatch.

È possibile dichiarare le proprietà negli elenchi di proprietà o metodi. La dichiarazione di proprietà nell'elenco delle proprietà non indica il tipo di accesso supportato dalla proprietà, ovvero get, put o putref. Specificare \[ [**l'attributo readonly**](readonly.md) \] per le proprietà che non supportano put o putref. Se si dichiarano le funzioni di proprietà nell'elenco dei metodi, tutte le funzioni per una proprietà hanno lo stesso identificatore.

Usando la prima sintassi, sono necessari i tag properties: e methods: . \[ [**L'attributo id**](id.md) \] è obbligatorio anche per ogni membro. Esempio:

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

A differenza dei membri di interfaccia, i membri dell'interfaccia dispatch non possono usare [**l'attributo retval**](retval.md) per restituire un valore oltre a un codice di errore HRESULT. Anche \[ [**l'attributo lcid**](lcid.md) \] non è valido per le interfacce dispatch, perché IDispatch::Invoke passa un LCID. Tuttavia, è possibile rideclare un'interfaccia che usa questi attributi.

Usando la seconda sintassi, le interfacce che supportano IDispatch e sono dichiarate in precedenza in uno script ODL possono essere ridichiare come interfacce IDispatch come indicato di seguito:

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

L'esempio precedente dichiara tutti i membri di hello e tutti i membri che hello ereditano come IDispatch di supporto. In questo caso, se hello è stato dichiarato in precedenza con membri lcid e retval che hanno restituito \[ \] \[ \] HRESULT, MkTypLib rimuove ogni parametro lcid e il tipo restituito HRESULT e contrassegna invece il tipo restituito come quello del \[ \] parametro \[ retval. \]

> [!Note]  
> Lo Mktyplib.exe è obsoleto. Usare invece il compilatore MIDL.

 

Le proprietà e i metodi di un'interfaccia dispatch non fanno parte del VTBL dell'interfaccia dispatch. Di conseguenza, [non è possibile usare CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) e [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) per implementare IDispatch::Invoke. L'interfaccia dispatch viene usata quando un'applicazione deve esporre funzioni non VTBL esistenti tramite Automazione. Queste applicazioni possono implementare IDispatch::Invoke esaminando il parametro dispidMember e chiamando direttamente la funzione corrispondente.

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

[**Nascosto**](hidden.md)
</dt> <dt>

[**Pollici**](in.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Opzionale**](optional.md)
</dt> <dt>

[**in uscita**](out-idl.md)
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

[**Limitato**](restricted.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 