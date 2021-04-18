---
description: Questo argomento elenca le categorie comuni di problemi che possono verificarsi durante la scrittura di applicazioni Direct3D e come evitarli.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Risoluzione dei problemi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304359"
---
# <a name="troubleshooting-direct3d-9"></a>Risoluzione dei problemi (Direct3D 9)

Questo argomento elenca le categorie comuni di problemi che possono verificarsi durante la scrittura di applicazioni Direct3D e come evitarli.

## <a name="device-creation"></a>Creazione del dispositivo

Se l'applicazione non riesce durante la creazione del dispositivo, verificare gli errori comuni seguenti.

-   Assicurarsi di controllare le funzionalità del dispositivo, in particolare le profondità di rendering.
-   Esaminare il codice di errore. \_OUTOFVIDEOMEMORY D3DERR è sempre possibile.
-   Usare le librerie di collegamento dinamico (dll) di debug di DirectX ed esaminare i messaggi di output nel debugger.

## <a name="using-lit-vertices"></a>Uso di vertici illuminati

Le applicazioni che usano i vertici illuminati devono disabilitare il motore di illuminazione Direct3D impostando lo \_ stato di rendering dell'illuminazione D3DRS su **false**. Per impostazione predefinita, quando l'illuminazione è abilitata, il sistema imposta il colore per qualsiasi vertice che non contiene un vettore normale a 0 (nero), anche se il vertice di input contiene un valore di colore diverso da zero. Poiché i vertici illuminati non sono, per loro natura, contengono una normale del vertice, le informazioni sui colori passate a Direct3D vengono perse durante il rendering se il motore di illuminazione è abilitato.

Ovviamente, il colore del vertice è importante per qualsiasi applicazione che esegue la propria illuminazione. Per impedire al sistema di imporre i valori predefiniti, assicurarsi di impostare D3DRS \_ Lighting su **false**.

Se l'applicazione è in esecuzione ma non è visibile, verificare gli errori comuni seguenti.

-   Assicurarsi che i triangoli non siano degenerati.
-   Assicurarsi che i triangoli non vengano abbattuti.
-   Assicurarsi che le trasformazioni siano coerenti internamente.
-   Controllare le impostazioni del viewport per assicurarsi che consentano di visualizzare i triangoli.

## <a name="debugging"></a>Debug

Il debug di un'applicazione Direct3D può risultare complesso. Provare le tecniche seguenti, oltre a controllare tutti i valori restituiti, un suggerimento particolarmente importante nella programmazione Direct3D, che dipende da implementazioni hardware molto diverse.

-   Passa a debug di dll.
-   Forzare un dispositivo solo software, disattivando l'accelerazione hardware anche quando è disponibile.
-   Forzare le superfici nella memoria di sistema.
-   Creare un'opzione per l'esecuzione in una finestra, in modo che sia possibile utilizzare un debugger integrato.

La seconda e la terza opzione in questo elenco consentono di evitare il blocco Win16 che può altrimenti causare il blocco del debugger.

Provare anche ad aggiungere le voci seguenti a Win.ini.


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a>Inizializzazione Floating-Point Borland

I compilatori di Borland segnalano eccezioni a virgola mobile in modo non compatibile con Direct3D. Per risolvere questo problema, includere un \_ gestore di eccezioni matherr come il seguente:


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a>Convalida dei parametri

Per motivi di prestazioni, la versione di debug del tempo di esecuzione di Direct3D immediate Mode esegue una maggiore convalida dei parametri rispetto alla versione finale, che talvolta non esegue alcuna convalida. Ciò consente alle applicazioni di eseguire il debug affidabile con il componente runtime di debug più lento prima di utilizzare la versione definitiva più veloce per l'ottimizzazione delle prestazioni e la versione finale.

Sebbene diversi metodi in modalità immediata Direct3D impongano limiti sui valori che possono accettare, questi limiti vengono spesso controllati e applicati solo dalla versione di debug del runtime di esecuzione in modalità immediata Direct3D. Le applicazioni devono essere conformi a questi limiti, oppure possono verificarsi risultati imprevedibili e non desiderabili durante l'esecuzione nella versione finale di Direct3D. Ad esempio, il metodo [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accetta un parametro (primitiveCount) che indica il numero di primitive di cui il metodo eseguirà il rendering. Il metodo può accettare solo valori compresi tra 0 e D3DMAXNUMPRIMITIVES. Nella versione di debug di Direct3D, se si passano più di D3DMAXNUMPRIMITIVES primitive, il metodo ha esito negativo correttamente, stampa un messaggio di errore nel log degli errori e restituisce un valore di errore all'applicazione. Viceversa, se l'applicazione esegue lo stesso errore quando viene eseguita con la versione definitiva del runtime, il comportamento non è definito. Per motivi di prestazioni, il metodo non convalida i parametri, causando un comportamento imprevedibile e completamente situazionale quando non sono validi. In alcuni casi la chiamata potrebbe funzionare e in altri casi potrebbe causare un errore di memoria in Direct3D. Se una chiamata non valida funziona costantemente con una particolare configurazione hardware e una versione di DirectX, non c'è alcuna garanzia che continuerà a funzionare su altro hardware o con versioni successive di DirectX.

Se l'applicazione rileva errori inspiegabili durante l'esecuzione con il file di runtime Direct3D per la vendita al dettaglio, testare la versione di debug e osservare attentamente i casi in cui l'applicazione passa parametri non validi. Usare l'applet del pannello di controllo DirectX, passare al runtime di debug, se necessario, e selezionare l'opzione "Interrompi in D3DError". Questa opzione impone al runtime di usare il metodo DebugBreak di Windows per forzare l'arresto dell'applicazione quando viene rilevato un bug dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 
