---
description: I gestori di anteprima vengono chiamati quando si seleziona un elemento per visualizzare un'anteprima leggera, ricca e di sola lettura del contenuto del file nel riquadro di lettura della visualizzazione. Questa operazione viene eseguita senza avviare l'applicazione associata del file.
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: Gestori di anteprima e host di anteprima della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ccc6c2a519b4f9646e76a0a0ef4d0d26348e08d114eb9a080aaee09a75b9f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858763"
---
# <a name="preview-handlers-and-shell-preview-host"></a>Gestori di anteprima e host di anteprima della shell

I gestori di anteprima vengono chiamati quando si seleziona un elemento per visualizzare un'anteprima *leggera,* ricca e di sola lettura del contenuto del file nel riquadro di lettura della visualizzazione. Questa operazione viene eseguita senza avviare l'applicazione associata del file.

In questo argomento vengono illustrati gli argomenti seguenti:

-   [Architettura del gestore di anteprima](#preview-handler-architecture)
-   [Opzioni del modello server](#server-model-options)
-   [Inizializzazione](#initialization)
-   [Anteprima dei dati del gestore Flow](#preview-handler-data-flow)
-   [Debug di un gestore di anteprima](#debugging-a-preview-handler)
-   [Fornire un processo personalizzato per un gestore di anteprima](#providing-your-own-process-for-a-preview-handler)
-   [Argomenti correlati](#related-topics)

## <a name="preview-handler-architecture"></a>Architettura del gestore di anteprima

Un gestore di anteprima è un'applicazione ospitata. Gli host includono Windows Explorer in Windows Vista o Microsoft Outlook 2007. Gli host [**implementano IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) come metodo di comunicazione tra il gestore di anteprima e l'host.

Il gestore di anteprima implementa queste interfacce:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (facoltativo)

Il gestore viene chiamato tramite il relativo [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), che restituisce un puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) tramite il quale si richiede a [**un oggetto IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) di interagire con l'host.

## <a name="server-model-options"></a>Opzioni del modello server

I gestori di anteprima eseguono sempre il processo. Esistono due metodi per implementare questa funzionalità:

1.  Un gestore di anteprima può essere compilato come server in-process ma eseguito tramite un host surrogato out-of-process. Questo è il metodo preferito. Il sistema fornisce un host surrogato per questa operazione nel file Prevhost.exe file. I gestori di anteprima compilati da questo metodo non sono compatibili con Outlook 2007 in Windows XP. Tuttavia, questi stessi gestori funzioneranno in Windows Explorer e Outlook 2007 in esecuzione in Windows Vista.
2.  Un gestore di anteprima può essere compilato come server Component Object Model (COM). Questa operazione non è consigliata per diversi motivi. In primo luogo, l'implementazione di un server in-process è più semplice. Ancora più importante, l'implementazione come server in-process offre un maggiore controllo sulla durata dell'oggetto gestore, che consente una pulizia ed efficienza migliori.

Per impostazione predefinita, i gestori di anteprima vengono eseguiti in un processo a basso livello di integrità (IL) per motivi di sicurezza. Facoltativamente, è possibile disabilitare l'esecuzione come processo IL basso impostando il valore seguente nel Registro di sistema. Tuttavia, non è consigliabile eseguire questa operazione. I sistemi potrebbero infine essere configurati per rifiutare qualsiasi processo che non sia a basso livello DI.

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

Gestori di anteprima diversi condividono lo stesso processo per impostazione predefinita. Due istanze di Prevhost.exe possono essere eseguite contemporaneamente. uno per i gestori in esecuzione come processi IL bassi, uno per i gestori che hanno scelto esplicitamente tale comportamento.

## <a name="initialization"></a>Inizializzazione

Come per i gestori di anteprime e proprietà, è consigliabile inizializzare il gestore con un flusso. Se necessario, è possibile inizializzare tramite un file o un elemento, ma i flussi forniscono il modo più sicuro per implementare un gestore. L'inizializzazione tramite un flusso garantisce l'integrità dei file e i vantaggi di stabilità per il sistema di esecuzione del gestore come processo IL basso, ad esempio la protezione del sistema dai sovraccarichi del buffer, la limitazione della posizione in cui un gestore può scrivere informazioni e la limitazione della comunicazione con altre finestre.

Se è necessario inizializzare con un file o un elemento shell, archiviare il percorso del file o un riferimento a [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem). Non leggere i dati da queste origini finché non viene chiamato [**IPreviewHandler::D oPreview.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)

In generale, l'inizializzazione non deve eseguire operazioni pesanti, ad esempio la composizione e l'archiviazione di un'immagine di anteprima. Per un'efficienza ottimale, questo tipo di elaborazione non deve essere eseguita fino a quando non viene chiamata l'anteprima.

## <a name="preview-handler-data-flow"></a>Anteprima dei dati del gestore Flow

Il flusso di dati nel processo di anteprima segue il percorso generale illustrato qui. L'host può essere Windows Explorer in Windows Vista o Outlook 2007.

1.  Il gestore di anteprima viene inizializzato, preferibilmente con un flusso.
2.  La finestra di visualizzazione viene passata dall'host al gestore tramite [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).
3.  A questo punto, il gestore non deve eseguire altre azioni finché non viene chiamato [**IPreviewHandler::D oPreview.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)
4.  L'anteprima viene visualizzata nel riquadro di lettura tramite una chiamata a [**IPreviewHandler::D oPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview).
5.  Le dimensioni della finestra vengono impostate tramite [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
6.  La finestra viene ridimensionata quando necessario tramite [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
7.  L'anteprima viene scaricata e le relative risorse rilasciate quando non è più necessaria, tramite una chiamata a [**IPreviewHandler::Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload).

## <a name="debugging-a-preview-handler"></a>Debug di un gestore di anteprima

Se sono state seguite le raccomandazioni per implementare il gestore di anteprima come server in-process, per eseguire il debug del gestore di anteprima, è possibile connettersi a Prevhost.exe. Come accennato in precedenza, tenere presente che potrebbero essere presenti due istanze di Prevhost.exe, una per i normali processi IL bassi e una per i gestori che hanno scelto esplicitamente di non essere in esecuzione come processo IL basso.

Se non si trova Prevhost.exe nell'elenco dei processi disponibili, è probabile che non sia stato caricato in quel momento. Facendo clic su un file per un'anteprima, il surrogato viene caricato e quindi visualizzato come processo collegabile.

## <a name="providing-your-own-process-for-a-preview-handler"></a>Fornire un processo personalizzato per un gestore di anteprima

Se si vuole forzare la creazione di un nuovo processo per il gestore anziché eseguire nel processo predefinito, creare una nuova sottochiave per il gestore in **AppID** e impostarne la voce DllSurrogate su "Prevhost.exe". Usare la **sottochiave AppID** anziché il valore predefinito Prevhost.exe **AppID**.

Fornendo un nuovo processo, il gestore può evitare l'esecuzione in un processo condiviso come farebbe per impostazione predefinita. Ciò potrebbe consentire, ad esempio, di garantire la versione specifica di Common Language Runtime (CLR) nel processo. Questa operazione è necessaria se si compila un'implementazione gestita di un gestore di anteprima.

> [!Note]  
> I gestori di anteprima a 32 bit devono usare **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} se installati in sistemi operativi a 64 bit.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di gestori di anteprima](building-preview-handlers.md)
</dt> <dt>

[Come registrare un gestore di anteprima](how-to-register-a-preview-handler.md)
</dt> <dt>

[Linee guida per il gestore di anteprima](preview-handler-guidelines.md)
</dt> </dl>

 

 
