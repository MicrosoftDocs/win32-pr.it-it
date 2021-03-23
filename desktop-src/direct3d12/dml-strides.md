---
title: Uso di stride per esprimere il layout di riempimento e memoria
description: I tensori DirectML sono descritti dalle proprietà note come *dimensioni* e dagli *stride* del tensore.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b944b1a2600febe27f209bffcc0e355c6a9fc7db
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548824"
---
# <a name="using-strides-to-express-padding-and-memory-layout"></a>Uso di stride per esprimere il layout di riempimento e memoria

I tensori DirectML &mdash; che sono supportati dai buffer Direct3D 12 &mdash; sono descritti dalle proprietà note come *dimensioni* e dagli *stride* del tensore. Le *dimensioni* del tensore descrivono le dimensioni logiche del tensore. Ad esempio, un tensore 2D potrebbe avere un'altezza di 2 e una larghezza pari a 3. Logicamente, il tensore presenta 6 elementi distinti, sebbene le dimensioni non specifichino il modo in cui tali elementi vengono archiviati in memoria. Gli *stride* del tensore descrivono il layout della memoria fisica degli elementi del tensore.

## <a name="two-dimensional-2d-arrays"></a>Matrici bidimensionali (2D)

Si consideri un tensore 2D con altezza 2 e larghezza 3. i dati sono costituiti da caratteri testuali. In C/C++, questo può essere espresso usando una matrice multidimensionale.

```cpp
constexpr int rows = 2;
constexpr int columns = 3;
char tensor[rows][columns];
tensor[0][0] = 'A';
tensor[0][1] = 'B';
tensor[0][2] = 'C';
tensor[1][0] = 'D';
tensor[1][1] = 'E';
tensor[1][2] = 'F';
```

La visualizzazione logica del tensore precedente viene visualizzata sotto.

```console
A B C
D E F
```

In C/C++, una matrice multidimensionale viene archiviata in ordine riga-principale. In altre parole, gli elementi consecutivi lungo la dimensione Width vengono archiviati in modo contiguo nello spazio di memoria lineare.

Offset:|0|1|2|3|4|5
-|-|-|-|-|-|-
Valore:|A|B|C|D|E|F

Lo *stride* di una dimensione è il numero di elementi da ignorare per poter accedere all'elemento successivo della dimensione. Gli stride esprimono il layout del tensore nella memoria. Con un ordine di riga, lo stride della dimensione Width è sempre 1, poiché gli elementi adiacenti lungo la dimensione vengono archiviati in modo contiguo. Lo stride della dimensione Height dipende dalle dimensioni della dimensione Width; Nell'esempio precedente, la distanza tra gli elementi consecutivi lungo la dimensione Height (ad esempio, a a D) è uguale alla larghezza del tensore (ovvero 3 in questo esempio).

Per illustrare un layout diverso, prendere in considerazione l'ordine delle colonne. In altre parole, gli elementi consecutivi lungo la dimensione Height vengono archiviati in modo contiguo nello spazio di memoria lineare. In questo caso, il stride di altezza è sempre 1 e lo stride della larghezza è 2 (dimensione della dimensione dell'altezza).

Offset:|0|1|2|3|4|5
-|-|-|-|-|-|-
Valore:|A|D|B|E|C|F

## <a name="higher-dimensions"></a>Dimensioni superiori

Quando si tratta di un valore maggiore di due dimensioni, è difficile fare riferimento a un layout come riga-principale o colonna-principale. Quindi, nella parte restante di questo argomento vengono usati termini ed etichette, ad esempio.

- 2D: l'altezza "HW" &mdash; è la dimensione più ordinata (riga-principale).
- 2D: la larghezza "WH" &mdash; è la dimensione più alta (column-major).
- 3D: la profondità "ACS" &mdash; è la dimensione più ordinata, seguita dall'altezza e quindi dalla larghezza.
- 3D: la larghezza "WHD" &mdash; è la dimensione più ordinata, seguita dall'altezza e quindi dalla profondità.
- 4D: "NCHW" &mdash; il numero di immagini (dimensioni batch), il numero di canali, quindi l'altezza e poi la larghezza.

