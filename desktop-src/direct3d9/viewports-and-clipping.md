---
description: Concettualmente, un viewport è un rettangolo bidimensionale (2D) in cui viene proiettata una scena 3D.
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: Viewport e ritaglio (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57f64d17f7abf4e370406f984fa50037be6d44e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123342"
---
# <a name="viewports-and-clipping-direct3d-9"></a>Viewport e ritaglio (Direct3D 9)

Concettualmente, un viewport è un rettangolo bidimensionale (2D) in cui viene proiettata una scena 3D. In Direct3D il rettangolo esiste come coordinate all'interno di una superficie Direct3D utilizzata dal sistema come destinazione di rendering. La trasformazione proiezione converte i vertici nel sistema di coordinate usato per il viewport. Un viewport viene usato anche per specificare l'intervallo di valori di profondità in una superficie di destinazione di rendering in cui verrà eseguito il rendering di una scena (in genere da 0,0 a 1,0).

## <a name="the-viewing-frustum"></a>Tronco di visualizzazione

Un tronco di visualizzazione è un volume 3D in una scena posizionata rispetto alla fotocamera del viewport. La forma del volume influiscono sulla modalità di proiezione dei modelli dallo spazio della fotocamera sullo schermo. Il tipo di proiezione più comune, una proiezione prospettica, è responsabile di rendere gli oggetti vicini alla fotocamera più grandi degli oggetti a distanza. Per la visualizzazione della prospettiva, la visualizzazione tronco può essere visualizzata come una piramide, con la fotocamera posizionata in corrispondenza del suggerimento, come illustrato nella figura seguente. Questa piramide è intersecata da un piano di ritaglio anteriore e posteriore. Il volume all'interno della piramide tra i piani di ritaglio anteriore e posteriore è il tronco di visualizzazione. Gli oggetti sono visibili solo quando si trovano in questo volume.

![illustrazione di un frustrum di visualizzazione con un piano di ritaglio anteriore e posteriore](images/frustum.png)

Se si immagina che ci si trova in una stanza scura e si esamina una finestra quadrata, si visualizza un tronco di visualizzazione. In questa analogia, il piano di ritaglio vicino è la finestra e il piano di ritaglio indietro è quello che interrompe la visualizzazione, ovvero il grattacielo lungo la strada, le montagne della distanza o niente. È possibile visualizzare tutti gli elementi all'interno della piramide troncata che inizia dalla finestra e termina con qualsiasi altra operazione che interrompa la visualizzazione.

Il tronco di visualizzazione è definito da FOV (campo di visualizzazione) e dalle distanze dei piani di ritaglio anteriore e posteriore, specificato nelle coordinate z, come illustrato nel diagramma seguente.

![diagramma della tronco di visualizzazione](images/fovdiag.png)

In questo diagramma la variabile D è la distanza tra la camera e l'origine dello spazio definito nell'ultima parte della pipeline Geometry, ovvero la trasformazione visualizzazione. Si tratta dello spazio intorno al quale si organizzano i limiti di visualizzazione tronco. Per informazioni sull'uso di questa variabile D per compilare la matrice di proiezione, vedere la [trasformazione proiezione (Direct3D 9)](projection-transform.md) .

## <a name="viewport-rectangle"></a>Rettangolo viewport

Il rettangolo del viewport viene definito in C++ usando la struttura [**D3DVIEWPORT9**](d3dviewport9.md) . La struttura D3DVIEWPORT9 viene utilizzata con i metodi di manipolazione del viewport seguenti esposti dall'interfaccia IDirect3DDevice9.

-   [**IDirect3DDevice9:: getViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [**IDirect3DDevice9:: seviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

La struttura D3DVIEWPORT9 contiene quattro membri, X, Y, Width e Height, che definiscono l'area della superficie di destinazione di rendering in cui verrà eseguito il rendering di una scena. Questi valori corrispondono al rettangolo di destinazione o al rettangolo del viewport, come illustrato nel diagramma seguente.

![diagramma del rettangolo del viewport](images/destrect.png)

I valori specificati per i membri X, Y, larghezza e altezza sono coordinate dello schermo rispetto all'angolo superiore sinistro della superficie di destinazione di rendering. La struttura definisce due membri aggiuntivi (MinZ e MaxZ) che indicano gli intervalli di profondità in cui verrà eseguito il rendering della scena.

Direct3D presuppone che il volume di ritaglio del viewport sia compreso tra-1,0 e 1,0 in X e da 1,0 a-1,0 in Y. Queste sono le impostazioni utilizzate più spesso dalle applicazioni in passato. È possibile modificare le proporzioni del viewport prima del ritaglio utilizzando la [trasformazione proiezione](projection-transform.md).

> [!Note]  
> MinZ e MaxZ indicano gli intervalli di profondità in cui verrà eseguito il rendering della scena e non vengono usati per il ritaglio. Per la maggior parte delle applicazioni i membri vengono impostati su 0,0 e 1,0 per consentire al sistema di eseguire il rendering nell'intero intervallo di valori di profondità nel buffer di profondità. In alcuni casi, è possibile ottenere effetti speciali utilizzando altri intervalli di profondità. Ad esempio, per eseguire il rendering di una visualizzazione Heads-up in un gioco, è possibile impostare entrambi i valori su 0,0 per forzare il rendering degli oggetti in una scena in primo piano da parte del sistema. in alternativa, è possibile impostare entrambi su 1,0 per eseguire il rendering di un oggetto che deve essere sempre in background.

 

Le dimensioni utilizzate nei membri X, Y, larghezza e altezza della struttura [**D3DVIEWPORT9**](d3dviewport9.md) per un viewport definiscono la posizione e le dimensioni del viewport sulla superficie di destinazione di rendering. Questi valori sono nelle coordinate dello schermo, in relazione all'angolo superiore sinistro della superficie.

Direct3D usa il percorso e le dimensioni del viewport per ridimensionare i vertici in modo da adattarli a una scena sottoposta a rendering nella posizione appropriata sulla superficie di destinazione. Internamente, Direct3D inserisce questi valori nella matrice seguente applicata a ogni vertice.

![equazione della matrice applicata a ogni vertice](images/vpscale.png)

Questa matrice consente di ridimensionare i vertici in base alle dimensioni del viewport e all'intervallo di profondità desiderato e di convertirli nella posizione appropriata sulla superficie di destinazione di rendering. La matrice capovolge anche la coordinata y in modo da riflettere un'origine dello schermo nell'angolo superiore sinistro con y crescente verso il basso. Dopo l'applicazione di questa matrice, i vertici sono ancora omogenei, ovvero sono ancora presenti come \[ vertici x, y, z e w, che \] devono essere convertiti in coordinate non omogenee prima di essere inviati al rasterizzatore.

> [!Note]  
> La matrice di ridimensionamento del viewport incorpora i membri MinZ e MaxZ della struttura [**D3DVIEWPORT9**](d3dviewport9.md) per ridimensionare i vertici in modo da adattarsi all'intervallo di profondità \[ Minz, MaxZ \] . Rappresenta una semantica diversa rispetto alle versioni precedenti di DirectX, in cui tali membri sono stati utilizzati per il ritaglio.

 

> [!Note]  
> Le applicazioni in genere impostano rispettivamente MinZ e MaxZ su 0,0 e 1,0 per provocare il rendering del sistema nell'intero intervallo di profondità. Tuttavia, è possibile usare altri valori per ottenere determinati effetti. Ad esempio, è possibile impostare entrambi i valori su 0,0 per forzare tutti gli oggetti in primo piano o impostare entrambi su 1,0 per eseguire il rendering di tutti gli oggetti in background.

 

## <a name="clearing-a-viewport"></a>Cancellazione di un viewport

La cancellazione del viewport Reimposta il contenuto del rettangolo viewport sulla superficie di destinazione di rendering. Può inoltre cancellare il rettangolo nelle superfici del buffer di profondità e dello stencil.

Usare [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) per cancellare il viewport. Il metodo accetta uno o più rettangoli che definiscono le aree sull'area da cancellare. Impostando il parametro count su 1 e il parametro pRects sull'indirizzo di un singolo rettangolo che copre l'intera area del viewport, l'intero viewport viene cancellato. Un altro modo per cancellare l'intero viewport consiste nell'impostare il parametro pRects su **null** e il parametro count su 0.

È possibile utilizzare [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) per cancellare i bit dello stencil all'interno di un buffer di profondità. È sufficiente impostare il parametro Flags per determinare il funzionamento di **IDirect3DDevice9:: Clear** con la destinazione di rendering e i buffer di profondità o stencil associati. Il \_ flag di destinazione D3DCLEAR cancellerà il viewport usando un colore RGBA arbitrario fornito nell'argomento Color (questo non è il colore del materiale). Il flag D3DCLEAR ZBUFFER cancellerà \_ il buffer di profondità a una profondità arbitraria specificata in Z: 0,0 è la distanza più vicina e 1,0 è il più lontano. Il \_ flag dello stencil D3DCLEAR Reimposta i bit dello stencil sul valore fornito nell'argomento dello stencil. È possibile utilizzare numeri interi compresi tra 0 e 2n-1, dove n è la profondità di bit del buffer dello stencil.

In alcune situazioni, è possibile che venga eseguito il rendering solo in piccole parti della destinazione di rendering e delle superfici del buffer di profondità. I metodi Clear consentono inoltre di cancellare più aree delle superfici in un'unica chiamata. A tale scopo, impostare il parametro count sul numero di rettangoli che si desidera cancellare e specificare l'indirizzo del primo rettangolo in una matrice di rettangoli nel parametro pRects.

## <a name="set-up-the-viewport-for-clipping"></a>Configurare il viewport per il ritaglio

I risultati della matrice di proiezione determinano il volume di ritaglio nello spazio di proiezione come:

-w<sub>c</sub><= x<sub>c</sub><= w<sub>c</sub>

-w<sub>c</sub><= y<sub>c</sub><= w<sub>c</sub>

0 <= z<sub>c</sub><= w<sub>c</sub>

Dove: x, y, z e w rappresentano le coordinate dei vertici dopo l'applicazione della trasformazione di proiezione. Eventuali vertici che includono un componente x, y o z al di fuori di questi intervalli vengono ritagliati, se il ritaglio è abilitato (comportamento predefinito).

Fatta eccezione per i buffer dei vertici, le applicazioni abilitano o disabilitano il ritaglio tramite lo stato di rendering del [**\_ ritaglio D3DRS**](./d3drenderstatetype.md) . Le informazioni di ritaglio per i buffer dei vertici vengono generate durante l'elaborazione. Per altre informazioni, vedere [elaborazione dei vertici delle funzioni (Direct3D 9)](fixed-function-vertex-processing.md) e [elaborazione di vertici programmabili (Direct3D 9)](programmable-vertex-processing.md).

Direct3D non ritaglia i vertici trasformati di una primitiva da un buffer dei vertici a meno che non provenga da [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices). Se si eseguono trasformazioni personalizzate e si ha bisogno di Direct3D per eseguire il ritaglio, è consigliabile non usare i buffer dei vertici. In questo caso, l'applicazione attraversa i dati per trasformarli. Direct3D attraversa i dati una seconda volta per ritagliarli, quindi il driver esegue il rendering dei dati, il che non è efficiente. Quindi, se l'applicazione trasforma i dati, deve anche ritagliare i dati.

Quando il dispositivo riceve i vertici pre-trasformati e illuminati (T&L vertici) che devono essere ritagliati, per eseguire l'operazione di ritaglio i vertici vengono trasformati in uno spazio di ridimensionamento usando le informazioni di RHW e le informazioni del viewport del vertice. Il ritaglio viene quindi eseguito. Non tutti i dispositivi sono in grado di eseguire questo back-Transform per ritagliare i vertici a T&L.

La \_ funzionalità del dispositivo CLIPTLVERTS D3DPMISCCAPS indica se il dispositivo è in grado di ritagliare i vertici T&L. Se questa funzionalità non è impostata, l'applicazione è responsabile del ritaglio dei vertici T&L che intende inviare al dispositivo per il rendering. Il dispositivo è sempre in grado di ritagliare i vertici di T&L nella modalità di elaborazione dei vertici software (indipendentemente dal fatto che il dispositivo sia stato creato in modalità di elaborazione dei vertici software o passato alla modalità di elaborazione dei vertici software).

L'unico requisito per la configurazione dei parametri del viewport per un dispositivo di rendering consiste nell'impostare il volume di ritaglio del viewport. A tale scopo, inizializzare e impostare i valori di ritaglio per il volume di ritaglio e per la superficie di destinazione di rendering. I viewport vengono in genere impostati per eseguire il rendering nell'area completa della superficie di destinazione di rendering, ma questo non è un requisito.

Per ottenere questo risultato in C++, è possibile usare le impostazioni seguenti per i membri della struttura [**D3DVIEWPORT9**](d3dviewport9.md) .


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



Dopo aver impostato i valori nella struttura [**D3DVIEWPORT9**](d3dviewport9.md) , applicare i parametri del viewport al dispositivo chiamando il relativo metodo [**IDirect3DDevice9:: seviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) . L'esempio di codice seguente illustra l'aspetto di questa chiamata.


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



Se la chiamata ha esito positivo, i parametri del viewport vengono impostati e diverranno effettivi la volta successiva che viene chiamato un metodo di rendering. Per apportare modifiche ai parametri del viewport, è sufficiente aggiornare i valori nella struttura [**D3DVIEWPORT9**](d3dviewport9.md) e chiamare di nuovo [**IDirect3DDevice9:: seviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) .

> [!Note]  
> I membri della struttura [**D3DVIEWPORT9**](d3dviewport9.md) MinZ e MaxZ indicano gli intervalli di profondità in cui verrà eseguito il rendering della scena e non vengono usati per il ritaglio. La maggior parte delle applicazioni imposta questi membri su 0,0 e 1,0 per consentire al sistema di eseguire il rendering nell'intero intervallo di valori di profondità nel buffer di profondità. In alcuni casi, è possibile ottenere effetti speciali utilizzando altri intervalli di profondità. Ad esempio, per eseguire il rendering di una visualizzazione Heads-up in un gioco, è possibile impostare entrambi i valori su 0,0 per forzare il rendering degli oggetti in una scena in primo piano da parte del sistema. in alternativa, è possibile impostare entrambi su 1,0 per eseguire il rendering di un oggetto che deve essere sempre in background.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
