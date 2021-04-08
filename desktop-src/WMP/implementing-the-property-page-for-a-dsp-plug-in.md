---
title: Implementazione della pagina delle proprietà per un plug-in DSP
description: Implementazione della pagina delle proprietà per un plug-in DSP
ms.assetid: 3dd3e547-fd06-4f01-8731-da1f8c958a32
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, proprietà audio
- Plug-in DSP, proprietà audio
- plug-in DSP audio, proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec87318b77fec4e9218398c1cb43dd5954a49e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855798"
---
# <a name="implementing-the-property-page-for-a-dsp-plug-in"></a>Implementazione della pagina delle proprietà per un plug-in DSP

Windows Media Player può visualizzare una pagina delle proprietà per ogni plug-in DSP per consentire agli utenti di impostare valori che modificano il comportamento del plug-in. Gli utenti possono accedere alla pagina delle proprietà dalla scheda **plug-** in della finestra di dialogo Opzioni facendo clic sul nome del plug-in DSP per selezionarlo e quindi fare clic su **Proprietà**.

Il codice di esempio della procedura guidata plug-in di Windows Media Player fornisce un'implementazione predefinita di una pagina delle proprietà che include una singola casella di modifica che riceve dall'utente un valore che rappresenta un fattore di scala per il volume audio. Quando l'utente fa clic su **applica**, la pagina delle proprietà passa questo valore all'oggetto plug-in in modo che il plug-in possa modificare il valore usato per la scalabilità del volume durante l'elaborazione.

## <a name="about-the-property-page-object"></a>Informazioni sull'oggetto pagina delle proprietà

L'oggetto pagina delle proprietà è un oggetto COM che implementa l'interfaccia **IPropertyPage** . Il codice di esempio generato dalla procedura guidata per il plug-in utilizza l'implementazione ATL di **IPropertyPage**, documentata nella documentazione di Visual C++ su MSDN. Il codice deve almeno fornire implementazioni di override per **IPropertyPage:: OnInitDialog**, che gestisce l'evento che si verifica quando viene visualizzata la pagina delle proprietà e **IPropertyPage:: Apply**, che gestisce l'evento che si verifica quando l'utente fa clic su **applica**. La creazione guidata plug-in genera codice di esempio per ognuno di questi gestori di eventi. L'implementazione di esempio di **OnInitDialog** recupera un valore dal registro di sistema in modo che possa visualizzare l'impostazione del fattore di scala corrente. L'implementazione di esempio di **Apply** convalida l'input dell'utente eseguendo un test per assicurarsi che rientri in un intervallo specificato, quindi Salva in modo permanente il valore nel registro di sistema, quindi passa il valore (se valido) al metodo Put della proprietà del plug-in DSP, denominato **\_ scale put**.

Sarà inoltre necessario aggiungere il codice per gestire l'evento che si verifica quando l'utente modifica un valore in un controllo fornito nella pagina delle proprietà. Ad esempio, la procedura guidata plug-in implementa una funzione denominata **OnChangeScale**, che Abilita semplicemente il pulsante **applica** quando l'utente modifica il testo nella casella di modifica nella pagina delle proprietà chiamando il metodo **IsDirty** con un valore di argomento **true**.

## <a name="about-the-property-page-dialog-resource"></a>Informazioni sulla risorsa finestra di dialogo della pagina delle proprietà

L'interfaccia utente per la pagina delle proprietà viene archiviata come una risorsa finestra di dialogo. È possibile visualizzare e modificare facilmente la finestra di dialogo della pagina delle proprietà in Visual Studio selezionando la scheda **ResourceView** nella finestra dell'area di lavoro del progetto, quindi aprendo la cartella della **finestra di dialogo** e quindi facendo doppio clic sul nome della risorsa della pagina delle proprietà. L'editor di risorse della finestra di dialogo in Visual Studio fornisce gli strumenti necessari per aggiungere controlli alla finestra di dialogo della pagina delle proprietà e per creare gestori di eventi di cui è stato eseguito il mapping ai messaggi Windows appropriati. Per informazioni dettagliate su come usare l'editor di risorse in Visual Studio, vedere la Guida di Visual Studio.

## <a name="about-ispecifypropertypages"></a>Informazioni su ISpecifyPropertyPages

Se un plug-in DSP fornisce una pagina delle proprietà, il plug-in deve implementare l'interfaccia **ISpecifyPropertyPages** . Questa interfaccia contiene un solo metodo: **ISpecifyPropertyPages:: GetPages**. Si tratta del metodo che associa la pagina delle proprietà al plug-in DSP. Windows Media Player chiama questo metodo quando l'utente richiama la pagina delle proprietà, passando un parametro di tipo CAUUID, che è una matrice conteggiata di GUID. L'implementazione del plug-in di esempio di **GetPages** riempie questa struttura con un solo GUID che rappresenta l'ID di classe dell'oggetto della pagina delle proprietà del plug-in. Windows Media Player usa quindi l'ID di classe per creare l'oggetto pagina delle proprietà.

Si può notare che l'implementazione di esempio di **GetPages** USA **CoTaskMemAlloc** per allocare memoria per la struttura Guid. È responsabilità del chiamante, in questo caso Windows Media Player, di usare **CoTaskMemFree** per rilasciare la memoria. Per informazioni dettagliate sulla struttura CAUUID, vedere la documentazione di Platform SDK.

## <a name="about-the-proxystub-dll"></a>Informazioni sulla DLL proxy/stub

Per il funzionamento di un plug-in DSP in Windows Media Player 11 in esecuzione in Windows Vista, è necessario fornire una DLL proxy/stub per le interfacce personalizzate utilizzate per comunicare le modifiche nelle impostazioni da una finestra di dialogo della pagina delle proprietà alla classe del plug-in. È necessario effettuare il marshalling delle chiamate al metodo effettuate tramite tali interfacce quando le chiamate vengono effettuate tra i limiti del processo o dell'Apartment. Con la versione più recente della procedura guidata plug-in viene creato un progetto di DLL proxy/stub di esempio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




