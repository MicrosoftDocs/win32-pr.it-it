---
description: Domande frequenti su DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: Domande frequenti su DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521794"
---
# <a name="directshow-faq"></a>Domande frequenti su DirectShow

Questo articolo risponde a molte domande frequenti su Microsoft DirectShow.

**Quali sistemi operativi sono supportati da DirectShow?**

DirectShow è disponibile in tutte le versioni supportate di Windows.

**Quante conoscenze COM è necessario programmare con DirectShow?**

Per lo sviluppo di applicazioni, è necessario comprendere le nozioni di base per l'utilizzo di oggetti COM: come crearne un'istanza, accedere alle interfacce che espongono e gestire i conteggi dei riferimenti su tali interfacce. Per lo sviluppo di filtri sono necessarie altre informazioni COM.

**Quali formati sono supportati da DirectShow?**

Vedere [formati supportati in DirectShow](supported-formats-in-directshow.md).

**È disponibile un elenco di compatibilità hardware (HCL) DirectShow?**

No. DirectShow usa le funzionalità hardware Microsoft DirectDraw e Microsoft DirectSound se sono disponibili. Quando non è disponibile hardware speciale, DirectShow USA GDI per creare video e le  \* API multimediali di Wave per riprodurre l'audio.

**Quali lingue è possibile utilizzare per scrivere un'applicazione DirectShow?**

DirectShow è progettato principalmente per lo sviluppo in C++. Un piccolo set di sottoinsiemi dell'API DirectShow viene esposto tramite Visual Basic 6,0; Questa funzionalità è tuttavia deprecata.

**DirectShow sarà sempre accessibile tramite codice gestito?**

Microsoft non prevede l'implementazione di un'API DirectShow gestita.

**Quale compilatore è necessario per lo sviluppo DirectShow?**

Qualsiasi compilatore in grado di generare oggetti Component Object Model (COM) dovrebbe funzionare una volta che l'ambiente del compilatore è stato configurato correttamente.

**In che modo DirectShow è correlato a Microsoft DirectX?**

Internamente, DirectShow usa DirectSound e DirectDraw quando l'hardware lo supporta. I filtri per il renderer video e il mixer sovrapposto utilizzano le superfici DirectDraw 3 e DirectDraw 5. Il video che combina il renderer 7 (solo Windows XP) usa le superfici di DirectDraw 7. Il renderer di video mixing 9 e il renderer video migliorato usano le API Microsoft Direct3D più recenti. Non è necessario usare le altre API DirectX per scrivere un'applicazione DirectShow, sebbene sia possibile combinarle.

**In che modo DirectShow è correlato a Microsoft ActiveMovie?**

ActiveMovie è il nome originale di DirectShow. Il termine ActiveMovie non viene più utilizzato.

**Il codice sorgente per l'utilità GraphEdit è disponibile? È possibile ridistribuire GraphEdit?**

No, l'origine non è disponibile e Graphedt.exe non è ridistribuibile.

**DMOs sostituire i filtri DirectShow?**

Microsoft DirectX Media Objects (DMOs) può essere usato in un'applicazione DirectShow. Per codificatori, decodificatori ed effetti, è consigliabile scrivere un DMO anziché un filtro DirectShow. Nota: se si vuole usare l'accelerazione video DirectX nel decodificatore, è necessario implementarla come filtro. Per altri scopi, un filtro DirectShow potrebbe essere più appropriato. Per altre informazioni su DMOs, vedere [oggetti multimediali DirectX](directx-media-objects.md).

**Sto eseguendo un file di formato AVI con Windows Media Player. Posso ascoltare l'audio, ma sembra che non sia presente alcun video, ma vedo solo il nero. Cosa c'è che non va?**

Probabilmente il file è stato codificato con un codec non presente nel sistema. Anche se il formato di file AVI è comune, è possibile creare file AVI con diversi formati di compressione (codec). Se si prova a riprodurre un file AVI che usa un codec non supportato, è possibile udire il componente audio, ma il video verrà visualizzato come schermata nera oppure il contenuto della schermata rimarrà invariato.

> [!Note]  
> Windows Media Player spesso tenta di scaricare e installare un codec se non è presente nel sistema.

 

**Ricerca per categorie compilare l'applicazione? Quali librerie e file di intestazione sono necessari?**

Vedere [configurazione dell'ambiente di compilazione](setting-up-the-build-environment.md).

**GraphEdit Visualizza numerosi filtri che non sono documentati. Quali sono i filtri?**

GraphEdit enumera tutti i filtri registrati nel sistema in una categoria di filtro. Potrebbero essere inclusi i filtri installati da applicazioni di terze parti o installati da altre tecnologie Microsoft, ad esempio Windows Media o NetMeeting. Inoltre, alcuni filtri DirectShow fungono da wrapper per codec o dispositivi hardware, con ogni codec o dispositivo visualizzato come filtro distinto. Il codec video Microsoft H. 263 viene usato da NetMeeting e non è più supportato in DirectShow. Per altre informazioni, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).

