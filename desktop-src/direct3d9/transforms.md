---
description: La parte di Direct3D che inserisce la geometria attraverso la pipeline geometry a funzione fissa è il motore di trasformazione.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Trasformazioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5570562c02f2283b869bbb5e60143ed4badac94eb10651b002a89aedf1cd60f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519754"
---
# <a name="transforms-direct3d-9"></a>Trasformazioni (Direct3D 9)

La parte di Direct3D che inserisce la geometria attraverso la pipeline geometry a funzione fissa è il motore di trasformazione. Individua il modello e il visualizzatore nel mondo, proietta i vertici per la visualizzazione sullo schermo e ritaglia i vertici nel viewport. Il motore di trasformazione esegue anche calcoli di illuminazione per determinare i componenti diffusi e speculari in ogni vertice.

La pipeline di geometria accetta i vertici come input. Il motore di trasformazione applica le trasformazioni di mondo, visualizzazione e proiezione ai vertici, ritaglia il risultato e passa tutto al rasterizzatore.

All'inizio della pipeline, i vertici di un modello vengono dichiarati relativi a un sistema di coordinate locale. Si tratta di un'origine locale e di un orientamento. Questo orientamento delle coordinate viene spesso definito spazio del modello e le singole coordinate sono denominate coordinate del modello.

La prima fase della pipeline geometrica trasforma i vertici di un modello dal sistema di coordinate locale a un sistema di coordinate usato da tutti gli oggetti in una scena. Il processo di riorientamento dei vertici è detto trasformazione del mondo. Questo nuovo orientamento viene comunemente definito spazio del mondo e ogni vertice nello spazio mondiale viene dichiarato usando le coordinate globali.

Nella fase successiva, i vertici che descrivono il mondo 3D sono orientati rispetto a una fotocamera. Ciò significa che l'applicazione sceglie un punto di vista per la scena e le coordinate dello spazio del mondo vengono rilocate e ruotate intorno alla visualizzazione della fotocamera, trasformando lo spazio del mondo nello spazio della fotocamera. Questa è la trasformazione della visualizzazione.

La fase successiva è la trasformazione di proiezione. In questa parte della pipeline, gli oggetti vengono in genere ridimensionati in relazione alla distanza dal visualizzatore per dare l'irta di profondità a una scena; Gli oggetti close vengono resi più grandi degli oggetti distanti e così via. Per semplicità, questa documentazione fa riferimento allo spazio in cui i vertici esistono dopo la trasformazione della proiezione come spazio di proiezione. Alcuni libri di grafica possono fare riferimento allo spazio di proiezione come spazio omogeneo post-prospettiva. Non tutte le trasformazioni di proiezione ridimensionano le dimensioni degli oggetti in una scena. Una proiezione come questa viene talvolta chiamata proiezione affine o ortogonale.

Nella parte finale della pipeline vengono rimossi tutti i vertici che non saranno visibili sullo schermo, in modo che il rasterizzatore non prenda tempo per calcolare i colori e l'ombreggiatura per un elemento che non verrà mai visualizzato. Questo processo è detto ritaglio. Dopo il ritaglio, i vertici rimanenti vengono ridimensionati in base ai parametri del viewport e convertiti in coordinate dello schermo. I vertici risultanti, visibili sullo schermo quando la scena è rasterizzata, esistono nello spazio dello schermo.

Le trasformazioni vengono usate per convertire la geometria dell'oggetto da uno spazio delle coordinate a un altro. Direct3D usa matrici per eseguire trasformazioni 3D. In questa sezione viene illustrato come le matrici creano trasformazioni 3D, vengono descritti alcuni usi comuni per le trasformazioni e viene descritto in dettaglio come combinare le matrici per produrre una singola matrice che include più trasformazioni.

-   [World Transform (Direct3D 9):](world-transform.md) conversione dallo spazio del modello allo spazio del mondo
-   [Trasformazione visualizzazione (Direct3D 9):](view-transform.md) conversione dallo spazio del mondo allo spazio di visualizzazione
-   [Trasformazione proiezione (Direct3D 9):](projection-transform.md) conversione dallo spazio di visualizzazione allo spazio di proiezione

## <a name="matrix-transforms"></a>Trasformazioni con matrice

Nelle applicazioni che usano grafica 3D, è possibile usare trasformazioni geometriche per eseguire le operazioni seguenti:

-   Esprimere la posizione di un oggetto rispetto a un altro oggetto.
-   Ruotare e ridimensionare gli oggetti.
-   Modificare le posizioni di visualizzazione, le direzioni e le prospettive.

