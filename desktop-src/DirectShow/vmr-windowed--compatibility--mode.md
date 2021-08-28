---
description: Modalità finestra VMR (compatibilità)
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: Modalità finestra VMR (compatibilità)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d27a5a115ac87475a27365a0211d93cf18e785983cda12ee338e73b24fb0f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049296"
---
# <a name="vmr-windowed-compatibility-mode"></a>Modalità finestra VMR (compatibilità)

La macchina virtuale è progettata per essere compatibile con tutte le applicazioni DirectShow esistenti. Quando viene usata con un'applicazione esistente, la macchina virtuale opera in modalità finestra con un singolo flusso video, detto anche modalità di compatibilità. Questa modalità viene fornita perché VMR-7 è il renderer predefinito in Windows XP e viene quindi usata automaticamente nelle chiamate ai metodi intelligent [Connessione,](intelligent-connect.md) ad esempio [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Se l'applicazione usa Intelligent Connessione e richiede solo funzionalità di rendering di base, non è necessario alcun codice speciale per eseguire correttamente il rendering con VMR-7 in Windows XP.

VmR-9 viene eseguito anche in modalità finestra/compatibilità per impostazione predefinita. Tuttavia, VMR-9 non è mai il renderer video predefinito. Per usare VMR-9 in un'applicazione, è necessario aggiungerlo in modo esplicito al grafico dei filtri. Per questo motivo, e poiché la modalità senza finestra offre funzionalità migliori rispetto alla modalità finestra, l'uso di VMR-9 in modalità finestra/compatibilità non offre alcun vantaggio particolare.

**Uso di VMR-7 in modalità finestra/compatibilità**

Non è necessaria alcuna programmazione speciale per configurare o controllare VMR-7 in modalità finestra/compatibilità. È sufficiente compilare il grafico dei filtri usando le chiamate standard per la creazione di grafi e VMR-7 usa per impostazione predefinita questa modalità.

In modalità finestra/compatibilità, VMR-7 crea una finestra per visualizzare il video. A tale scopo, carica il componente Gestione finestre, che espone le [**interfacce IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) L'applicazione può eseguire una query su Filter Graph Manager per queste interfacce, esattamente come si farebbe con il filtro del renderer video precedente. Per altre informazioni, vedere [Uso della modalità finestra.](using-windowed-mode.md)

La figura seguente mostra VMR-7 in modalità finestra/compatibilità.

![vmr in modalità di compatibilità](images/vmr-compat-mode.png)

Per garantire il livello massimo di compatibilità, la finestra video ha lo stesso nome di classe di quello creato dal filtro del renderer video precedente e la maggior parte del codice di Window Manager del renderer video precedente viene ancora usato dal vmr. In modalità finestra/compatibilità, la macchina virtuale non usa più risorse di sistema rispetto al renderer video precedente. Poiché VMR-7 ha un solo flusso di input in modalità finestra/compatibilità, non carica i componenti mixer o compositor.

Per impostazione predefinita, la macchina virtuale estende l'immagine per riempire la finestra video. Per mantenere le proporzioni dell'origine, chiamare il metodo [**IVMRAspectRatioControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) con il \_ flag VMR ARMODE \_ LETTER \_ BOX.

> [!Note]  
> Le applicazioni MFC che posizionano la finestra video in una finestra figlio devono definire un gestore di messaggi WM ERASEBKGND vuoto, in caso contrario l'area di visualizzazione video non verrà \_ ridisegnata correttamente.

 

**Uso di VMR-7 in modalità finestra/compatibilità con più Flussi**

In modalità finestra/compatibilità, VMR-7 crea un singolo pin di input per impostazione predefinita e disabilita la modalità di combinazione. Per abilitare la modalità di combinazione, è necessario configurare la macchina virtuale prima di connetterla. Per altre informazioni, vedere [VMR con più Flussi (modalità di combinazione).](vmr-with-multiple-streams--mixing-mode.md) In modalità di combinazione, la macchina virtuale carica i componenti di combinazione e compositor, che richiedono più risorse di sistema.

**Uso di VMR-9 in modalità finestra**

Poiché VMR-9 non è il renderer predefinito, non ha una modalità di compatibilità come tale. Il valore predefinito di VMR-9 è la modalità finestra con quattro pin di input. È possibile usare questa modalità per combinare fino a quattro flussi video. Se è necessario combinare un numero maggiore di flussi, è necessario configurarlo come descritto in VMR con più Flussi (modalità di [combinazione).](vmr-with-multiple-streams--mixing-mode.md) In caso contrario, vmR-9 in modalità finestra si comporta esattamente come VMR-7 in modalità finestra/compatibilità.

 

 



