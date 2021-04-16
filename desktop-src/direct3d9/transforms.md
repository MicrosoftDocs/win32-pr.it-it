---
description: La parte di Direct3D che inserisce la geometria attraverso la pipeline di geometria della funzione fissa è il motore di trasformazione.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Trasformazioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401339"
---
# <a name="transforms-direct3d-9"></a>Trasformazioni (Direct3D 9)

La parte di Direct3D che inserisce la geometria attraverso la pipeline di geometria della funzione fissa è il motore di trasformazione. Individua il modello e il visualizzatore nel mondo, proietta i vertici per la visualizzazione sullo schermo e taglia i vertici nel viewport. Il motore di trasformazione esegue anche calcoli di illuminazione per determinare i componenti speculari e speculari in ogni vertice.

La pipeline Geometry accetta i vertici come input. Il motore di trasformazione applica le trasformazioni del mondo, della visualizzazione e della proiezione ai vertici, ne ritaglia il risultato e passa tutti gli elementi al rasterizzatore.

All'inizio della pipeline, i vertici di un modello vengono dichiarati in relazione a un sistema di coordinate locale. Si tratta di un'origine locale e di un orientamento. Questo orientamento delle coordinate viene spesso definito spazio del modello e le singole coordinate sono denominate coordinate del modello.

La prima fase della pipeline Geometry trasforma i vertici di un modello dal sistema di coordinate locale a un sistema di coordinate usato da tutti gli oggetti in una scena. Il processo di riorientamento dei vertici è denominato trasformazione mondiale. Questo nuovo orientamento viene comunemente definito spazio globale e ogni vertice nello spazio globale viene dichiarato usando le coordinate internazionali.

Nella fase successiva i vertici che descrivono il mondo 3D sono orientati rispetto alla fotocamera. In altre termini, l'applicazione sceglie un punto di visualizzazione per la scena e le coordinate dello spazio globale vengono rilocate e ruotate intorno alla visualizzazione della fotocamera, trasformando lo spazio mondiale nello spazio della fotocamera. Si tratta della trasformazione visualizzazione.

La fase successiva è la trasformazione di proiezione. In questa parte della pipeline gli oggetti vengono in genere ridimensionati in relazione alla distanza dal visualizzatore per dare l'illusione di profondità a una scena. gli oggetti Close vengono creati per apparire più grandi degli oggetti distanti e così via. Per semplicità, questa documentazione si riferisce allo spazio in cui si trovano i vertici dopo la trasformazione della proiezione come spazio di proiezione. Alcuni libri grafici potrebbero riferirsi allo spazio di proiezione come spazio omogeneo post-prospettiva. Non tutte le trasformazioni di proiezione ridimensionano le dimensioni degli oggetti in una scena. Una proiezione come questa viene talvolta denominata proiezione affine o ortogonale.

Nella parte finale della pipeline, tutti i vertici che non saranno visibili sullo schermo vengono rimossi, in modo che il rasterizzatore non imprenda il tempo necessario per calcolare i colori e l'ombreggiatura per un elemento che non verrà mai visualizzato. Questo processo è detto ritaglio. Dopo il ritaglio, i vertici rimanenti vengono ridimensionati in base ai parametri del viewport e convertiti in coordinate dello schermo. I vertici risultanti, visualizzati sullo schermo quando la scena è rasterizzata, esistono nello spazio dello schermo.

Le trasformazioni vengono utilizzate per convertire la geometria dell'oggetto da uno spazio delle coordinate a un altro. Direct3D usa matrici per eseguire trasformazioni 3D. Questa sezione illustra in che modo le matrici creano trasformazioni 3D, descrive alcuni usi comuni per le trasformazioni e illustra come combinare le matrici per produrre una singola matrice che include più trasformazioni.

-   [Trasformazione globale (Direct3D 9)](world-transform.md) -conversione dallo spazio del modello allo spazio globale
-   [Visualizzazione della trasformazione (Direct3D 9)](view-transform.md) : conversione dallo spazio globale allo spazio di visualizzazione
-   [Trasformazione proiezione (Direct3D 9)](projection-transform.md) -conversione dallo spazio di visualizzazione allo spazio di proiezione

## <a name="matrix-transforms"></a>Trasformazioni con matrice

Nelle applicazioni che funzionano con la grafica 3D, è possibile utilizzare trasformazioni geometriche per eseguire le operazioni seguenti:

-   Esprimere la posizione di un oggetto in relazione a un altro oggetto.
-   Ruotare e ridimensionare gli oggetti.
-   Modificare le posizioni, le direzioni e le prospettive di visualizzazione.

