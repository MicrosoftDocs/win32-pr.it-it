---
title: Richiesta di un oggetto per un'interfaccia
description: Richiesta di un oggetto per un'interfaccia
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a173342c7dba59c09cdef05c6b20d9d4d37da9d6971e6a7c26c1787b708121bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680742"
---
# <a name="asking-an-object-for-an-interface"></a>Richiesta di un oggetto per un'interfaccia

In precedenza si è visto che un oggetto può implementare più di un'interfaccia. L'oggetto Common Item Dialog è un esempio reale. Per supportare gli usi più tipici, l'oggetto implementa [**l'interfaccia IFileOpenDialog.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) Questa interfaccia definisce i metodi di base per visualizzare la finestra di dialogo e ottenere informazioni sul file selezionato. Per un uso più avanzato, tuttavia, l'oggetto implementa anche un'interfaccia denominata [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Un programma può usare questa interfaccia per personalizzare l'aspetto e il comportamento della finestra di dialogo aggiungendo nuovi controlli dell'interfaccia utente.

Tenere presente che ogni interfaccia COM deve ereditare, direttamente o indirettamente, [**dall'interfaccia IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) Il diagramma seguente illustra l'ereditarietà dell'oggetto Common Item Dialog.

![diagramma che mostra le interfacce esposte dall'oggetto finestra di dialogo elemento comune](images/com06.png)

Come si può vedere dal diagramma, il predecessore diretto di [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) è [**l'interfaccia IFileDialog,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) che a sua volta eredita [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). Quando si passa dalla catena di ereditarietà **da IFileOpenDialog a** **IModalWindow**, le interfacce definiscono funzionalità di finestra sempre più generalizzate. Infine, **l'interfaccia IModalWindow** eredita [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) L'oggetto Common Item Dialog implementa anche [**IFileDialogCustomize,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)presente in una catena di ereditarietà separata.

Si supponga ora di avere un puntatore [**all'interfaccia IFileOpenDialog.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) Come si ottiene un puntatore [**all'interfaccia IFileDialogCustomize?**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)

![diagramma che mostra due puntatori a interfaccia alle interfacce sullo stesso oggetto](images/com07.png)

Il semplice cast [**del puntatore IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) a un puntatore [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) non funzionerà. Non esiste un modo affidabile per eseguire il "cross cast" in una gerarchia di ereditarietà, senza una qualche forma di informazioni sul tipo di runtime (RTTI), che è una funzionalità altamente dipendente dal linguaggio.

L'approccio COM *consiste* nel chiedere all'oggetto di fornire un puntatore [**IFileDialogCustomize,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) usando la prima interfaccia come condotto nell'oggetto. Questa operazione viene eseguita chiamando il [**metodo IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) dal primo puntatore a interfaccia. È possibile pensare a **QueryInterface** come a una versione indipendente dal linguaggio della parola chiave **\_ dynamic cast** in C++.

Il [**metodo QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ha la firma seguente:

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

In base a quanto già si sa su [**CoCreateInstance,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)è possibile indovinare il [**funzionamento di QueryInterface.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

-   Il *parametro riid* è il GUID che identifica l'interfaccia richiesta. Il tipo di **dati REFIID** è un **typedef** per `const GUID&` . Si noti che l'identificatore di classe (CLSID) non è obbligatorio, perché l'oggetto è già stato creato. È necessario solo l'identificatore di interfaccia.
-   Il *parametro ppvObject* riceve un puntatore all'interfaccia . Il tipo di dati di questo parametro è **\* \* void**, per lo stesso motivo per cui [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa questo tipo di dati: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) può essere usato per eseguire query per qualsiasi interfaccia COM, pertanto il parametro non può essere fortemente tipizzato.

Ecco come chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un [**puntatore IFileDialogCustomize:**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



Come sempre, controllare il **valore restituito HRESULT,** nel caso in cui il metodo non riesca. Se il metodo ha esito positivo, è necessario chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) al termine dell'uso del puntatore, come descritto in Gestione della [durata di un oggetto](managing-the-lifetime-of-an-object.md).

## <a name="next"></a>Prossima

[Allocazione di memoria in COM](memory-allocation-in-com.md)

 

 