**Si sono verificati problemi durante la creazione del grafico personalizzato a livello di codice.**

Per prima cosa, provare a creare il grafico di filtro con GraphEdit. Questo strumento consente di simulare rapidamente numerose possibilità. GraphEdit è sempre un ottimo punto di partenza per testare il grafo prima di provare a compilarlo con il codice sorgente.

Per ulteriori informazioni sulla creazione di grafici, vedere gli articoli seguenti:

-   [Creazione del grafico di filtro](building-the-filter-graph.md)
-   [Enumerazione di oggetti in un grafico di filtro](enumerating-objects-in-a-filter-graph.md)

**Come è possibile rilevare se DirectShow è installato in un computer specifico?**

Chiamare **CoCreateInstance** per creare un'istanza del gestore del grafo dei filtri. Se la chiamata ha esito positivo, DirectShow viene installato nel computer. Nel codice seguente viene illustrato come eseguire questa operazione:


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



**Ricerca per categorie modificare le impostazioni di un filtro senza visualizzare la pagina delle proprietà?**

La maggior parte dei filtri espone una o più interfacce per l'impostazione delle proprietà nel filtro. Per il filtro in questione, vedere la pagina di riferimento. (Vedere [filtri DirectShow](directshow-filters.md)).

**È possibile testare il filtro con GraphEdit?**

Durante lo sviluppo di un filtro, GraphEdit può essere utile per visualizzare le connessioni tra i filtri. Può inoltre fornire un rapido test della funzionalità di un filtro. Tuttavia, non è concepita come una piattaforma di test affidabile.

**Con quale anello dei privilegi vengono eseguiti i filtri?**

I filtri vengono eseguiti in corrispondenza del Ring 3, sebbene alcuni filtri controllino i dispositivi di streaming eseguiti in corrispondenza dell'anello 0. Per ulteriori informazioni, vedere [come i dispositivi hardware partecipano al grafico dei filtri](how-hardware-devices-participate-in-the-filter-graph.md).

**È necessario usare un debugger del kernel?**

Dipende dal progetto specifico. L'installazione delle librerie di runtime di debug DirectX significa che si stanno installando driver di debug e altri componenti in modalità kernel e che se l'applicazione causa un'asserzione di debug in uno di questi componenti, il computer verrà riavviato automaticamente a meno che non si disponga di un debugger del kernel collegato al processo.

**Quando eseguo l'applicazione nel debugger, si arresta in modo anomalo.**

Alcuni decodificatori sono progettati in modo da non funzionare mentre l'applicazione è collegata al debugger. Provare a eseguire l'applicazione all'esterno del debugger.

**Come \_ funziona la macro GUID define?**

La macro **define \_ GUID** risolve il problema della dichiarazione dei `extern` riferimenti ai valori GUID nel codice sorgente. Si supponga, ad esempio, che il progetto contenga tre file di origine, src1. cpp, src2. cpp e Src3. cpp, e che tutti e tre i file usino un determinato valore GUID definito dall'utente. Il valore GUID deve essere definito esattamente una volta nel progetto e gli altri file di origine devono dichiarare i relativi `extern` riferimenti. Con la macro **Definisci \_ GUID** , è possibile usare lo stesso file di intestazione per entrambi gli scopi. Nel file di intestazione dichiarare il GUID come indicato di seguito:


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



(In questo esempio sono presenti zeri, inserire i valori GUID effettivi). È possibile utilizzare l'utilità Guidgen.exe per creare un nuovo GUID e incollarlo nel file di intestazione nel formato **di \_ GUID Definisci** . Includere il file di intestazione in ogni file di origine che fa riferimento al GUID. In esattamente uno dei file di origine includere il file di intestazione INITGUID. h prima del file di intestazione. Ad esempio:


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



Ogni volta che il file di intestazione INITGUID. h non è incluso, la macro di **Definisci \_ GUID** crea un `extern` riferimento al valore GUID. Quando viene incluso il file di intestazione INITGUID. h, la macro **define \_ GUID** viene ridefinita in modo che **define \_ GUID** crei una dichiarazione di definizione del GUID.

Se non si include Initguid. h in uno dei file di origine, verrà ricevuto un errore di collegamento "simbolo esterno non risolto". Se si include Initguid. h due volte per lo stesso GUID, viene ricevuto un errore di compilazione "ridefinizione; inizializzazione multipla ". Per risolvere questi errori, assicurarsi che Initguid. h sia incluso una sola volta. Inoltre, non includere Initguid. h all'interno di un file di intestazione precompilato, perché in effetti l'intestazione precompilata è inclusa in ogni file di origine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione a DirectShow](introduction-to-directshow.md)
</dt> </dl>

 

 



