---
description: I gestori di anteprime vengono chiamati quando viene selezionato un elemento per visualizzare un'anteprima semplice e dettagliata di sola lettura del contenuto del file nel riquadro di lettura della visualizzazione. Questa operazione viene eseguita senza avviare l'applicazione associata del file.
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: Gestori di anteprime e host di anteprima della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993c6c8e7b15d9bfc24b5dd42352407a3a53c45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979959"
---
# <a name="preview-handlers-and-shell-preview-host"></a>Gestori di anteprime e host di anteprima della shell

I gestori di anteprime vengono chiamati quando viene selezionato un elemento per visualizzare un'anteprima semplice e dettagliata di sola *lettura* del contenuto del file nel riquadro di lettura della visualizzazione. Questa operazione viene eseguita senza avviare l'applicazione associata del file.

In questo argomento vengono illustrati gli argomenti seguenti:

-   [Architettura del gestore di anteprime](#preview-handler-architecture)
-   [Opzioni del modello server](#server-model-options)
-   [Inizializzazione](#initialization)
-   [Flusso di dati del gestore di anteprime](#preview-handler-data-flow)
-   [Debug di un gestore di anteprime](#debugging-a-preview-handler)
-   [Fornire un processo personalizzato per un gestore di anteprime](#providing-your-own-process-for-a-preview-handler)
-   [Argomenti correlati](#related-topics)

## <a name="preview-handler-architecture"></a>Architettura del gestore di anteprime

Un gestore di anteprime è un'applicazione ospitata. Gli host includono Esplora risorse di Windows Vista o Microsoft Outlook 2007. Gli host implementano [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) come metodo di comunicazione tra il gestore di anteprime e l'host.

Il gestore di anteprime implementa queste interfacce:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (facoltativo)

Il gestore viene chiamato tramite il relativo [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), che restituisce un puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) attraverso il quale si richiede un oggetto [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) per interagire con l'host.

## <a name="server-model-options"></a>Opzioni del modello server

I gestori di anteprime hanno sempre esaurito il processo. Esistono due metodi per implementare questa operazione:

1.  Un gestore di anteprime può essere compilato come server in-process ma eseguito tramite un host surrogato out-of-process. Questo è il metodo preferito. Il sistema fornisce un host surrogato per questa operazione nel file di Prevhost.exe. I gestori di anteprime compilati da questo metodo non sono compatibili con Outlook 2007 in Windows XP. Tuttavia, questi stessi gestori funzioneranno in Esplora risorse e Outlook 2007 in esecuzione su Windows Vista.
2.  Un gestore di anteprime può essere compilato come server di Component Object Model locale (COM). Questa operazione non è consigliata per diversi motivi. In primo luogo, l'implementazione di un server in-process è più semplice. Ancora più importante, l'implementazione come server in-process garantisce un maggiore controllo sulla durata dell'oggetto gestore, che consente una migliore pulitura ed efficienza.

Per impostazione predefinita, i gestori di anteprime vengono eseguiti in un processo di livello di integrità basso (IL) per motivi di sicurezza. Facoltativamente, è possibile disabilitare l'esecuzione come processo IL basso impostando il valore seguente nel registro di sistema. Tuttavia, non è consigliabile farlo. È possibile che i sistemi siano configurati in modo da rifiutare qualsiasi processo che non sia IL basso.

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

Per impostazione predefinita, diversi gestori di anteprime condividono lo stesso processo. Due istanze di Prevhost.exe possono essere eseguite contemporaneamente. uno per i gestori eseguiti come processi IL Bassi, uno per i gestori che hanno rifiutato questo comportamento.

## <a name="initialization"></a>Inizializzazione

Come per i gestori di anteprime e proprietà, si consiglia vivamente di inizializzare il gestore con un flusso. Se necessario, è possibile inizializzare un file o un elemento, ma i flussi forniscono il modo più sicuro per implementare un gestore. L'inizializzazione tramite un flusso garantisce l'integrità dei file e i vantaggi di stabilità al sistema di esecuzione del gestore come processo IL basso, ad esempio la protezione del sistema dai sovraccarichi del buffer, la limitazione della posizione in cui un gestore può scrivere informazioni e la limitazione della comunicazione con altre finestre.

Se è necessario inizializzare con un file o un elemento della shell, archiviare il percorso del file o un riferimento a [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem). Non leggere i dati da queste origini fino a quando non viene chiamato [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) .

In generale, l'inizializzazione non deve eseguire operazioni complesse, ad esempio la composizione e l'archiviazione di un'immagine di anteprima. Per ottimizzare l'efficienza, tale tipo di elaborazione non deve essere eseguita fino a quando non viene chiamata l'anteprima per.

## <a name="preview-handler-data-flow"></a>Flusso di dati del gestore di anteprime

Il flusso di dati nel processo di anteprima segue il percorso generale illustrato qui. L'host può essere considerato come Esplora risorse in Windows Vista o Outlook 2007.

1.  Il gestore di anteprime viene inizializzato, preferibilmente con un flusso.
2.  La finestra di visualizzazione viene passata dall'host al gestore tramite [**IPreviewHandler:: sewindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).
3.  A questo punto, il gestore non deve più eseguire alcuna operazione fino a quando non viene chiamato [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) .
4.  L'anteprima viene visualizzata nel riquadro di lettura tramite una chiamata a [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview).
5.  Le dimensioni della finestra vengono impostate tramite [**IPreviewHandler:: serect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
6.  Quando necessario, la finestra viene ridimensionata tramite [**IPreviewHandler:: serect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
7.  L'anteprima viene scaricata e le relative risorse vengono rilasciate quando non è più necessaria, tramite una chiamata a [**IPreviewHandler:: Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload).

## <a name="debugging-a-preview-handler"></a>Debug di un gestore di anteprime

Se sono state seguite le raccomandazioni per implementare il gestore di anteprime come server in-process, per eseguire il debug del gestore di anteprime, è possibile connettersi a Prevhost.exe. Come indicato in precedenza, tenere presente che potrebbero esistere due istanze di Prevhost.exe, una per i normali processi IL basso e una per quei gestori che hanno rifiutato l'esecuzione come processo IL basso.

Se non si trovano Prevhost.exe nell'elenco dei processi disponibili, è probabile che non sia stato caricato in quel momento. Se si fa clic su un file per un'anteprima, il surrogato viene caricato e dovrebbe essere visualizzato come processo collegabile.

## <a name="providing-your-own-process-for-a-preview-handler"></a>Fornire un processo personalizzato per un gestore di anteprime

Se si desidera forzare la creazione di un nuovo processo per il gestore anziché eseguire nel processo predefinito, creare una nuova sottochiave per il gestore in **AppID** e impostare la relativa voce DllSurrogate su "Prevhost.exe". Usare tale sottochiave **AppID** anziché il valore predefinito Prevhost.exe **AppID**.

Fornendo un nuovo processo, il gestore può evitare l'esecuzione in un processo condiviso come per impostazione predefinita. Questo potrebbe consentire, ad esempio, di verificare la versione specifica del Common Language Runtime (CLR) nel processo. Questa operazione è necessaria se si compila un'implementazione gestita di un gestore di anteprime.

> [!Note]  
> i gestori di anteprime a 32 bit devono usare **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} quando vengono installati nei sistemi operativi a 64 bit.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di gestori di anteprime](building-preview-handlers.md)
</dt> <dt>

[Come registrare un gestore di anteprime](how-to-register-a-preview-handler.md)
</dt> <dt>

[Linee guida per il gestore di anteprime](preview-handler-guidelines.md)
</dt> </dl>

 

 
