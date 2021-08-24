---
title: Formato BC6H
description: Il formato BC6H è un formato di compressione trame progettato per supportare spazi colori HDR (High Dynamic Range) nei dati di origine.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27422e177e98ecdc53b4152ba0514866f5ad75216e9ef789145d1af882a645d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633821"
---
# <a name="bc6h-format"></a>Formato BC6H

Il formato BC6H è un formato di compressione trame progettato per supportare spazi colori HDR (High Dynamic Range) nei dati di origine.

-   [Informazioni su BC6H/DXGI \_ FORMAT \_ BC6H](/windows)
-   [Implementazione di BC6H](#bc6h-implementation)
-   [Decodifica del formato BC6H](#decoding-the-bc6h-format)
-   [Formato dell'endpoint compresso BC6H](#bc6h-compressed-endpoint-format)
-   [Estensione di firma per i valori dell'endpoint](#sign-extension-for-endpoint-values)
-   [Inversione della trasformazione per i valori dell'endpoint](#transform-inversion-for-endpoint-values)
-   [Unquantization of Color Endpoints](#unquantization-of-color-endpoints)
-   [Argomenti correlati](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a>Informazioni su BC6H/DXGI \_ FORMAT \_ BC6H

Il formato BC6H offre una compressione di alta qualità per le immagini che usano tre canali di colori HDR, con un valore a 16 bit per ogni canale di colore del valore (16:16:16). Non è disponibile alcun supporto per un canale alfa.

BC6H è specificato dai valori di enumerazione DXGI \_ FORMAT seguenti:

-   **DXGI \_ FORMAT \_ BC6H \_ TYPELESS**.
-   **DXGI \_ FORMAT \_ BC6H \_ UF16**. Questo formato BC6H non usa un bit di segno nei valori del canale di colore a virgola mobile a 16 bit.
-   **DXGI \_ FORMAT \_ BC6H \_ SF16**. Questo formato BC6H usa un bit di segno nei valori del canale di colore a virgola mobile a 16 bit.

> [!Note]  
> Il formato a virgola mobile a 16 bit per i canali di colore viene spesso definito formato a virgola mobile "metà". Questo formato ha il layout di bit seguente:
>
> |  Formato                     | Layout di bit                                                |
> |-----------------------|-------------------------------------------------|
> | UF16 (float senza segno) | 5 bit esponenti + 11 bit di mantissa              |
> | SF16 (float con segno)   | 1 bit di segno + 5 bit esponenti + 10 bit di mantissa |
>
> 
>
>  

 

Il formato BC6H può essere usato per [le risorse texture Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluse le matrici), Texture3D o TextureCube (incluse le matrici). Analogamente, questo formato si applica a tutte le superfici della mappa MIP associate a queste risorse.

BC6H usa una dimensione di blocco fissa di 16 byte (128 bit) e una dimensione di riquadro fissa di 4x4 texel. Come per i formati BC precedenti, le immagini di trama più grandi delle dimensioni del riquadro supportate (4x4) vengono compresse usando più blocchi. Questa identità di indirizzamento si applica anche a immagini tridimensionali, mappe MIP, mappe cubi e matrici di trame. Tutti i riquadri immagine devono avere lo stesso formato.

Alcune note importanti sul formato BC6H:

-   BC6H supporta la denormalizzazione a virgola mobile, ma non supporta INF (infinito) e NaN (non un numero). L'eccezione è la modalità firmata di BC6H (DXGI \_ FORMAT \_ BC6H \_ SF16), che supporta -INF (infinito negativo). Si noti che questo supporto per -INF è semplicemente un artefatto del formato stesso e non è supportato in modo specifico dai codificatori per questo formato. In generale, quando i codificatori rilevano dati di input INF (positivi o negativi) o NaN, devono convertire tali dati nel valore di rappresentazione non INF massimo consentito ed eseguire il mapping di NaN a 0 prima della \\ compressione.
-   BC6H non supporta un canale alfa.
-   Il decodificatore BC6H esegue la decompressione prima di eseguire il filtro trame.
-   La decompressione BC6H deve essere bit accurata; ciò significa che l'hardware deve restituire risultati identici al decodificatore descritto in questa documentazione.

## <a name="bc6h-implementation"></a>Implementazione di BC6H

Un blocco BC6H è costituito da bit di modalità, endpoint compressi, indici compressi e un indice di partizione facoltativo. Questo formato specifica 14 modalità diverse.

Un colore dell'endpoint viene archiviato come tripletta RGB. BC6H definisce una tavolozza di colori su una linea approssimativa attraverso diversi endpoint di colore definiti. Inoltre, a seconda della modalità, un riquadro può essere suddiviso in due aree o considerato come una singola area, in cui un riquadro a due aree ha un set separato di endpoint di colore per ogni area. BC6H archivia un indice della tavolozza per ogni texel.

Nel caso di due aree, sono presenti 32 partizioni possibili.

## <a name="decoding-the-bc6h-format"></a>Decodifica del formato BC6H

Lo pseudocodice seguente illustra i passaggi per decomprimere il pixel in corrispondenza di (x,y) in base al blocco BC6H a 16 byte.

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

La tabella seguente contiene il numero di bit e i valori per ognuno dei 14 formati possibili per i blocchi BC6H. 

| Mode | Indici di partizione | Partition | Endpoint di colore                  | Bit di modalità      |
|------|-------------------|-----------|----------------------------------|----------------|
| 1    | 46 bit           | 5 bit    | 75 bit (10.555, 10.555, 10.555) | 2 bit (00)    |
| 2    | 46 bit           | 5 bit    | 75 bit (7666, 7666, 7666)       | 2 bit (01)    |
| 3    | 46 bit           | 5 bit    | 72 bit (11.555, 11.444, 11.444) | 5 bit (00010) |
| 4    | 46 bit           | 5 bit    | 72 bit (11.444, 11.555, 11.444) | 5 bit (00110) |
| 5    | 46 bit           | 5 bit    | 72 bit (11.444, 11.444, 11.555) | 5 bit (01010) |
| 6    | 46 bit           | 5 bit    | 72 bit (9555, 9555, 9555)       | 5 bit (01110) |
| 7    | 46 bit           | 5 bit    | 72 bit (8666, 8555, 8555)       | 5 bit (10010) |
| 8    | 46 bit           | 5 bit    | 72 bit (8555, 8666, 8555)       | 5 bit (10110) |
| 9    | 46 bit           | 5 bit    | 72 bit (8555, 8555, 8666)       | 5 bit (11010) |
| 10   | 46 bit           | 5 bit    | 72 bit (6666, 6666, 6666)       | 5 bit (11110) |
| 11   | 63 bit           | 0 bit    | 60 bit (10.10, 10.10, 10.10)    | 5 bit (00011) |
| 12   | 63 bit           | 0 bit    | 60 bit (11.9, 11.9, 11.9)       | 5 bit (00111) |
| 13   | 63 bit           | 0 bit    | 60 bit (12.8, 12.8, 12.8)       | 5 bit (01011) |
| 14   | 63 bit           | 0 bit    | 60 bit (16.4, 16.4, 16.4)       | 5 bit (01111) |



 

Ogni formato in questa tabella può essere identificato in modo univoco dai bit di modalità. Le prime dieci modalità vengono usate per i riquadri a due aree e il campo di bit mode può essere lungo due o cinque bit. Questi blocchi hanno anche campi per gli endpoint dei colori compressi (72 o 75 bit), la partizione (5 bit) e gli indici di partizione (46 bit).

Per gli endpoint dei colori compressi, i valori nella tabella precedente annotano la precisione degli endpoint RGB archiviati e il numero di bit usati per ogni valore di colore. Ad esempio, la modalità 3 specifica un livello di precisione dell'endpoint del colore di 11 e il numero di bit usati per archiviare i valori differenziali degli endpoint trasformati per i colori rosso, blu e verde (rispettivamente 5, 4 e 4). La modalità 10 non usa la compressione differenziale e archivia invece tutti e quattro gli endpoint di colore in modo esplicito.

Le ultime quattro modalità di blocco vengono usate per i riquadri in un'area, in cui il campo mode è a 5 bit. Questi blocchi hanno campi per gli endpoint (60 bit) e gli indici compressi (63 bit). La modalità 11 (come la modalità 10) non usa la compressione differenziale e archivia invece entrambi gli endpoint di colore in modo esplicito.

Le modalità 10011, 10111, 11011 e 11111 (non visualizzate) sono riservate. Non usarli nel codificatore. Se l'hardware viene passato a blocchi con una di queste modalità specificate, il blocco decompresso risultante deve contenere tutti gli zeri in tutti i canali ad eccezione del canale alfa.

Per BC6H, il canale alfa deve sempre restituire 1.0 indipendentemente dalla modalità.

### <a name="bc6h-partition-set"></a>Set di partizioni BC6H

Sono disponibili 32 set di partizioni possibili per un riquadro a due aree e sono definiti nella tabella seguente. Ogni blocco 4x4 rappresenta una singola forma.

![tabella dei set di partizioni bc6h](images/bc6h-partition-sets.png)

In questa tabella di set di partizioni, la voce in grassetto e sottolineata è la posizione dell'indice di correzione per il subset 1 (specificato con un bit in meno). L'indice di correzione per il subset 0 è sempre indice 0, perché il partizionamento è sempre organizzato in modo che l'indice 0 sia sempre nel subset 0. L'ordine delle partizioni va dall'alto a sinistra verso il basso a destra, spostandosi da sinistra a destra e quindi dall'alto verso il basso.

## <a name="bc6h-compressed-endpoint-format"></a>Formato dell'endpoint compresso BC6H

![campi di bit per i formati di endpoint compressi bc6h](images/bc6h-headers-med.png)

Questa tabella mostra i campi di bit per gli endpoint compressi come funzione del formato dell'endpoint, con ogni colonna che specifica una codifica e ogni riga che specifica un campo di bit. Questo approccio richiede 82 bit per i riquadri a due aree e 65 bit per i riquadri in un'area. Ad esempio, i primi 5 bit per la codifica a un'area 16 4 precedente (in particolare la colonna più a destra) sono bit m 4:0, i 10 bit successivi sono bit rw 9:0 e così via con gli ultimi 6 bit contenenti \[ \] \[ \] \[ \] bw \[ 10:15 \] .

I nomi dei campi nella tabella precedente sono definiti come segue:

| Campo | Variabile          |
|-------|-------------------|
| m     | mode              |
| d     | indice delle forme       |
| Rw    | endpt \[ 0 \] . Un \[ valore 0\] |
| Rx    | endpt \[ 0 \] . B \[ 0\] |
| Ry    | endpt \[ 1 \] . Un \[ valore 0\] |
| Rz    | endpt \[ 1 \] . B \[ 0\] |
| Gw    | endpt \[ 0 \] . A \[ 1\] |
| Gx    | endpt \[ 0 \] . B \[ 1\] |
| Gy    | endpt \[ 1 \] . A \[ 1\] |
| Gz    | endpt \[ 1 \] . B \[ 1\] |
| Bw    | endpt \[ 0 \] . A \[ 2\] |
| Bx    | endpt \[ 0 \] . B \[ 2\] |
| by    | endpt \[ 1 \] . A \[ 2\] |
| Bz    | endpt \[ 1 \] . B \[ 2\] |



 

Endpt i , dove i è 0 o 1, fa riferimento rispettivamente al \[ \] 0° o 1° set di endpoint.

## <a name="sign-extension-for-endpoint-values"></a>Estensione della firma per i valori dell'endpoint

Per i riquadri in due aree, sono disponibili quattro valori di endpoint che possono essere firmati estesi. Endpt \[ 0 \] . Un oggetto è firmato solo se il formato è un formato con segno; gli altri endpoint vengono firmati solo se l'endpoint è stato trasformato o se il formato è un formato con segno. Il codice seguente illustra l'algoritmo per l'estensione del segno dei valori dell'endpoint a due aree.

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

Per i riquadri in un'area, il comportamento è lo stesso, solo con endpt \[ 1 \] rimosso.

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a>Inversione della trasformazione per i valori dell'endpoint

Per i riquadri a due aree, la trasformazione applica l'inverso della codifica delle differenze, aggiungendo il valore di base a endpt \[ \] 0. Oggetto per le altre tre voci per un totale di 9 operazioni di aggiunta. Nell'immagine seguente il valore di base è rappresentato come "A0" e ha la precisione a virgola mobile più elevata. "A1", "B0" e "B1" sono tutti delta calcolati dal valore di ancoraggio e questi valori differenziali sono rappresentati con precisione inferiore. (A0 corrisponde a endpt \[ \] 0. A, B0 corrisponde a endpt \[ \] 0. B, A1 corrisponde a endpt \[ \] 1. A e B1 corrispondono a endpt \[ 1 \] .B.

![calcolo dei valori dell'endpoint di inversione della trasformazione](images/bc6h-transform-inverse.png)

Per i riquadri in un'area è presente una sola offset differenziale e quindi solo 3 operazioni di aggiunta.

Il decompressore deve assicurarsi che i risultati della trasformazione inversa non esercitino la precisione di endpt \[ 0 \] .a. In caso di overflow, i valori risultanti dalla trasformazione inversa devono eseguire il wrapping all'interno dello stesso numero di bit. Se la precisione di A0 è "p", l'algoritmo di trasformazione è:

`B0 = (B0 + A0) & ((1 << p) - 1)`

Per i formati firmati, anche i risultati del calcolo differenziale devono essere estesi con segno. Se l'operazione di estensione del segno considera l'estensione di entrambi i segni, dove 0 è positivo e 1 è negativo, l'estensione del segno 0 si occupa della chiusura precedente. In modo equivalente, dopo la chiusura precedente, deve essere esteso solo il valore 1 (negativo).

## <a name="unquantization-of-color-endpoints"></a>Unquantization of Color Endpoints

Dato gli endpoint non compressi, il passaggio successivo consiste nell'eseguire un'iniziale nonquantizzazione degli endpoint di colore. Questa operazione comporta tre passaggi:

-   Nonquantizzazione delle tavolozze dei colori
-   Interpolazione delle tavolozze
-   Finalizzazione nonquantization

La separazione del processo di nonquantizzazione in due parti (un'equivalenza della tavolozza dei colori prima dell'interpolazione e dell'unquantizzazione finale dopo l'interpolazione) riduce il numero di operazioni di moltiplicazione necessarie rispetto a un processo di nonquantizzazione completo prima dell'interpolazione della tavolozza.

Il codice seguente illustra il processo per recuperare stime dei valori di colore originali a 16 bit e quindi usare i valori di peso forniti per aggiungere altri 6 valori di colore alla tavolozza. La stessa operazione viene eseguita su ogni canale.

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

L'esempio di codice successivo illustra il processo di interpolazione, con le osservazioni seguenti:

-   Poiché l'intero intervallo di valori di colore per la funzione **unquantize** (sotto) è compreso tra -32768 e 65535, l'interpolatore viene implementato usando l'aritmetica con segno a 17 bit.
-   Dopo l'interpolazione, i valori vengono passati alla funzione **finish \_ unquantize** (descritta nel terzo esempio in questa sezione), che applica il ridimensionamento finale.
-   Tutti i decompressori hardware sono necessari per restituire risultati accurati in bit con queste funzioni.

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

**finish \_ unquantize viene** chiamato dopo l'interpolazione della tavolozza. La **funzione unquantize** posticipa il ridimensionamento di 31/32 per signed, 31/64 per unsigned. Questo comportamento è necessario per ottenere il valore finale nell'intervallo dimezzamento valido (-0x7BFF ~ 0x7BFF) dopo il completamento dell'interpolazione del riquadro per ridurre il numero di moltiplicazioni necessarie. **finish \_ unquantize applica** il ridimensionamento finale e restituisce un valore **short** senza segno che viene reinterpretato a **metà.**

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compressione dei blocchi di trama in Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 