È possibile trasformare qualsiasi punto (x, y, z) in un altro punto (x ', y ', z ') usando una matrice 4x4, come illustrato nella seguente equazione.

![equazione di trasformazione di qualsiasi punto in un altro punto](images/matmult.png)

Eseguire le equazioni seguenti in (x, y, z) e nella matrice per produrre il punto (x ', y ', z ').

![equazioni per il nuovo punto](images/matexpnd.png)

Le trasformazioni più comuni sono la traslazione, la rotazione e il ridimensionamento. È possibile combinare le matrici che producono questi effetti in un'unica matrice per calcolare diverse trasformazioni contemporaneamente. Ad esempio, è possibile compilare una singola matrice per tradurre e ruotare una serie di punti.

Le matrici sono scritte nell'ordine delle colonne di riga. Una matrice che consente di ridimensionare uniformemente i vertici lungo ogni asse, nota come scalabilità uniforme, viene rappresentata dalla matrice seguente usando la notazione matematica.

![equazione di una matrice per la scalabilità uniforme](images/matrix.png)

In C++, Direct3D dichiara le matrici come matrice bidimensionale, usando la struttura [**D3DMATRIX**](d3dmatrix.md) . Nell'esempio seguente viene illustrato come inizializzare una struttura **D3DMATRIX** per fungere da matrice di scala uniforme.


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

L'equazione seguente converte il punto (x, y, z) in un nuovo punto (x ', y ', z ').

![equazione di una matrice di traslazione per un nuovo punto](images/transl8.png)

È possibile creare manualmente una matrice di traslazione in C++. Nell'esempio seguente viene illustrato il codice sorgente per una funzione che crea una matrice per tradurre i vertici.


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



Per praticità, la libreria dell'utilità D3DX fornisce la funzione [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) .

## <a name="scale"></a>Scalabilità

L'equazione seguente consente di ridimensionare il punto (x, y, z) in base ai valori arbitrari nelle direzioni x, y e z a un nuovo punto (x ', y ', z ').

![equazione di una matrice di scala per un nuovo punto](images/matscale.png)

## <a name="rotate"></a>Ruota

Le trasformazioni descritte di seguito sono per i sistemi di coordinate a sinistra, quindi possono essere diverse dalle matrici di trasformazione visualizzate altrove.

L'equazione seguente ruota il punto (x, y, z) intorno all'asse x, producendo un nuovo punto (x ', y ', z ').

![equazione di una matrice di rotazione x per un nuovo punto](images/matxrot.png)

L'equazione seguente ruota il punto intorno all'asse y.

![equazione di una matrice di rotazione y per un nuovo punto](images/matyrot.png)

L'equazione seguente ruota il punto intorno all'asse z.

![equazione di una matrice di rotazione z per un nuovo punto](images/matzrot.png)

In queste matrici di esempio, la lettera greca theta sta per l'angolo di rotazione, in radianti. Gli angoli sono misurati in senso orario quando si osserva lungo l'asse di rotazione verso l'origine.

In un'applicazione C++, usare le funzioni [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)e [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) fornite dalla libreria di utilità D3DX per creare matrici di rotazione. Di seguito è riportato il codice per la funzione **D3DXMatrixRotationX** .


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

Un vantaggio dell'uso delle matrici è che è possibile combinare gli effetti di due o più matrici moltiplicando questi ultimi. Ciò significa che, per ruotare un modello e quindi convertirlo in una determinata posizione, non è necessario applicare due matrici. Si moltiplicano invece le matrici di rotazione e traslazione per produrre una matrice composita che contiene tutti gli effetti. Questo processo, denominato concatenazione di matrici, può essere scritto con la seguente equazione.

![equazione della concatenazione di matrici](images/matrxcat.png)

In questa equazione C è la matrice composta da creare e M ₁ tramite MN sono le singole matrici. Nella maggior parte dei casi, vengono concatenate solo due o tre matrici, ma non esiste alcun limite.

Utilizzare la funzione [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) per eseguire la moltiplicazione di matrici.

L'ordine in cui viene eseguita la moltiplicazione della matrice è fondamentale. La formula precedente riflette la regola da sinistra a destra della concatenazione di matrici. Ovvero gli effetti visibili delle matrici utilizzate per creare una matrice composita vengono eseguiti nell'ordine da sinistra a destra. Nell'esempio seguente viene illustrata una tipica matrice mondiale. Si supponga di creare la matrice globale per uno stereotipo di un disco volante. È probabile che si voglia ruotare il disco volante intorno al centro, ovvero l'asse y dello spazio del modello, e tradurlo in un'altra posizione nella scena. Per ottenere questo risultato, creare prima di tutto una matrice di rotazione, quindi moltiplicarla per una matrice di traslazione, come illustrato nella seguente equazione.

![equazione di rotazione basata su una matrice di rotazione e una matrice di traslazione](images/wrldexpl.png)

In questa formula, R<sub>y</sub> è una matrice per la rotazione sull'asse y e T<sub>w</sub> è una traduzione in una posizione in coordinate internazionali.

L'ordine in cui si moltiplicano le matrici è importante perché, diversamente dalla moltiplicazione di due valori scalari, la moltiplicazione di matrici non è commutativa. La moltiplicazione delle matrici nell'ordine opposto ha l'effetto visivo di tradurre il disco volante nella posizione dello spazio globale e quindi di ruotarlo intorno all'origine globale.

Indipendentemente dal tipo di matrice che si sta creando, tenere presente la regola da sinistra a destra per assicurarsi di ottenere gli effetti previsti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 