È possibile trasformare qualsiasi punto (x,y,z) in un altro punto (x', y', z') usando una matrice 4x4, come illustrato nell'equazione seguente.

![equazione di trasformazione di qualsiasi punto in un altro punto](images/matmult.png)

Eseguire le equazioni seguenti su (x, y, z) e sulla matrice per produrre il punto (x', y', z').

![equazioni per il nuovo punto](images/matexpnd.png)

Le trasformazioni più comuni sono traslazione, rotazione e ridimensionamento. È possibile combinare le matrici che producono questi effetti in un'unica matrice per calcolare più trasformazioni contemporaneamente. Ad esempio, è possibile creare una singola matrice per traslare e ruotare una serie di punti.

Le matrici vengono scritte nell'ordine delle colonne di riga. Una matrice che ridimensiona uniformemente i vertici lungo ogni asse, nota come scala uniforme, è rappresentata dalla matrice seguente usando la notazione matematica.

![equazione di una matrice per il ridimensionamento uniforme](images/matrix.png)

In C++, Direct3D dichiara le matrici come matrice bidimensionale, usando la [**struttura D3DMATRIX.**](d3dmatrix.md) L'esempio seguente illustra come inizializzare una **struttura D3DMATRIX** in modo da fungere da matrice di ridimensionamento uniforme.


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a>Traduci

L'equazione seguente converte il punto (x, y, z) in un nuovo punto (x', y', z').

![equazione di una matrice di traslazione per un nuovo punto](images/transl8.png)

È possibile creare manualmente una matrice di traslazione in C++. L'esempio seguente illustra il codice sorgente per una funzione che crea una matrice per convertire i vertici.


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



Per praticità, la libreria di utilità D3DX fornisce la [**funzione D3DXMatrixTranslation.**](d3dxmatrixtranslation.md)

## <a name="scale"></a>Scalabilità

L'equazione seguente ridimensiona il punto (x, y, z) in base a valori arbitrari nelle direzioni x, y e z in un nuovo punto (x', y', z').

![equazione di una matrice di scala per un nuovo punto](images/matscale.png)

## <a name="rotate"></a>Ruota

Le trasformazioni descritte di seguito sono per i sistemi di coordinate mancino e quindi possono essere diverse dalle matrici di trasformazione viste altrove.

L'equazione seguente ruota il punto (x, y, z) intorno all'asse x, producendo un nuovo punto (x', y', z').

![equazione di una matrice di rotazione x per un nuovo punto](images/matxrot.png)

L'equazione seguente ruota il punto intorno all'asse y.

![equazione di una matrice di rotazione y per un nuovo punto](images/matyrot.png)

L'equazione seguente ruota il punto intorno all'asse z.

![equazione di una matrice di rotazione z per un nuovo punto](images/matzrot.png)

In queste matrici di esempio la lettera greco theta sta per l'angolo di rotazione, espresso in radianti. Gli angoli vengono misurati in senso orario quando si guarda lungo l'asse di rotazione verso l'origine.

In un'applicazione C++ usare le funzioni [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)e [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) fornite dalla libreria di utilità D3DX per creare matrici di rotazione. Di seguito è riportato il codice per **la funzione D3DXMatrixRotationX.**


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a>Concatenazione di matrici

Uno dei vantaggi dell'uso delle matrici è che è possibile combinare gli effetti di due o più matrici moltiplicandoli. Ciò significa che, per ruotare un modello e quindi traslarlo in una posizione, non è necessario applicare due matrici. Si moltiplicano invece le matrici di rotazione e traslazione per produrre una matrice composita che contiene tutti i relativi effetti. Questo processo, denominato concatenazione di matrici, può essere scritto con l'equazione seguente.

![equazione di concatenazione di matrici](images/matrxcat.png)

In questa equazione C è la matrice composita da creare e M₁ Mn sono le singole matrici. Nella maggior parte dei casi vengono concatenate solo due o tre matrici, ma non esiste alcun limite.

Usare la [**funzione D3DXMatrixMultiply**](d3dxmatrixmultiply.md) per eseguire la moltiplicazione di matrici.

L'ordine in cui viene eseguita la moltiplicazione della matrice è fondamentale. La formula precedente riflette la regola da sinistra a destra della concatenazione di matrici. Ciò significa che gli effetti visibili delle matrici usate per creare una matrice composita si verificano nell'ordine da sinistra a destra. Nell'esempio seguente viene illustrata una tipica matrice globale. Imagine si sta creando la matrice globale per un disco stereotipo di disco. È probabile che si voglia ruotare il disco intorno al centro, l'asse y dello spazio del modello, e traslarlo in un'altra posizione nella scena. Per ottenere questo effetto, creare prima di tutto una matrice di rotazione e quindi moltiplicarla per una matrice di traslazione, come illustrato nell'equazione seguente.

![equazione di rotazione basata su una matrice di rotazione e una matrice di traslazione](images/wrldexpl.png)

In questa formula R<sub>y è</sub> una matrice per la rotazione intorno all'asse y e T<sub>w</sub> è una traslazione in una posizione nelle coordinate globali.

L'ordine in cui si moltiplicano le matrici è importante perché, a differenza della moltiplicazione di due valori scalari, la moltiplicazione della matrice non è commutativa. La moltiplicazione delle matrici nell'ordine opposto ha l'effetto visivo di tradurre il disco per la posizione nello spazio mondiale e quindi ruotarlo intorno all'origine del mondo.

Indipendentemente dal tipo di matrice che si sta creando, ricordare la regola da sinistra a destra per assicurarsi di ottenere gli effetti previsti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 



