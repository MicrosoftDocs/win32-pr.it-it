---
description: Uso di GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Uso di GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529521"
---
# <a name="using-graphedit"></a>Uso di GraphEdit

GraphEdit è disponibile nel Software Development Kit (SDK) di Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).

Il nome dell'applicazione GraphEdit è "graphedt.exe". Dopo aver installato l'SDK, "graphedt.exe" si trova nella directory seguente: \[ programmi \] \\ Microsoft SDK \\ Windows \\ \[ versione \] \\ bin \\ .

Prima di eseguire GraphEdit, usare l'utilità regsvr32 per registrare le seguenti DLL, che si trovano nella stessa directory:

-   proppage.dll
-   evrprop.dll

Queste DLL consentono a GraphEdit di visualizzare le pagine delle proprietà per alcuni dei filtri DirectShow incorporati.

## <a name="build-a-file-playback-graph"></a>Creazione di un grafico per la riproduzione di file

GraphEdit è in grado di creare un grafico di filtro per la riproduzione di file. Questa funzionalità equivale a chiamare il metodo [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) in un'applicazione. Scegliere **rendering file multimediale** dal menu **file** . GraphEdit Visualizza una finestra di dialogo **Apri file** . Selezionare un file multimediale e fare clic su **Apri**. GraphEdit compila un grafico di filtro per riprodurre il file selezionato.

È anche possibile eseguire il rendering di un file multimediale che si trova in un URL. Scegliere **Render URL** dal menu **file** . GraphEdit Visualizza una finestra di dialogo in cui digitare l'URL.

## <a name="build-a-filter-graph"></a>Creare un grafico di filtro

GraphEdit è in grado di creare un grafico di filtro personalizzato, usando uno dei filtri registrati nel sistema. Scegliere **Inserisci filtri** dal menu **grafo** . Viene visualizzata una finestra di dialogo con un elenco dei filtri presenti nel sistema, organizzati in base alla categoria filtro. GraphEdit compila questo elenco dalle informazioni contenute nel registro di sistema. Nella figura seguente viene illustrata la finestra di dialogo.

![quali filtri si desidera inserire?](images/gedit12.png)

Per aggiungere un filtro al grafico, selezionare il nome del filtro e fare clic sul pulsante **Inserisci filtri** oppure fare doppio clic sul nome del filtro. Dopo aver aggiunto i filtri, è possibile connettere due filtri trascinando il mouse dal pin di output di un filtro al pin di input di un altro filtro. Se i pin accettano la connessione, GraphEdit disegna una freccia per connetterli.

![connessione di due filtri](images/gedit-connect.png)

## <a name="run-the-graph"></a>Eseguire il grafo

Una volta creato un grafico di filtro nella modifica del grafo, è possibile eseguire il grafo per verificare se funziona come previsto. Il menu **grafico** contiene i comandi di menu **Riproduci**, **Sospendi** e **Arresta**. Questi comandi richiamano i metodi [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , rispettivamente, [**vengono eseguiti**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**sospesi**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)e [**arrestati**](/windows/desktop/api/Control/nf-control-imediacontrol-stop). La barra degli strumenti di GraphEdit include anche pulsanti per questi comandi:

![pulsanti Sospendi, Riproduci e arresta](images/gedit-toolbar.png)

> [!Note]  
> Il comando GraphEdit **Stop** consente innanzitutto di sospendere il grafico e di cercare il tempo zero (presupponendo che il grafico sia ricercabile). Per la riproduzione di file, questa azione Reimposta la finestra video sul primo fotogramma. Quindi GraphEdit chiama [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).

 

Se il grafico è ricercabile, è possibile cercarlo trascinando la barra del dispositivo di scorrimento visualizzata sotto la barra degli strumenti. Il trascinamento della barra del dispositivo di scorrimento richiama il metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

## <a name="view-property-pages"></a>Visualizzare le pagine delle proprietà

Alcuni filtri supportano le pagine delle proprietà personalizzate, che forniscono un'interfaccia utente per l'impostazione delle proprietà nel filtro. Per visualizzare la pagina delle proprietà di un filtro in GraphEdit, fare clic con il pulsante destro del mouse sul filtro e scegliere **Proprietà** dalla finestra popup. GraphEdit Visualizza una pagina delle proprietà che contiene le finestre delle proprietà definite dal filtro (se presente). Inoltre, GraphEdit include una finestra delle proprietà per ogni pin nel filtro. Le finestre delle proprietà del pin sono definite da GraphEdit, non dal filtro. Se il PIN è connesso, nella finestra delle proprietà Aggiungi viene visualizzato il tipo di supporto per la connessione. In caso contrario, elenca i tipi di supporto preferiti del PIN.

> [!Note]  
> Per usare le pagine delle proprietà predefinite di GraphEdit, è necessario registrare proppage.dll. Questa DLL è disponibile nel Windows SDK. La DLL contiene anche pagine di proprietà aggiuntive per alcuni filtri DirectShow. Queste pagine delle proprietà vengono fornite solo a scopo di debug.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Simulazione della creazione di grafici con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



