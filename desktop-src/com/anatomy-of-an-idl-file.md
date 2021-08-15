---
title: Anatomia di un file IDL
description: Questi file IDL di esempio illustrano i costrutti fondamentali della definizione dell'interfaccia.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531d46bfcfa0ef4e4eee075ae65b64dd0c80a8f6a51543a1762a0ddcd8a03888
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311335"
---
# <a name="anatomy-of-an-idl-file"></a>Anatomia di un file IDL

Questi file IDL di esempio illustrano i costrutti fondamentali della definizione dell'interfaccia. L'allocazione di memoria, il marshalling personalizzato e la messaggistica asincrona sono solo alcune delle funzionalità che è possibile implementare in un'interfaccia COM personalizzata. Gli attributi MIDL vengono usati per definire le interfacce COM. Per altre informazioni sull'implementazione di interfacce e librerie dei tipi, incluso un riepilogo degli attributi MIDL, vedere [Interface Definitions and Type Libraries](/windows/desktop/Midl/interface-definitions-and-type-libraries) (Definizioni di interfaccia e librerie dei tipi) in MIDL Programmer's Guide and Reference (Guida e riferimento per programmatori MIDL). Per informazioni di riferimento complete su tutti gli attributi, le parole chiave e le direttive MIDL, vedere MIDL Language Reference (Riferimenti [al linguaggio MIDL).](/windows/desktop/Midl/midl-language-reference)

## <a name="exampleidl"></a>Example.idl

Il file IDL di esempio seguente definisce due interfacce COM. Da questo file IDL, Midl.exe genererà proxy/stub e il marshalling del codice e dei file di intestazione. Una sezione riga per riga segue l'esempio.

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

L'istruzione [**IDL import**](/windows/desktop/Midl/import) viene usata qui per importare un file di intestazione, Mydefs.h, che contiene tipi definiti dall'utente, e Unknwn.idl, che contiene la definizione di [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)da cui derivano IFace1 e IFace2.

[**L'attributo**](/windows/desktop/Midl/object) dell'oggetto identifica l'interfaccia come interfaccia oggetto e indica al compilatore MIDL di generare codice proxy/stub anziché stub client e server RPC. I metodi dell'interfaccia oggetto devono avere un tipo restituito [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), per consentire al meccanismo RPC sottostante di segnalare gli errori relativi alle chiamate che non vengono completate a causa di problemi di rete.

[**L'attributo uuid**](/windows/desktop/Midl/uuid) specifica l'identificatore di interfaccia (IID). Ogni interfaccia, classe e libreria dei tipi deve essere identificata con il proprio identificatore univoco. Usare l'Uuidgen.exe per generare un set di ID univoci per le interfacce e altri componenti.

La [**parola chiave interface**](/windows/desktop/Midl/interface) definisce il nome dell'interfaccia. Tutte le interfacce oggetto devono derivare, direttamente o indirettamente, da [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)

Il [**parametro in**](/windows/desktop/Midl/in) directional specifica un parametro impostato solo dal chiamante. Il [**parametro out**](/windows/desktop/Midl/out-idl) specifica i dati che vengono passati al chiamante. L'uso di entrambi gli attributi direzionali in un parametro specifica che il parametro viene usato sia per inviare dati al metodo che per passare di nuovo i dati al chiamante.

[**L'attributo \_ predefinito del**](/windows/desktop/Midl/pointer-default) puntatore specifica il tipo di puntatore predefinito ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)o [**ptr**](/windows/desktop/Midl/ptr)) per tutti i puntatori ad eccezione di quelli inclusi negli elenchi di parametri. Se non viene specificato alcun tipo predefinito, MIDL presuppone che i singoli puntatori siano **univoci.** Tuttavia, quando si dispone di più livelli di puntatori, è necessario specificare in modo esplicito un tipo di puntatore predefinito, anche se si vuole che il tipo predefinito sia **univoco.**

Nell'esempio precedente la matrice BkfstStuff è una matrice conforme, la cui dimensione viene \[ \] determinata in fase di esecuzione.  [**\_ L'attributo max**](/windows/desktop/Midl/max-is) is specifica la variabile che contiene il valore massimo per l'indice della matrice.

[**\_ L'attributo size**](/windows/desktop/Midl/size-is) viene usato anche per specificare le dimensioni di una matrice o, come nell'esempio precedente, più livelli di puntatori. Nell'esempio la chiamata può essere effettuata senza sapere in anticipo la quantità di dati che verranno restituiti.

## <a name="example2idl"></a>Example2.idl

Nell'esempio IDL seguente (che riutilizza le interfacce descritte nell'esempio IDL precedente) vengono illustrati i vari modi per generare informazioni sulle librerie dei tipi per le interfacce.

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

[**L'attributo helpstring**](/windows/desktop/Midl/helpstring) è facoltativo. viene utilizzato per descrivere brevemente l'oggetto o per fornire una riga di stato. Queste stringhe della Guida sono leggibili con un visualizzatore oggetti, ad esempio quello fornito con Microsoft Visual Basic.

[**L'attributo dual**](/windows/desktop/Midl/dual) in IFace3 crea un'interfaccia che è sia un'interfaccia dispatch che un'interfaccia COM. Poiché deriva da **IDispatch,** un'interfaccia duale supporta l'automazione, che è ciò che [**l'attributo oleautomation**](/windows/desktop/Midl/oleautomation) specifica. IFace3 importa Oaidl.idl per ottenere la definizione di **IDispatch.**

[**L'istruzione**](/windows/desktop/Midl/library) library definisce la libreria dei tipi ExampleLib, che ha i propri [**attributi uuid**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring)e [**version.**](/windows/desktop/Midl/version)

All'interno della definizione della libreria dei tipi, la [**direttiva importlib**](/windows/desktop/Midl/importlib) include una libreria dei tipi compilata. Tutte le definizioni della libreria dei tipi devono importare la libreria dei tipi di base definita in Stdole32.tlb.

Questa definizione della libreria dei tipi illustra tre diversi modi per includere le interfacce nella libreria dei tipi. IFace3 viene incluso semplicemente facendo riferimento a esso nell'istruzione della libreria.

[**L'istruzione coclass**](/windows/desktop/Midl/coclass) definisce una classe componente completamente nuova, BkfstComponent, che include due interfacce definite in precedenza, IFace1 e IFace2. L'attributo predefinito designa IFace1 come interfaccia predefinita.

IFace4 viene descritto all'interno dell'istruzione della libreria. [**L'attributo propput**](/windows/desktop/Midl/propput) in MethodD indica che il metodo esegue un'azione set su una proprietà con lo stesso nome. [**L'attributo propget**](/windows/desktop/Midl/propget) indica che il metodo recupera informazioni da una proprietà con lo stesso nome del metodo. [**L'attributo retval**](/windows/desktop/Midl/retval) in MethodD definisce un parametro di output che contiene il valore restituito della funzione.

 

 
