---
description: Uso di GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Uso di GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f12dd613339680ac22352f4538b7029d8c9cea213c55f66e1986a8d32d0a68ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072160"
---
# <a name="using-graphedit"></a>Uso di GraphEdit

GraphEdit è disponibile in Microsoft Windows Software Development Kit (SDK) ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).

Il nome dell'applicazione GraphEdit è "graphedt.exe". Dopo aver installato l'SDK, "graphedt.exe" si trova nella directory seguente: \[ Programmi Microsoft SDK Windows \] \\ versione \\ Bin \\ \[ \] \\ \\ .

Prima di eseguire GraphEdit, usare l'utilità regsvr32 per registrare le DLL seguenti, che si trovano nella stessa directory:

-   proppage.dll
-   evrprop.dll

Queste DLL consentono a GraphEdit di visualizzare le pagine delle proprietà per alcuni dei filtri DirectShow predefiniti.

## <a name="build-a-file-playback-graph"></a>Creare un file di riproduzione Graph

GraphEdit consente di creare un grafico di filtro per la riproduzione di file. Questa funzionalità equivale a chiamare il metodo [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) in un'applicazione. Scegliere **Esegui** rendering file **multimediale dal** menu File . GraphEdit visualizza una **finestra di dialogo Apri** file. Selezionare un file multimediale e fare clic su **Apri.** GraphEdit crea un grafico di filtro per riprodurre il file selezionato.

È anche possibile eseguire il rendering di un file multimediale che si trova in un URL. Scegliere **URL di** rendering dal menu **File.** GraphEdit visualizza una finestra di dialogo in cui digitare l'URL.

## <a name="build-a-filter-graph"></a>Compilare un filtro Graph

GraphEdit consente di creare un grafo di filtro personalizzato usando uno qualsiasi dei filtri registrati nel sistema. Dal menu **Graph** scegliere **Inserisci filtri**. Verrà visualizzata una finestra di dialogo con un elenco dei filtri nel sistema, organizzati per categoria di filtri. GraphEdit compila questo elenco dalle informazioni nel Registro di sistema. Nella figura seguente viene illustrata la finestra di dialogo .

![quali filtri si desidera inserire?](images/gedit12.png)

Per aggiungere un filtro al grafico, selezionare il  nome del filtro e fare clic sul pulsante Inserisci filtri oppure fare doppio clic sul nome del filtro. Dopo aver aggiunto i filtri, è possibile connettere due filtri trascinando il mouse dal segnaposto di output di un filtro al pin di input di un altro filtro. Se i segnaposto accettano la connessione, GraphEdit disegna una freccia che li connette.

![connessione di due filtri](images/gedit-connect.png)

## <a name="run-the-graph"></a>Eseguire il Graph

Dopo aver creato un grafo di filtro in Graph, è possibile eseguire il grafo per verificare se funziona come previsto. Il menu **Graph** contiene i comandi di menu **Riproduci,** **Sospendi** e **Arresta**. Questi comandi richiamano [**rispettivamente i metodi IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**Run,**](/windows/desktop/api/Control/nf-control-imediacontrol-run) [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) [**e Stop.**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) La barra degli strumenti GraphEdit include anche i pulsanti per questi comandi:

![Pulsanti sospendi, riproduci e arresta](images/gedit-toolbar.png)

> [!Note]  
> Il comando GraphEdit **Stop** sospende innanzitutto il grafico e cerca il tempo zero (presupponendo che il grafico sia ricercabile). Per la riproduzione di file, questa azione reimposta la finestra video sul primo fotogramma. GraphEdit chiama quindi [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).

 

Se il grafico è ricercabile, è possibile cercarlo trascinando la barra del dispositivo di scorrimento visualizzata sotto la barra degli strumenti. Il trascinamento della barra del dispositivo di scorrimento richiama il metodo [**IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

## <a name="view-property-pages"></a>Visualizzare le pagine delle proprietà

Alcuni filtri supportano pagine delle proprietà personalizzate, che forniscono un'interfaccia utente per l'impostazione delle proprietà del filtro. Per visualizzare la pagina delle proprietà di un filtro in GraphEdit, fare clic con il pulsante destro del mouse sul filtro e scegliere **Proprietà** dalla finestra popup. GraphEdit visualizza una pagina delle proprietà che contiene le finestre delle proprietà definite dal filtro (se presenti). GraphEdit include anche una finestra delle proprietà per ogni segnaposto nel filtro. Le finestre delle proprietà di aggiunta sono definite da GraphEdit, non dal filtro. Se il pin è connesso, nella finestra delle proprietà del pin viene visualizzato il tipo di supporto per la connessione. In caso contrario, elenca i tipi di supporti preferiti del segnaposto.

> [!Note]  
> Per usare le pagine delle proprietà incorporate di GraphEdit, è necessario registrare proppage.dll. Questa DLL è disponibile in Windows SDK. La DLL contiene anche pagine delle proprietà aggiuntive per DirectShow filtri. Queste pagine delle proprietà vengono fornite solo a scopo di debug.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Simulazione Graph compilazione con GraphModifica](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



