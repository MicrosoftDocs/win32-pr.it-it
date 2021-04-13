---
title: Anatomia di un file IDL
description: In questi file IDL di esempio vengono illustrati i costrutti fondamentali della definizione dell'interfaccia.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "104351011"
---
# <a name="anatomy-of-an-idl-file"></a>Anatomia di un file IDL

In questi file IDL di esempio vengono illustrati i costrutti fondamentali della definizione dell'interfaccia. L'allocazione di memoria, il marshalling personalizzato e la messaggistica asincrona sono solo alcune delle funzionalità che è possibile implementare in un'interfaccia COM personalizzata. Gli attributi MIDL vengono utilizzati per definire le interfacce COM. Per ulteriori informazioni sull'implementazione di interfacce e librerie dei tipi, incluso un riepilogo degli attributi MIDL, vedere [definizioni di interfaccia e librerie dei tipi](/windows/desktop/Midl/interface-definitions-and-type-libraries) nella guida e guida di riferimento per programmatori MIDL. Per un riferimento completo di tutti gli attributi, le parole chiave e le direttive MIDL, vedere le informazioni di [riferimento sul linguaggio MIDL](/windows/desktop/Midl/midl-language-reference).

## <a name="exampleidl"></a>Esempio di IDL

Il file IDL di esempio seguente definisce due interfacce COM. Da questo file IDL Midl.exe genererà i file di intestazione e il codice di marshalling e di marshalling. Una dissezione riga per riga segue l'esempio.

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

L'istruzione di [**importazione**](/windows/desktop/Midl/import) IDL viene utilizzata qui per inserire un file di intestazione, Mydefs. h, che contiene i tipi definiti dall'utente e Unknwn. idl, che contiene la definizione di [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), da cui derivano IFace1 e IFace2.

L'attributo [**Object**](/windows/desktop/Midl/object) identifica l'interfaccia come un'interfaccia oggetto e indica al compilatore MIDL di generare codice proxy/stub anziché stub client e server RPC. I metodi dell'interfaccia oggetto devono avere un tipo restituito [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), per consentire al meccanismo RPC sottostante di segnalare gli errori per le chiamate che non vengono completate a causa di problemi di rete.

L'attributo [**UUID**](/windows/desktop/Midl/uuid) specifica l'identificatore di interfaccia (IID). Ogni interfaccia, classe e libreria dei tipi deve essere identificata con il relativo identificatore univoco. Utilizzare l'utilità Uuidgen.exe per generare un set di ID univoci per le interfacce e altri componenti.

La parola chiave [**Interface**](/windows/desktop/Midl/interface) definisce il nome dell'interfaccia. Tutte le interfacce oggetto devono derivare, direttamente o indirettamente, da [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).

Il parametro [**in**](/windows/desktop/Midl/in) direzionale specifica un parametro che viene impostato solo dal chiamante. Il parametro [**out**](/windows/desktop/Midl/out-idl) specifica i dati che vengono passati di nuovo al chiamante. L'uso di entrambi gli attributi direzionali in un parametro specifica che il parametro viene usato sia per inviare dati al metodo che per passare i dati al chiamante.

L' [**attributo \_ default del puntatore**](/windows/desktop/Midl/pointer-default) specifica il tipo di puntatore predefinito ([**Unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)o [**ptr**](/windows/desktop/Midl/ptr)) per tutti i puntatori tranne quelli inclusi negli elenchi di parametri. Se non viene specificato alcun tipo predefinito, MIDL presuppone che i puntatori singoli siano **univoci**. Tuttavia, quando si dispone di più livelli di puntatori, è necessario specificare in modo esplicito un tipo di puntatore predefinito, anche se si desidera che il tipo predefinito sia **univoco**.

Nell'esempio precedente, la matrice BkfstStuff \[ \] è una *matrice conforme*, la cui dimensione è determinata in fase di esecuzione. L'attributo [**Max \_ is**](/windows/desktop/Midl/max-is) specifica la variabile che contiene il valore massimo per l'indice della matrice.

L'attributo [**size \_ è**](/windows/desktop/Midl/size-is) usato anche per specificare la dimensione di una matrice o, come nell'esempio precedente, più livelli di puntatori. Nell'esempio, la chiamata può essere effettuata senza conoscere in anticipo la quantità di dati che verranno restituiti.

## <a name="example2idl"></a>Example2. idl

Nell'esempio IDL seguente, che riutilizza le interfacce descritte nell'esempio IDL precedente, vengono illustrati i vari modi per generare informazioni sulla libreria dei tipi per le interfacce.

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

L'attributo [**helpstring**](/windows/desktop/Midl/helpstring) è facoltativo. viene usato per descrivere brevemente l'oggetto o per fornire una riga di stato. Queste stringhe della guida sono leggibili con un Visualizzatore oggetti, ad esempio quello fornito con Microsoft Visual Basic.

L'attributo [**duale**](/windows/desktop/Midl/dual) in IFace3 crea un'interfaccia che è sia un'interfaccia dispatch che un'interfaccia com. Poiché è derivato da **IDispatch**, un'interfaccia duale supporta l'automazione, che è l'elemento specificato dall'attributo [**oleautomation**](/windows/desktop/Midl/oleautomation) . IFace3 importa OAIDL. idl per ottenere la definizione di **IDispatch**.

L'istruzione [**Library**](/windows/desktop/Midl/library) definisce la libreria dei tipi ExampleLib, che ha gli attributi [**UUID**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring)e [**Version**](/windows/desktop/Midl/version) .

All'interno della definizione della libreria dei tipi, la direttiva [**importlib**](/windows/desktop/Midl/importlib) porta in una libreria dei tipi compilata. Tutte le definizioni di librerie dei tipi devono inserire la libreria dei tipi di base definita in Stdole32. tlb.

Questa definizione della libreria dei tipi illustra tre modi diversi per includere le interfacce nella libreria dei tipi. IFace3 è incluso semplicemente facendo riferimento all'interno dell'istruzione Library.

L'istruzione [**coclass**](/windows/desktop/Midl/coclass) definisce una classe di componenti completamente nuova, BkfstComponent, che include due interfacce definite in precedenza, IFace1 e IFace2. L'attributo default designa IFace1 come interfaccia predefinita.

IFace4 è descritto nell'istruzione Library. L'attributo [**propput**](/windows/desktop/Midl/propput) su methodd indica che il metodo esegue un'azione set su una proprietà con lo stesso nome. L'attributo [**propget**](/windows/desktop/Midl/propget) indica che il metodo recupera informazioni da una proprietà con lo stesso nome del metodo. L'attributo [**retval**](/windows/desktop/Midl/retval) in methodd definisce un parametro di output che contiene il valore restituito della funzione.

 

 
