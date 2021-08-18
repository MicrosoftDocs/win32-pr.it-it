---
title: Implementazione della pagina delle proprietà per un plug-in DSP
description: Implementazione della pagina delle proprietà per un plug-in DSP
ms.assetid: 3dd3e547-fd06-4f01-8731-da1f8c958a32
keywords:
- Windows Media Player plug-in, DSP audio
- plug-in, DSP audio
- plug-in di elaborazione del segnale digitale, proprietà audio
- Plug-in DSP, proprietà audio
- plug-in DSP audio,proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac64dbd1e984d649a4405341d907ddd0c93eabce855bed90e83f698b778a3a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617311"
---
# <a name="implementing-the-property-page-for-a-dsp-plug-in"></a>Implementazione della pagina delle proprietà per un plug-in DSP

Windows Media Player possibile visualizzare una pagina delle proprietà per ogni plug-in DSP per consentire agli utenti di impostare valori che modificano il comportamento del plug-in. Gli utenti possono accedere alla pagina delle proprietà dalla scheda **Plug-in della** finestra di dialogo Opzioni facendo clic sul nome del plug-in DSP per selezionarlo e quindi facendo clic su **Proprietà**.

Il Windows Media Player di esempio della Creazione guidata plug-in fornisce un'implementazione predefinita di una pagina delle proprietà che include una singola casella di modifica che riceve dall'utente un valore che rappresenta un fattore di scala per il volume audio. Quando l'utente fa clic su **Applica,** la pagina delle proprietà passa questo valore all'oggetto plug-in in modo che il plug-in possa modificare il valore utilizzato per ridimensionare il volume durante l'elaborazione.

## <a name="about-the-property-page-object"></a>Informazioni sull'oggetto pagina delle proprietà

L'oggetto della pagina delle proprietà è un oggetto COM che implementa **l'interfaccia IPropertyPage.** Il codice di esempio generato dalla procedura guidata del plug-in usa l'implementazione ATL di **IPropertyPage**, documentata nella documentazione Visual C++ su MSDN. Il codice deve almeno fornire implementazioni di override per **IPropertyPage::OnInitDialog**, che gestisce l'evento che si verifica all'apertura della pagina delle proprietà, e **IPropertyPage::Apply**, che gestisce l'evento che si verifica quando l'utente fa clic su **Applica**. La procedura guidata del plug-in genera codice di esempio per ognuno di questi gestori eventi. L'implementazione di esempio **di OnInitDialog** recupera un valore dal Registro di sistema in modo che possa visualizzare l'impostazione corrente del fattore di scala. L'implementazione di esempio di **Apply** convalida l'input utente verificando che sia compreso in un intervallo specificato, quindi rende persistente il valore nel Registro di sistema e quindi passa il valore (se valido) al metodo put della proprietà plug-in DSP, denominato **put \_ scale**.

Inoltre, è necessario aggiungere codice per gestire l'evento che si verifica quando l'utente modifica un valore in un controllo specificato nella pagina delle proprietà. Ad esempio, la creazione guidata plug-in implementa una funzione  denominata **OnChangeScale**, che abilita semplicemente il pulsante Applica quando l'utente modifica il testo nella casella di modifica nella pagina delle proprietà chiamando il **metodo SetDirty** con un valore di argomento **TRUE.**

## <a name="about-the-property-page-dialog-resource"></a>Informazioni sulla risorsa finestra di dialogo Pagina delle proprietà

L'interfaccia utente per la pagina delle proprietà viene archiviata come risorsa finestra di dialogo. È possibile visualizzare e modificare facilmente la finestra di dialogo della pagina delle proprietà in Visual Studio selezionando  la scheda **ResourceView** nella finestra area di lavoro di Project, quindi aprendo la cartella Finestra di dialogo e facendo doppio clic sul nome della risorsa della pagina delle proprietà. L'editor delle risorse finestra di dialogo in Visual Studio fornisce gli strumenti necessari per aggiungere controlli alla finestra di dialogo della pagina delle proprietà e per creare gestori eventi di cui è stato eseguito il mapping ai messaggi Windows appropriati. Per informazioni dettagliate su come usare l'editor di risorse in Visual Studio, vedere Visual Studio Guida.

## <a name="about-ispecifypropertypages"></a>Informazioni su ISpecifyPropertyPages

Se un plug-in DSP fornisce una pagina delle proprietà, il plug-in deve implementare **l'interfaccia ISpecifyPropertyPages.** Questa interfaccia contiene un solo metodo: **ISpecifyPropertyPages::GetPages**. Questo è il metodo che associa la pagina delle proprietà al plug-in DSP. Windows Media Player questo metodo quando l'utente richiama la pagina delle proprietà, passando un parametro di tipo CAUUID, ovvero una matrice conteggiata di GUID. L'implementazione del plug-in di esempio **di GetPages** riempie questa struttura con un singolo GUID che rappresenta l'ID classe dell'oggetto pagina delle proprietà del plug-in. Windows Media Player quindi usa l'ID classe per creare l'oggetto pagina delle proprietà.

È possibile notare che l'implementazione di esempio di **GetPages** usa **CoTaskMemAlloc** per allocare memoria per la struttura GUID. È responsabilità del chiamante, in questo caso Windows Media Player, usare **CoTaskMemFree** per rilasciare la memoria. Per informazioni dettagliate sulla struttura CAUUID, vedere la documentazione di Platform SDK.

## <a name="about-the-proxystub-dll"></a>Informazioni sulla DLL proxy/stub

Per il funzionamento di un plug-in DSP in Windows Media Player 11 in esecuzione in Windows Vista, è necessario fornire una DLL proxy/stub per le interfacce personalizzate usate per comunicare le modifiche nelle impostazioni da una finestra di dialogo della pagina delle proprietà alla classe plug-in. È necessario effettuare il marshalling delle chiamate ai metodi effettuate tramite tali interfacce quando le chiamate vengono effettuate attraverso i limiti del processo o dell'apartment. La versione più recente della procedura guidata del plug-in crea un progetto DLL proxy/stub di esempio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




