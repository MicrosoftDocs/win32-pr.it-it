---
title: Richiesta di un oggetto per un'interfaccia
description: Richiesta di un oggetto per un'interfaccia
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fa740f0ef770e069ee03b644bbfcb9b2c5e0eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046753"
---
# <a name="asking-an-object-for-an-interface"></a>Richiesta di un oggetto per un'interfaccia

Abbiamo visto in precedenza che un oggetto può implementare più di un'interfaccia. L'oggetto finestra di dialogo elemento comune è un esempio reale di questo. Per supportare gli utilizzi più comuni, l'oggetto implementa l'interfaccia [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Questa interfaccia definisce i metodi di base per visualizzare la finestra di dialogo e ottenere informazioni sul file selezionato. Per un uso più avanzato, tuttavia, l'oggetto implementa anche un'interfaccia denominata [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Un programma può usare questa interfaccia per personalizzare l'aspetto e il comportamento della finestra di dialogo aggiungendo nuovi controlli dell'interfaccia utente.

Si ricordi che ogni interfaccia COM deve ereditare, direttamente o indirettamente, dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Nel diagramma seguente viene illustrata l'ereditarietà dell'oggetto finestra di dialogo elemento comune.

![diagramma che mostra le interfacce esposte dall'oggetto finestra di dialogo elemento comune](images/com06.png)

Come si può notare dal diagramma, il predecessore diretto di [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) è l'interfaccia [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) , che a sua volta eredita [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). Man mano che si passa alla catena di ereditarietà da **IFileOpenDialog** a **IModalWindow**, le interfacce definiscono funzionalità della finestra sempre più generalizzate. Infine, l'interfaccia **IModalWindow** eredita [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). L'oggetto finestra di dialogo elemento comune implementa anche [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), presente in una catena di ereditarietà separata.

Si supponga ora di avere un puntatore all'interfaccia [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Come si ottiene un puntatore all'interfaccia [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ?

![diagramma che mostra due puntatori a interfaccia per le interfacce sullo stesso oggetto](images/com07.png)

Il semplice cast del puntatore [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) a un puntatore [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) non funzionerà. Non esiste un modo affidabile per "cross cast" in una gerarchia di ereditarietà, senza alcuna forma di informazioni sui tipi in fase di esecuzione (RTTI), che è una funzionalità altamente dipendente dal linguaggio.

L'approccio COM consiste nel *richiedere* all'oggetto di fornire un puntatore [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , usando la prima interfaccia come canale nell'oggetto. Questa operazione viene eseguita chiamando il metodo [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) dal primo puntatore di interfaccia. È possibile considerare **QueryInterface** come una versione indipendente dal linguaggio della parola chiave **Dynamic \_ cast** in C++.

Il metodo [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ha la firma seguente:

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

In base a quanto già noto su [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), potrebbe essere possibile indovinare il funzionamento di [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

-   Il parametro *riid* è il GUID che identifica l'interfaccia richiesta. Il tipo di dati **REFIID** è un **typedef** per `const GUID&` . Si noti che l'identificatore di classe (CLSID) non è obbligatorio perché l'oggetto è già stato creato. È necessario solo l'identificatore di interfaccia.
-   Il parametro *ppvObject* riceve un puntatore all'interfaccia. Il tipo di dati di questo parametro **è \* \* void**, per lo stesso motivo per cui [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilizza questo tipo di dati: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) può essere utilizzato per eseguire una query per qualsiasi interfaccia com, quindi il parametro non può essere fortemente tipizzato.

Di seguito viene illustrato come chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) :


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



Come sempre, controllare il valore restituito **HRESULT** , nel caso in cui il metodo abbia esito negativo. Se il metodo ha esito positivo, è necessario chiamare [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) al termine dell'utilizzo del puntatore, come descritto in [gestione della durata di un oggetto](managing-the-lifetime-of-an-object.md).

## <a name="next"></a>Prossima

[Allocazione di memoria in COM](memory-allocation-in-com.md)

 

 