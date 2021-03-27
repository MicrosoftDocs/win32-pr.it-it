---
title: Formato BC6H
description: Il formato BC6H è un formato di compressione di trama progettato per supportare spazi dei colori HDR (High Dynamic Range) nei dati di origine.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed4b934df742a4d2c99e20b52b7172b64e598dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047101"
---
# <a name="bc6h-format"></a>Formato BC6H

Il formato BC6H è un formato di compressione di trama progettato per supportare spazi dei colori HDR (High Dynamic Range) nei dati di origine.

-   [Informazioni sul formato BC6H/DXGI \_ \_ BC6H](/windows)
-   [Implementazione di BC6H](#bc6h-implementation)
-   [Decodifica del formato BC6H](#decoding-the-bc6h-format)
-   [Formato dell'endpoint compresso BC6H](#bc6h-compressed-endpoint-format)
-   [Estensione del segno per i valori dell'endpoint](#sign-extension-for-endpoint-values)
-   [Trasforma Inversion per i valori dell'endpoint](#transform-inversion-for-endpoint-values)
-   [Dequantizzazione degli endpoint dei colori](#unquantization-of-color-endpoints)
-   [Argomenti correlati](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a>Informazioni sul formato BC6H/DXGI \_ \_ BC6H

Il formato BC6H offre una compressione di alta qualità per le immagini che utilizzano tre canali di colore HDR, con un valore a 16 bit per ogni canale di colore del valore (16:16:16). Non è disponibile alcun supporto per un canale alfa.

BC6H viene specificato dai valori di enumerazione del formato DXGI seguenti \_ :

-   **DXGI \_ FORMATTARE \_ BC6H con \_ tipo**.
-   **DXGI \_ FORMATTARE \_ BC6H \_ UF16**. Questo formato BC6H non usa un bit di segno nei valori dei canali a virgola mobile a 16 bit.
-   **DXGI \_ FORMATTARE \_ BC6H \_ SF16**. Questo formato BC6H utilizza un bit di segno nei valori dei canali a virgola mobile a 16 bit.

> [!Note]  
> Il formato a virgola mobile a 16 bit per i canali dei colori è spesso definito formato a virgola mobile "metà". Questo formato presenta il layout di bit seguente:
>
> |                       |                                                 |
> |-----------------------|-------------------------------------------------|
> | UF16 (float senza segno) | 5 bit esponente + 11 bit mantissa              |
> | SF16 (float con segno)   | 1 bit di segno + 5 bit esponente + 10 mantissa bit |
>
> 
>
>  

 

Il formato BC6H può essere usato per le risorse di trama [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluse le matrici), Texture3D o TextureCube (incluse le matrici). Analogamente, questo formato si applica a qualsiasi superficie mappa MIP associata a tali risorse.

BC6H usa una dimensione fissa a blocchi di 16 byte (128 bit) e una dimensione del riquadro fissa di Texel 4x4. Come per i formati BC precedenti, le immagini di trama più grandi delle dimensioni del riquadro supportate (4x4) vengono compresse usando più blocchi. Questa identità di indirizzamento si applica anche alle immagini tridimensionali, alle mappe MIP, CubeMaps e alle matrici di trama. Tutti i riquadri immagine devono avere lo stesso formato.

Di seguito sono riportate alcune note importanti sul formato BC6H:

-   BC6H supporta la denormalizzazione a virgola mobile, ma non supporta INF (Infinity) e NaN (non un numero). L'eccezione è la modalità con segno di BC6H (DXGI \_ Format \_ BC6H \_ SF16), che supporta-inf (Infinity negativo). Si noti che questo supporto per-INF è semplicemente un elemento del formato stesso e non è supportato in modo specifico dai codificatori per questo formato. In generale, quando i codificatori incontrano i dati di input INF (positivi o negativi) o NaN, devono \\ convertire i dati nel valore di rappresentazione non inf massimo consentito ed eseguire il mapping di Nan a 0 prima della compressione.
-   BC6H non supporta un canale alfa.
-   Il decodificatore BC6H esegue la decompressione prima di eseguire il filtro della trama.
-   La decompressione di BC6H deve essere leggermente precisa; ovvero, l'hardware deve restituire risultati identici a quelli descritti in questa documentazione.

## <a name="bc6h-implementation"></a>Implementazione di BC6H

Un blocco BC6H è costituito da bit in modalità, endpoint compressi, indici compressi e un indice di partizione facoltativo. Questo formato specifica 14 modalità diverse.

Il colore di un endpoint viene archiviato come tripletta RGB. BC6H definisce una tavolozza di colori su una linea approssimativa tra diversi endpoint di colore definiti. Inoltre, a seconda della modalità, un riquadro può essere suddiviso in due aree o trattato come una singola area, in cui un riquadro a due aree dispone di un set separato di endpoint dei colori per ogni area. BC6H archivia un indice tavolozza per Texel.

Nel caso di due aree sono disponibili 32 partizioni possibili.

## <a name="decoding-the-bc6h-format"></a>Decodifica del formato BC6H

Lo pseudocodice seguente illustra i passaggi per decomprimere il pixel in corrispondenza di (x, y) in base al blocco BC6H a 16 byte.

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

| Modalità | Indici di partizione | Partition | Endpoint colori                  | Bit della modalità      |
|------|-------------------|-----------|----------------------------------|----------------|
| 1    | 46 bit           | 5 bit    | 75 bit (10,555, 10,555, 10,555) | 2 bit (00)    |
| 2    | 46 bit           | 5 bit    | 75 bit (7666, 7666, 7666)       | 2 bit (01)    |
| 3    | 46 bit           | 5 bit    | 72 bit (11,555, 11,444, 11,444) | 5 bit (00010) |
| 4    | 46 bit           | 5 bit    | 72 bit (11,444, 11,555, 11,444) | 5 bit (00110) |
| 5    | 46 bit           | 5 bit    | 72 bit (11,444, 11,444, 11,555) | 5 bit (01010) |
| 6    | 46 bit           | 5 bit    | 72 bit (9555, 9555, 9555)       | 5 bit (01110) |
| 7    | 46 bit           | 5 bit    | 72 bit (8666, 8555, 8555)       | 5 bit (10010) |
| 8    | 46 bit           | 5 bit    | 72 bit (8555, 8666, 8555)       | 5 bit (10110) |
| 9    | 46 bit           | 5 bit    | 72 bit (8555, 8555, 8666)       | 5 bit (11010) |
| 10   | 46 bit           | 5 bit    | 72 bit (6666, 6666, 6666)       | 5 bit (11110) |
| 11   | 63 bit           | 0 bit    | 60 bit (10,10, 10,10, 10,10)    | 5 bit (00011) |
| 12   | 63 bit           | 0 bit    | 60 bit (11,9, 11,9, 11,9)       | 5 bit (00111) |
| 13   | 63 bit           | 0 bit    | 60 bit (12,8, 12,8, 12,8)       | 5 bit (01011) |
| 14   | 63 bit           | 0 bit    | 60 bit (16,4, 16,4, 16,4)       | 5 bit (01111) |



 

Ogni formato in questa tabella può essere identificato in modo univoco dai bit in modalità. Le prime dieci modalità vengono usate per i riquadri a due aree e il campo di bit della modalità può essere lungo due o cinque bit. Questi blocchi hanno anche campi per gli endpoint dei colori compressi (72 o 75 bit), la partizione (5 bit) e gli indici di partizione (46 bit).

Per gli endpoint di colore compressi, i valori della tabella precedente annotano la precisione degli endpoint RGB archiviati e il numero di bit usati per ogni valore di colore. La modalità 3, ad esempio, specifica un livello di precisione dell'endpoint di colore 11 e il numero di bit utilizzati per archiviare i valori Delta degli endpoint trasformati per i colori rosso, blu e verde (5, 4 e 4 rispettivamente). La modalità 10 non utilizza la compressione delta e archivia invece tutti e quattro gli endpoint dei colori in modo esplicito.

Le ultime quattro modalità di blocco vengono usate per i riquadri di un'area, in cui il campo modalità è a 5 bit. Questi blocchi hanno campi per gli endpoint (60 bit) e gli indici compressi (63 bit). La modalità 11 (come la modalità 10) non usa la compressione delta e archivia invece entrambi gli endpoint dei colori in modo esplicito.

Le modalità 10011, 10111, 11011 e 11111 (non visualizzate) sono riservate. Non usarli nel codificatore. Se all'hardware vengono passati blocchi con una di queste modalità, il blocco decompresso risultante deve contenere tutti gli zeri in tutti i canali tranne il canale alfa.

Per BC6H, il canale alfa deve sempre restituire 1,0 indipendentemente dalla modalità.

### <a name="bc6h-partition-set"></a>Set di partizioni BC6H

Sono disponibili 32 set di partizioni possibili per un riquadro a due aree, definiti nella tabella seguente. Ogni blocco 4x4 rappresenta una singola forma.

![tabella dei set di partizioni bc6h](images/bc6h-partition-sets.png)

In questa tabella di set di partizioni, la voce in grassetto e sottolineata è il percorso dell'indice di correzione per il subset 1 (specificato con un bit meno). L'indice di correzione per il subset 0 è sempre indice 0, perché il partizionamento è sempre disposto in modo che l'indice 0 sia sempre nel subset 0. L'ordine della partizione va dalla parte superiore sinistra alla parte inferiore destra, andando verso sinistra verso destra e quindi dall'alto verso il basso.

## <a name="bc6h-compressed-endpoint-format"></a>Formato dell'endpoint compresso BC6H

![campi di bit per i formati di endpoint compressi bc6h](images/bc6h-headers-med.png)

Questa tabella mostra i campi di bit per gli endpoint compressi come funzione del formato dell'endpoint, con ogni colonna che specifica una codifica e ogni riga che specifica un campo di bit. Questo approccio richiede 82 bit per i riquadri a due aree e 65 bit per i riquadri di un'area. Ad esempio, i primi 5 bit per la codifica 1-Region \[ 16 4 \] precedente (in particolare la colonna più a destra) sono bits m \[ 4:0 \] , i 10 bit successivi sono bits RW \[ 9:0 \] e così via con gli ultimi 6 bit che contengono BW \[ 10:15 \] .

I nomi dei campi nella tabella precedente sono definiti come segue:

| Campo | Variabile          |
|-------|-------------------|
| m     | mode              |
| d     | Indice delle forme       |
| RW    | endpt \[ 0 \] . \[0\] |
| RX    | endpt \[ 0 \] . B \[ 0\] |
| Ry    | endpt \[ 1 \] . \[0\] |
| RZ    | endpt \[ 1 \] . B \[ 0\] |
| GW    | endpt \[ 0 \] . \[1\] |
| GX    | endpt \[ 0 \] . B \[ 1\] |
| GY (    | endpt \[ 1 \] . \[1\] |
| GZ    | endpt \[ 1 \] . B \[ 1\] |
| BW    | endpt \[ 0 \] . \[2\] |
| BX    | endpt \[ 0 \] . B \[ 2\] |
| by    | endpt \[ 1 \] . \[2\] |
| BZ    | endpt \[ 1 \] . B \[ 2\] |



 

Endpt \[ i \] , dove i è 0 o 1, fa riferimento rispettivamente al 0A o al primo set di endpoint.

## <a name="sign-extension-for-endpoint-values"></a>Estensione del segno per i valori dell'endpoint

Per i riquadri a due aree sono disponibili quattro valori di endpoint che possono essere firmati come esteso. Endpt \[ 0 \] . Un oggetto è firmato solo se il formato è firmato; gli altri endpoint sono firmati solo se l'endpoint è stato trasformato o se il formato è firmato. Il codice seguente illustra l'algoritmo per estendere il segno dei valori degli endpoint a due aree.

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

Per i riquadri a una regione, il comportamento è lo stesso, ma solo con endpt \[ 1 \] rimosso.

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

## <a name="transform-inversion-for-endpoint-values"></a>Trasforma Inversion per i valori dell'endpoint

Per i riquadri a due aree, la trasformazione applica l'inverso della codifica delle differenze, aggiungendo il valore di base in endpt \[ 0 \] . Un oggetto alle altre tre voci per un totale di 9 operazioni di aggiunta. Nell'immagine seguente il valore di base è rappresentato come "a0" e presenta la massima precisione a virgola mobile. "A1," B0 "e" B1 "sono tutti i Delta calcolati dal valore di ancoraggio e questi valori Delta sono rappresentati con una precisione inferiore. (A0 corrisponde a endpt \[ 0 \] . , B0 corrisponde a endpt \[ 0 \] . B, a1 corrisponde a endpt \[ 1 \] . A e B1 corrisponde a endpt \[ 1 \] . B.

![calcolo dei valori degli endpoint di trasformazione inversione](images/bc6h-transform-inverse.png)

Per i riquadri a una regione è presente un solo offset Delta e pertanto solo 3 operazioni di aggiunta.

Il decompressore deve garantire che i risultati della trasformazione inversa non ridurrà l'overflow della precisione di endpt \[ 0 \] . a. In caso di overflow, i valori risultanti dalla trasformazione inversa devono essere racchiusi nello stesso numero di bit. Se la precisione di a0 è "p" bit, l'algoritmo di trasformazione è:

`B0 = (B0 + A0) & ((1 << p) - 1)`

Per i formati firmati, anche i risultati del calcolo delta devono essere con estensione Sign. Se l'operazione di estensione del segno considera l'estensione di entrambi i segni, dove 0 è positivo e 1 è negativo, l'estensione del segno 0 gestisce il morsetto sopra riportato. In modo analogo, dopo il morsetto precedente, solo un valore pari a 1 (negativo) deve essere firmato come esteso.

## <a name="unquantization-of-color-endpoints"></a>Dequantizzazione degli endpoint dei colori

Considerati gli endpoint non compressi, il passaggio successivo consiste nell'eseguire una dequantizzazione iniziale degli endpoint dei colori. Questa operazione comporta tre passaggi:

-   Un errore di quantizzazione delle tavolozze dei colori
-   Interpolazione delle tavolozze
-   Finalizzazione dell'unquantizzazione

Separando il processo di dequantizzazione in due parti (la dequantità della tavolozza dei colori prima dell'interpolazione e l'imquantizzazione finale dopo l'interpolazione) riduce il numero di operazioni di moltiplicazione richieste rispetto a un processo di unquantizzazione completo prima dell'interpolazione della tavolozza.

Il codice seguente illustra il processo di recupero delle stime dei valori di colore originali a 16 bit e quindi l'uso dei valori di peso forniti per aggiungere 6 valori di colore aggiuntivi alla tavolozza. Viene eseguita la stessa operazione su ogni canale.

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

Nell'esempio di codice successivo viene illustrato il processo di interpolazione, con le osservazioni seguenti:

-   Poiché l'intervallo completo dei valori di colore per la funzione **unquantizzate** (sotto) è compreso tra-32768 e 65535, l'interpolatore viene implementato utilizzando l'aritmetica con segno a 17 bit.
-   Dopo l'interpolazione, i valori vengono passati alla funzione di **\_ unquantizzate Finish** (descritta nel terzo esempio in questa sezione), che applica il ridimensionamento finale.
-   Tutti i decompressori hardware sono necessari per restituire risultati con precisione in bit con queste funzioni.

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

il **termine \_ unquantizzate** viene chiamato dopo l'interpolazione della tavolozza. La funzione **unquantizzate** posticipa il ridimensionamento di 31/32 per la firma di 31/64 per l'oggetto senza segno. Questo comportamento è necessario per ottenere il valore finale in un intervallo di tempo valido (-0x7BFF ~ 0x7BFF) dopo che l'interpolazione della tavolozza è stata completata per ridurre il numero di moltiplicazioni necessarie. **Finish \_ unquantizzate** applica il ridimensionamento finale e restituisce un valore **short senza segno** che viene reinterpretato in **metà**.

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

 

 