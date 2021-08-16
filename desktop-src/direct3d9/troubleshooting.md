---
description: Questo argomento elenca le categorie comuni di problemi che possono verificarsi durante la scrittura di applicazioni Direct3D e come prevenirli.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Risoluzione dei problemi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637ac4b43e8947a6011e35ae9a36db7829ed47fd4d5740f93778116e4ee8f9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044079"
---
# <a name="troubleshooting-direct3d-9"></a>Risoluzione dei problemi (Direct3D 9)

Questo argomento elenca le categorie comuni di problemi che possono verificarsi durante la scrittura di applicazioni Direct3D e come prevenirli.

## <a name="device-creation"></a>Creazione del dispositivo

Se l'applicazione non riesce durante la creazione del dispositivo, verificare la presenza degli errori comuni seguenti.

-   Assicurarsi di controllare le funzionalità del dispositivo, in particolare le profondità di rendering.
-   Esaminare il codice di errore. D3DERR \_ OUTOFVIDEOMEMORY è sempre possibile.
-   Usare le librerie a collegamento dinamico (DLL) DirectX di debug ed esaminare i messaggi di output nel debugger.

## <a name="using-lit-vertices"></a>Uso dei vertici accesi

Le applicazioni che usano vertici accesi devono disabilitare il motore di illuminazione Direct3D impostando lo stato di rendering D3DRS \_ LIGHTING su **FALSE.** Per impostazione predefinita, quando l'illuminazione è abilitata, il sistema imposta il colore per qualsiasi vertice che non contiene un vettore normale su 0 (nero), anche se il vertice di input contiene un valore di colore diverso da zero. Poiché i vertici accesi non contengono per loro natura una normale vertice, le informazioni sul colore passate a Direct3D vengono perse durante il rendering se il motore di illuminazione è abilitato.

Ovviamente, il colore dei vertici è importante per qualsiasi applicazione che esegua la propria illuminazione. Per impedire al sistema di imporre i valori predefiniti, assicurarsi di impostare D3DRS \_ LIGHTING su **FALSE.**

Se l'applicazione viene eseguita ma non è visibile nulla, verificare la presenza degli errori comuni seguenti.

-   Assicurarsi che i triangoli non siano degeneri.
-   Assicurarsi che i triangoli non vengano culled.
-   Assicurarsi che le trasformazioni siano coerenti internamente.
-   Controllare le impostazioni del viewport per assicurarsi che consentano la visualizzazione dei triangoli.

## <a name="debugging"></a>Debug

Il debug di un'applicazione Direct3D può essere complesso. Provare le tecniche seguenti, oltre a controllare tutti i valori restituiti, un suggerimento particolarmente importante nella programmazione Direct3D, che dipende da implementazioni hardware molto diverse.

-   Passare alle DLL di debug.
-   Forzare un dispositivo solo software, disattivando l'accelerazione hardware anche quando è disponibile.
-   Forza le superfici nella memoria di sistema.
-   Creare un'opzione da eseguire in una finestra, in modo da poter usare un debugger integrato.

La seconda e la terza opzione di questo elenco consentono di evitare il blocco Win16 che altrimenti potrebbe causare il blocco del debugger.

Provare anche ad aggiungere le voci seguenti a Win.ini.


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a>Inizializzazione Floating-Point Borland

I compilatori di Borland segnalano eccezioni a virgola mobile in un modo incompatibile con Direct3D. Per risolvere questo problema, includere un gestore \_ di eccezioni matherr simile al seguente:


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

Per motivi di prestazioni, la versione di debug della modalità immediata Direct3D esegue una convalida dei parametri maggiore rispetto alla versione definitiva, che talvolta non esegue alcuna convalida. In questo modo le applicazioni possono eseguire un debug affidabile con il componente di run-time di debug più lento prima di usare la versione definitiva più veloce per l'ottimizzazione delle prestazioni e la versione finale.

Anche se diversi metodi della modalità immediata Direct3D impongono limiti ai valori che possono accettare, questi limiti vengono spesso controllati e applicati solo dalla versione di debug del tempo di esecuzione della modalità immediata Direct3D. Le applicazioni devono essere conformi a questi limiti o possono verificarsi risultati imprevisti e indesiderati quando vengono eseguite nella versione definitiva di Direct3D. Ad esempio, il metodo [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accetta un parametro (PrimitiveCount) che indica il numero di primitive di cui il metodo eseguirà il rendering. Il metodo può accettare solo valori compresi tra 0 e D3DMAXNUMPRIMITIVES. Nella versione di debug di Direct3D, se si passano più primitive D3DMAXNUMPRIMITIVES, il metodo ha esito negativo normalmente, stampando un messaggio di errore nel log degli errori e restituisce un valore di errore all'applicazione. Al contrario, se l'applicazione esegue lo stesso errore quando è in esecuzione con la versione definitiva del runtime, il comportamento non è definito. Per motivi di prestazioni, il metodo non convalida i parametri, determinando un comportamento imprevedibile e completamente imprevisto quando non sono validi. In alcuni casi la chiamata potrebbe funzionare e in altri casi potrebbe causare un errore di memoria in Direct3D. Se una chiamata non valida funziona in modo coerente con una particolare configurazione hardware e una versione di DirectX specifica, non è garantito che continuerà a funzionare su altro hardware o con le versioni successive di DirectX.

Se l'applicazione rileva errori inspiegabili durante l'esecuzione con il file di run-time Direct3D finale, testare la versione di debug e cercare attentamente i casi in cui l'applicazione passa parametri non validi. Usare l'applet del pannello di controllo DirectX, passare al runtime di debug se necessario e selezionare l'opzione "Interrompi in D3DError". Questa opzione forza il runtime a usare il Windows DebugBreak per forzare l'arresto dell'applicazione quando viene rilevato un bug dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione Suggerimenti](programming-tips.md)
</dt> </dl>

 

 