In generale, lo stride *compresso* di una dimensione è uguale al prodotto delle dimensioni delle dimensioni di ordine inferiore. Ad esempio, con un layout "ACS", D-stride è uguale a H * W; lo stride H è uguale a W; e il W-STRIDE è uguale a 1. Si dice che gli stride vengono *compressi* quando la dimensione fisica totale del tensore è uguale alla dimensione logica totale del tensore; in altre parole, non c'è spazio aggiuntivo né elementi sovrapposti.

Si estenderà l'esempio 2D a tre dimensioni, in modo da avere un tensore con profondità 2, altezza 2 e larghezza 3 (per un totale di 12 elementi logici).

```console
A B C
D E F

G H I
J K L
```

Con un layout di "ACS", questo tensore viene archiviato come segue.

Offset:|0|1|2|3|4|5|6|7|8|9|10|11|
-|-|-|-|-|-|-|-|-|-|-|-|-|
Valore:|A|B|C|D|E|F|G|H|I|J|K|L|

- D-stride = Height (2) * Width (3) = 6 (ad esempio la distanza tra "A" e "G").
- H-stride = Width (3) = 3 (ad esempio la distanza tra' A ' è d').
- W-STRIDE = 1 (ad esempio la distanza tra "A" e "B").

Il prodotto a virgola degli indici/coordinate di un elemento e degli stride fornisce l'offset a tale elemento nel buffer. Ad esempio, l'offset dell'elemento H (d = 1, H = 0, w = 1) è 7.

{1, 0, 1} ⋅ {6, 3, 1} = 1 * 6 + 0 * 3 + 1 * 1 = 7

## <a name="packed-tensors"></a>Tensori confezionati

Gli esempi precedenti illustrano i tensori *confezionati* . Si dice che un tensore viene *compresso* quando la dimensione logica del tensore (in elementi) è uguale alla dimensione fisica del buffer (in elementi) e ogni elemento ha un indirizzo/offset univoco. Ad esempio, un tensore 2x2x3 viene compresso se il buffer ha una lunghezza di 12 elementi e nessuna coppia di elementi condivide lo stesso offset nel buffer. I tensori compressi sono i casi più comuni. ma gli stride consentono un layout di memoria più complesso.

## <a name="broadcasting-with-strides"></a>Broadcast con stride

Se le dimensioni del buffer di un tensore (in elementi) sono inferiori al prodotto delle dimensioni logiche, è necessario che sia presente una sovrapposizione di elementi. Il solito caso per questo è noto come *broadcasting*; dove gli elementi di una dimensione sono duplicati di un'altra dimensione. Ad esempio, è ora di rivedere l'esempio 2D. Supponiamo che si desideri un tensore logicamente 2x3, ma la seconda riga è identica alla prima riga. Ecco come appare.

```console
A B C
A B C
```

Questo può essere archiviato come un tensore HW/row-major compresso. Tuttavia, una risorsa di archiviazione più compatta conterrà solo 3 elementi (A, B e C) e utilizzerà uno stride di altezza pari a 0 anziché 3. In questo caso, le dimensioni fisiche del tensore sono 3 elementi, ma la dimensione logica è 6 elementi.

In generale, se lo stride di una dimensione è 0, tutti gli elementi nelle dimensioni di ordine inferiore vengono ripetuti lungo la dimensione broadcast; Se, ad esempio, il tensore è NCHW e C-stride è 0, ogni canale avrà gli stessi valori lungo H e W.

## <a name="padding-with-strides"></a>Riempimento con stride

Un tensore viene detto riempimento *se la* dimensione fisica è maggiore della dimensione minima necessaria per adattarsi ai propri elementi. Quando non sono presenti elementi broadcast o sovrapposti, le dimensioni minime del tensore (in elementi) sono semplicemente il prodotto delle dimensioni. È possibile usare la funzione helper `DMLCalcBufferTensorSize` (vedere le [funzioni helper DirectML](dml-helper-functions.md) per un elenco di tale funzione) per calcolare le dimensioni *minime* del buffer per i tensori DirectML.

Si immagini che un buffer contenga i valori seguenti (gli elementi ' x ' indicano i valori di spaziatura interna).

0|1|2|3|4|5|6|7|8|9|
-|-|-|-|-|-|-|-|-|-|
A|B|C|x|x|D|E|F|x|x

Il tensore imbottito può essere descritto usando un stride di altezza pari a 5 anziché 3. Anziché eseguire un'istruzione per tre elementi per ottenere la riga successiva, il passaggio è 5 elementi (3 elementi *reali* più 2 elementi di riempimento). La spaziatura interna è comune nella grafica del computer, ad esempio, per garantire che un'immagine abbia un allineamento di potenza di due.

```console
A B C
D E F
```

## <a name="directml-buffer-tensor-descriptions"></a>Descrizioni del tensore del buffer DirectML

DirectML può funzionare con un'ampia gamma di layout di tensori fisici, perché la [struttura **DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) dispone di entrambi `Sizes` `Strides` i membri e. Alcune implementazioni di operatori potrebbero essere più efficienti con un layout specifico, quindi non è insolito modificare il modo in cui i dati del tensore vengono archiviati per ottenere prestazioni migliori.

Per la maggior parte degli operatori DirectML sono richiesti i tensori 4D o 5D e l'ordine dei valori di dimensioni e stride è fisso. Correggendo l'ordine dei valori di dimensioni e stride in una descrizione del tensore, è possibile che DirectML induca diversi layout fisici.

**4D**
- [**DML_BUFFER_TENSOR_DESC::**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) sizes = {N-size, C-size, H-size, W-size}
- [**DML_BUFFER_TENSOR_DESC:: Strides**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = {N-stride, C-stride, H-stride, W-STRIDE}

**5D**
- **DML_BUFFER_TENSOR_DESC::** sizes = {N-size, C-size, D-size, H-size, W-size}
- **DML_BUFFER_TENSOR_DESC:: Strides** = {N-stride, C-stride, D-stride, H-stride, W-STRIDE}

Se un operatore DirectML richiede un tensore 4D o 5D, ma i dati effettivi hanno un rango inferiore (ad esempio, 2D), le dimensioni iniziali devono essere riempite con 1s. Ad esempio, un tensore "HW" viene impostato usando **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, H, W}.

Se i dati del tensore sono archiviati in NCHW/NCDHW, non è necessario impostare **DML_BUFFER_TENSOR_DESC:: Strides**, a meno che non si desideri trasmettere o riempire. È possibile impostare il campo Strides su `nullptr` . Tuttavia, se i dati del tensore sono archiviati in un altro layout, ad esempio NHWC, sono necessari stride per esprimere la trasformazione da NCHW a tale layout.

Per un esempio semplice, si consideri la descrizione di un tensore 2D con altezza 3 e larghezza 5.

**NCHW compresso (stride impliciti)**
- **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: stride** = `nullptr`

**NCHW compresso (stride espliciti)**
- N-stride = C-size * H-size * W-size = 1 * 3 * 5 = 15
- C-stride = H-size * W-size = 3 * 5 = 15
- H-stride = W-size = 5
- W-STRIDE = 1
- **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: Strides** = {15, 15, 5, 1}

**NHWC compresso**
- N-stride = H-size * W-size * C-size = 3 * 5 * 1 = 15
- H-stride = W-size * C-size = 5 * 1 = 5
- W-STRIDE = C-size = 1
- C-stride = 1
- **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: Strides** = {15, 1, 5, 1}

## <a name="see-also"></a>Vedi anche

* [Funzioni helper DirectML](dml-helper-functions.md)
* [Struttura DML_BUFFER_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)
