---
description: Concettualmente, un viewport è un rettangolo bidimensionale (2D) in cui viene proiettata una scena 3D.
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: Viewport e ritaglio (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6ed7cd5e5a8a3116c07c5b88f3e665e7ba7de7c6dd1d3cd7bf55f936e60386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068855"
---
# <a name="viewports-and-clipping-direct3d-9"></a>Viewport e ritaglio (Direct3D 9)

Concettualmente, un viewport è un rettangolo bidimensionale (2D) in cui viene proiettata una scena 3D. In Direct3D il rettangolo esiste come coordinate all'interno di una superficie Direct3D che il sistema usa come destinazione di rendering. La trasformazione della proiezione converte i vertici nel sistema di coordinate usato per il viewport. Un viewport viene usato anche per specificare l'intervallo di valori di profondità su una superficie di destinazione di rendering in cui verrà eseguito il rendering di una scena (in genere da 0,0 a 1,0).

## <a name="the-viewing-frustum"></a>Frustum di visualizzazione

Un frustum di visualizzazione è un volume 3D in una scena posizionata rispetto alla fotocamera del viewport. La forma del volume influisce sul modo in cui i modelli vengono proiettati dallo spazio della fotocamera sullo schermo. Il tipo più comune di proiezione, una proiezione prospettica, è responsabile del fatto che gli oggetti vicino alla fotocamera appaiono più grandi degli oggetti in distanza. Per la visualizzazione prospettica, il frustum di visualizzazione può essere visualizzato come una piramide, con la fotocamera posizionata in corrispondenza della punta, come illustrato nella figura seguente. Questa piramide è intersecata da un piano di ritaglio anteriore e posteriore. Il volume all'interno della piramide tra i piani di ritaglio anteriore e posteriore è il frustum di visualizzazione. Gli oggetti sono visibili solo quando sono in questo volume.

![illustrazione di un frustrum di visualizzazione con un piano di ritaglio anteriore e posteriore](images/frustum.png)

Se si supponga di essere in una stanza scura e di guardare attraverso una finestra quadrata, si sta visualizzando un frusto di visualizzazione. In questa analogia, il piano di ritaglio vicino è la finestra e il piano di ritaglio all'indietro è ciò che interrompe infine la visualizzazione: il cielo sulla strada, il cielo in distanza o niente. È possibile visualizzare tutti gli elementi all'interno della piramide troncata che inizia dalla finestra e termina con qualsiasi interruzione della visualizzazione e non è possibile vedere altro.

Il frustum di visualizzazione è definito da fov (campo di visualizzazione) e dalle distanze dei piani di ritaglio anteriore e posteriore, specificate nelle coordinate z, come illustrato nel diagramma seguente.

![diagramma del frustum di visualizzazione](images/fovdiag.png)

In questo diagramma la variabile D è la distanza dalla fotocamera all'origine dello spazio definito nell'ultima parte della pipeline di geometria, la trasformazione di visualizzazione. Questo è lo spazio intorno al quale si organizzano i limiti del frustum di visualizzazione. Per informazioni sull'uso di questa variabile D per compilare la matrice di proiezione, vedere La trasformazione [proiezione (Direct3D 9)](projection-transform.md)

## <a name="viewport-rectangle"></a>Rettangolo del riquadro di visualizzazione

È possibile definire il rettangolo di visualizzazione in C++ usando la [**struttura D3DVIEWPORT9.**](d3dviewport9.md) La struttura D3DVIEWPORT9 viene usata con i metodi di manipolazione del viewport seguenti esposti dall'interfaccia IDirect3DDevice9.

-   [**IDirect3DDevice9::GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

La struttura D3DVIEWPORT9 contiene quattro membri, X, Y, Width, Height, che definiscono l'area della superficie di destinazione di rendering in cui verrà eseguito il rendering di una scena. Questi valori corrispondono al rettangolo di destinazione, o rettangolo del viewport, come illustrato nel diagramma seguente.

![Diagramma del rettangolo di visualizzazione](images/destrect.png)

I valori specificati per i membri X, Y, Width e Height sono coordinate dello schermo relative all'angolo superiore sinistro della superficie di destinazione di rendering. La struttura definisce due membri aggiuntivi (MinZ e MaxZ) che indicano gli intervalli di profondità in cui verrà eseguito il rendering della scena.

Direct3D presuppone che il volume di ritaglio del viewport sia compreso tra -1.0 e 1.0 in X e da 1.0 a -1.0 in Y. Si tratta delle impostazioni usate più spesso dalle applicazioni in passato. È possibile modificare le proporzioni del viewport prima del ritaglio usando la trasformazione [di proiezione](projection-transform.md).

> [!Note]  
> MinZ e MaxZ indicano gli intervalli di profondità in cui verrà eseguito il rendering della scena e non vengono usati per il ritaglio. La maggior parte delle applicazioni imposta questi membri su 0.0 e 1.0 per consentire al sistema di eseguire il rendering dell'intero intervallo di valori di profondità nel buffer di profondità. In alcuni casi, è possibile ottenere effetti speciali usando altri intervalli di profondità. Ad esempio, per eseguire il rendering di una visualizzazione testa a testa in un gioco, è possibile impostare entrambi i valori su 0,0 per forzare il sistema a eseguire il rendering degli oggetti in una scena in primo piano oppure è possibile impostarli entrambi su 1.0 per eseguire il rendering di un oggetto che deve essere sempre in background.

 

Le dimensioni usate nei membri X, Y, Width, Height della struttura [**D3DVIEWPORT9**](d3dviewport9.md) per un viewport definiscono la posizione e le dimensioni del viewport sulla superficie di destinazione di rendering. Questi valori sono in coordinate dello schermo, rispetto all'angolo superiore sinistro della superficie.

Direct3D usa la posizione e le dimensioni del viewport per ridimensionare i vertici per adattare una scena sottoposta a rendering nella posizione appropriata sulla superficie di destinazione. Internamente, Direct3D inserisce questi valori nella matrice seguente applicata a ogni vertice.

![equazione della matrice applicata a ogni vertice](images/vpscale.png)

Questa matrice ridimensiona i vertici in base alle dimensioni del viewport e all'intervallo di profondità desiderato e li converte nella posizione appropriata sulla superficie di destinazione di rendering. La matrice capovolge anche la coordinata y per riflettere un'origine dello schermo nell'angolo superiore sinistro con y che aumenta verso il basso. Dopo l'applicazione di questa matrice, i vertici sono ancora omogenei, ad esempio esistono ancora come vertici x,y,z,w, e devono essere convertiti in coordinate non omogenee prima di essere inviati al \[ \] rasterizzatore.

> [!Note]  
> La matrice di ridimensionamento del viewport incorpora i membri MinZ e MaxZ della struttura [**D3DVIEWPORT9**](d3dviewport9.md) per ridimensionare i vertici in base all'intervallo di profondità \[ MinZ, MaxZ \] . Rappresenta una semantica diversa rispetto alle versioni precedenti di DirectX, in cui questi membri sono stati usati per il ritaglio.

 

> [!Note]  
> Le applicazioni impostano in genere MinZ e MaxZ rispettivamente su 0.0 e 1.0 per fare in modo che il sistema eseeghi il rendering all'intero intervallo di profondità. Tuttavia, è possibile usare altri valori per ottenere determinati effetti. Ad esempio, è possibile impostare entrambi i valori su 0,0 per forzare tutti gli oggetti in primo piano oppure impostare entrambi su 1.0 per eseguire il rendering di tutti gli oggetti in background.

 

## <a name="clearing-a-viewport"></a>Cancellazione di un viewport

La cancellazione del riquadro di visualizzazione reimposta il contenuto del rettangolo di visualizzazione sulla superficie di destinazione del rendering. Può anche cancellare il rettangolo nelle superfici del buffer di profondità e stencil.

Usare [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) per cancellare il viewport. Il metodo accetta uno o più rettangoli che definiscono le aree sulla superficie da cancellare. Se si imposta il parametro Count su 1 e il parametro pRects sull'indirizzo di un singolo rettangolo che copre l'intera area del viewport, l'intero riquadro di visualizzazione verrà cancellato. Un altro modo per cancellare l'intero viewport è impostare il parametro pRects su **NULL** e il parametro Count su 0.

[**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) può essere usato per cancellare i bit degli stencil all'interno di un buffer di profondità. È sufficiente impostare il parametro Flags per determinare il funzionamento **di IDirect3DDevice9::Clear** con la destinazione di rendering ed eventuali buffer di profondità o stencil associati. Il flag D3DCLEAR TARGET cancella il viewport usando un colore RGBA arbitrario specificato nell'argomento Color (non si tratta \_ del colore del materiale). Il flag D3DCLEAR ZBUFFER cancella il buffer di profondità fino a una profondità arbitraria specificata in Z: 0,0 è la distanza più vicina e 1,0 è la più \_ distante. Il flag D3DCLEAR STENCIL reimposta i bit degli stencil sul valore \_ specificato nell'argomento Stencil. È possibile usare numeri interi che vanno da 0 a 2n-1, dove n è la profondità in bit del buffer degli stencil.

In alcune situazioni, il rendering potrebbe essere eseguito solo su piccole parti delle superfici del buffer di profondità e della destinazione di rendering. I metodi chiari consentono anche di cancellare più aree delle superfici in un'unica chiamata. A tale scopo, impostare il parametro Count sul numero di rettangoli da cancellare e specificare l'indirizzo del primo rettangolo in una matrice di rettangoli nel parametro pRects.

## <a name="set-up-the-viewport-for-clipping"></a>Configurare il riquadro di visualizzazione per il ritaglio

I risultati della matrice di proiezione determinano il volume di ritaglio nello spazio di proiezione come:

-w<sub>c</sub><= x<sub>c<</sub> = w<sub>c</sub>

-w<sub>c</sub><= y<sub>c<</sub> = w<sub>c</sub>

0 <= z<sub>c<</sub> = w<sub>c</sub>

Dove: x, y, z e w rappresentano le coordinate dei vertici dopo l'applicazione della trasformazione della proiezione. Tutti i vertici con un componente x, y o z al di fuori di questi intervalli vengono ritagliati, se il ritaglio è abilitato (comportamento predefinito).

Ad eccezione dei buffer dei vertici, le applicazioni abilitano o disabilitano il ritaglio tramite lo stato di rendering [**\_ CLIPPING D3DRS.**](./d3drenderstatetype.md) Le informazioni di ritaglio per i buffer dei vertici vengono generate durante l'elaborazione. Per altre informazioni, vedere [Fixed Function Vertex Processing (Direct3D 9)](fixed-function-vertex-processing.md) e [Programmable Vertex Processing (Direct3D 9) (Elaborazione](programmable-vertex-processing.md)di vertici programmabili (Direct3D 9) ).

Direct3D non ritaglia i vertici trasformati di una primitiva da un buffer dei vertici a meno che non derivi da [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices). Se si stanno eseguendo trasformazioni e si ha bisogno di Direct3D per eseguire il ritaglio, non è consigliabile usare i buffer dei vertici. In questo caso, l'applicazione attraversa i dati per trasformarlo. Direct3D attraversa i dati una seconda volta per ritagliare i dati e quindi il driver esegue il rendering dei dati, il che è inefficiente. Pertanto, se l'applicazione trasforma i dati, è necessario ritagliare anche i dati.

Quando il dispositivo riceve vertici pre-trasformati e accesi (vertici T&L) che devono essere ritagliati, per eseguire l'operazione di ritaglio i vertici vengono nuovamente trasformati nello spazio di ritaglio usando l'omogeneo reciproco w (RHW) del vertice e le informazioni sul viewport. Viene quindi eseguito il ritaglio. Non tutti i dispositivi sono in grado di eseguire questa trasformazione in avanti per ritagliare i vertici T&L.

La funzionalità di dispositivo D3DPMISCCAPS CLIPTLVERTS indica se il dispositivo è in grado di ritagliare t&\_ vertici L. Se questa funzionalità non è impostata, l'applicazione è responsabile del ritaglio dei vertici T&L che intende inviare al dispositivo di cui eseguire il rendering. Il dispositivo è sempre in grado di ritagliare i vertici T&L nella modalità di elaborazione dei vertici software (indipendentemente dal fatto che il dispositivo sia stato creato nella modalità di elaborazione dei vertici software o sia passata alla modalità di elaborazione dei vertici software).

L'unico requisito per la configurazione dei parametri del viewport per un dispositivo di rendering è l'impostazione del volume di ritaglio del viewport. A tale scopo, inizializzare e impostare i valori di ritaglio per il volume di ritaglio e per la superficie di destinazione di rendering. I viewport sono in genere impostati per il rendering nell'intera area della superficie di destinazione di rendering, ma questo non è un requisito.

Per ottenere questo risultato in C++, puoi usare le impostazioni seguenti per i membri della struttura [**D3DVIEWPORT9.**](d3dviewport9.md)


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



Dopo aver impostato i valori [**nella struttura D3DVIEWPORT9,**](d3dviewport9.md) applicare i parametri del viewport al dispositivo chiamando il relativo metodo [**IDirect3DDevice9::SetViewport.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) Nell'esempio di codice seguente viene illustrato l'aspetto di questa chiamata.


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



Se la chiamata ha esito positivo, i parametri del viewport vengono impostati e saranno validi alla successiva chiamata di un metodo di rendering. Per apportare modifiche ai parametri del viewport, è sufficiente aggiornare i valori nella struttura [**D3DVIEWPORT9**](d3dviewport9.md) e chiamare di nuovo [**IDirect3DDevice9::SetViewport.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

> [!Note]  
> I membri della struttura [**D3DVIEWPORT9**](d3dviewport9.md) MinZ e MaxZ indicano gli intervalli di profondità in cui verrà eseguito il rendering della scena e non vengono usati per il ritaglio. La maggior parte delle applicazioni imposta questi membri su 0.0 e 1.0 per consentire al sistema di eseguire il rendering dell'intero intervallo di valori di profondità nel buffer di profondità. In alcuni casi, è possibile ottenere effetti speciali usando altri intervalli di profondità. Ad esempio, per eseguire il rendering di una visualizzazione heads-up in un gioco, è possibile impostare entrambi i valori su 0,0 per forzare il sistema a eseguire il rendering degli oggetti in una scena in primo piano oppure è possibile impostarli entrambi su 1.0 per eseguire il rendering di un oggetto che deve essere sempre in background.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
