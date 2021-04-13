---
description: Modalità a finestra (compatibilità) VMR
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: Modalità a finestra (compatibilità) VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7312274881642d15b844e0fa950f72e52f92db8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561360"
---
# <a name="vmr-windowed-compatibility-mode"></a>Modalità a finestra (compatibilità) VMR

VMR è progettato per essere compatibile con tutte le applicazioni DirectShow esistenti. Quando viene usato con un'applicazione esistente, VMR funziona in modalità finestra con un solo flusso video, detto anche modalità di compatibilità. Questa modalità viene fornita perché VMR-7 è il renderer predefinito in Windows XP e viene quindi usato automaticamente nelle chiamate a metodi di [connessione intelligenti](intelligent-connect.md) , ad esempio [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Se l'applicazione usa la connessione intelligente e richiede solo funzionalità di rendering di base, non è necessario alcun codice speciale per il rendering corretto con VMR-7 in Windows XP.

Per impostazione predefinita, VMR-9 viene eseguito anche in modalità finestra/compatibilità. Tuttavia, VMR-9 non è mai il renderer video predefinito. Per usare VMR-9 in un'applicazione, è necessario aggiungerlo in modo esplicito al grafico dei filtri. Per questo motivo, e poiché la modalità senza finestra offre una funzionalità migliore rispetto alla modalità finestra, non esiste un vantaggio particolare nell'uso di VMR-9 in modalità Windows/Compatibility.

**Uso di VMR-7 in modalità finestra/compatibilità**

Non è necessaria alcuna programmazione speciale per configurare o controllare VMR-7 in modalità Windows/Compatibility. È sufficiente creare il grafico di filtro usando le chiamate di compilazione del grafo standard e VMR-7 per impostazione predefinita su questa modalità.

In modalità di compatibilità con finestra, VMR-7 crea la propria finestra per visualizzare il video. A tale scopo, carica il componente Window Manager, che espone le interfacce [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . L'applicazione può eseguire una query su Filter Graph Manager per queste interfacce, esattamente come si farebbe con il vecchio filtro renderer video. Per altre informazioni, vedere [uso della modalità Window](using-windowed-mode.md).

La figura seguente Mostra VMR-7 in modalità di compatibilità con finestra.

![VMR in modalità di compatibilità](images/vmr-compat-mode.png)

Per garantire il massimo livello di compatibilità, la finestra video ha lo stesso nome di classe di quello creato dal filtro renderer video precedente e la maggior parte del codice di Window Manager dal renderer video precedente è ancora usato da VMR. In modalità di compatibilità con Windows, VMR non utilizza più risorse di sistema rispetto al renderer video precedente. Poiché VMR-7 ha un solo flusso di input in modalità finestra/compatibilità, non carica i componenti mixer o Compositor.

Per impostazione predefinita, VMR estende l'immagine per riempire la finestra del video. Per mantenere le proporzioni dell'origine, chiamare il metodo [**IVMRAspectRatioControl:: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) con il flag della \_ casella della lettera VMR ARMODE \_ \_ .

> [!Note]  
> Le applicazioni MFC che collocano la finestra video in una finestra figlio devono definire un \_ gestore di messaggi WM ERASEBKGND vuoto oppure l'area di visualizzazione del video non viene ridisegnata correttamente.

 

**Uso di VMR-7 in modalità finestra/compatibilità con più flussi**

In modalità di compatibilità con finestra, VMR-7 crea un singolo pin di input per impostazione predefinita e Disabilita la modalità di combinazione. Per abilitare la modalità di combinazione, è necessario configurare il VMR prima di connetterlo. Per altre informazioni, vedere [VMR con più flussi (modalità di combinazione)](vmr-with-multiple-streams--mixing-mode.md). In modalità di combinazione, il VMR carica i componenti di combinazione e compositor, che richiedono più risorse di sistema.

**Uso di VMR-9 in modalità finestra**

Poiché VMR-9 non è il renderer predefinito, non dispone di una modalità di compatibilità di questo tipo. Il valore predefinito di VMR-9 è invece la modalità finestra con quattro pin di input. È possibile usare questa modalità per combinare fino a quattro flussi video. Se è necessario combinare un numero maggiore di flussi, è necessario configurarlo come descritto in [VMR con più flussi (modalità di combinazione)](vmr-with-multiple-streams--mixing-mode.md). In caso contrario, il VMR-9 in modalità finestra si comporta esattamente come VMR-7 in modalità di compatibilità con finestra.

 

 



