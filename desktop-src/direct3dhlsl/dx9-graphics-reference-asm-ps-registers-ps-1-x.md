---
title: Registri ps_1_1__ps_1_2__ps_1_3__ps_1_4
description: I pixel shader dipendono dai registri per ottenere i dati dei vertici, per restituire dati pixel, per conservare i risultati temporanei durante i calcoli e per identificare le fasi di campionamento della trama.
ms.assetid: ca25a030-b4da-4893-b9f3-e3bb12f18d83
keywords:
- Registri-ps_1_1 ps_1_4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4525b6d3be2e9287f53edc1da0cd2fb188184a69
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473422"
---
# <a name="ps_1_1__ps_1_2__ps_1_3__ps_1_4-registers"></a>PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 registri PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4

I pixel shader dipendono dai registri per ottenere i dati dei vertici, per restituire dati pixel, per conservare i risultati temporanei durante i calcoli e per identificare le fasi di campionamento della trama. Sono disponibili diversi tipi di registri, ognuno con una funzionalità univoca. Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da pixel shader versione 1 \_ X.

Registra i dati per l'uso da parte del pixel shader. I registri sono descritti in modo completo nelle sezioni riportate di seguito.

-   I tipi di registro descrivono i quattro tipi di registri disponibili e i relativi scopi.
-   Il limite della porta di lettura descrive le restrizioni relative all'uso di più registri in un'unica istruzione.
-   Read Only Read Write descrive i registri che possono essere usati per la lettura, la scrittura o entrambi.
-   Intervallo dettagli l'intervallo dei dati del componente.

## <a name="register-types"></a>Tipi di registro



|      |                    | Versioni |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nome | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registro costanti  | 8        | 8    | 8    | 8            |
| r\#  | Registro temporaneo | 2        | 2    | 2    | 6            |
| t\#  | Registro trama   | 4        | 4    | 4    | 6            |
| v\#  | Registro colori     | 2        | 2    | 2    | 2 nella fase 2 |



 

-   I registri costanti contengono dati costanti. I dati possono essere caricati in un registro costante usando [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) oppure possono essere definiti con [def-PS](def---ps.md). I registri costanti non sono utilizzabili dalle istruzioni per l'indirizzo della trama. L'unica eccezione è l'istruzione [texm3x3spec-PS](texm3x3spec---ps.md) , che usa un registro costante per fornire un vettore di occhi.
-   I registri temporanei vengono usati per archiviare i risultati intermedi. R0 funge inoltre da output pixel shader. Il valore in R0 alla fine dello shader è il colore del pixel per lo shader.

    La convalida dello shader avrà esito negativo [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) su qualsiasi shader che tenta di leggere da un registro temporaneo che non è stato scritto da un'istruzione precedente. [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) avrà esito negativo in modo analogo, supponendo che la convalida sia abilitata (non utilizzare D3DXSHADER \_ SKIPVALIDATION).

-   Registri di trama

    Per pixel shader versione 1 \_ 1 a 1 \_ 3, i registri di trama contengono dati di trama o coordinate di trama. Quando si campiona una trama, i dati di trama vengono caricati in un registro di trama. Il campionamento di trama usa coordinate di trama per cercare o campionare un valore di colore in corrispondenza delle coordinate specificate (u, v, w, q) tenendo conto degli attributi dello stato della fase della trama. I dati delle coordinate di trama vengono interpolati dai dati delle coordinate di trama dei vertici ed è associato a una fase di trama specifica. Esiste un'associazione predefinita uno-a-uno tra il numero di fase della trama e l'ordine di dichiarazione delle coordinate di trama. Per impostazione predefinita, il primo set di coordinate di trama definito nel formato vertice è associato alla fase 0 della trama.

    Per queste pixel shader versioni, i registri di trama si comportano come i registri temporanei quando vengono usati da istruzioni aritmetiche.

    Per pixel shader versione 1 \_ 4, i registri di trama (t \# ) contengono dati di coordinate di trama di sola lettura. Ciò significa che il set di coordinate di trama e il numero della fase della trama sono indipendenti l'uno dall'altro. Il numero di fase della trama (da cui eseguire il campionamento di una trama) è determinato dal numero di registro di destinazione (da R0 a R5). Per l'istruzione texld, il set di coordinate di trama è determinato dal registro di origine (T0 a T5), quindi il set di coordinate di trama può essere mappato a qualsiasi fase della trama. Inoltre, il registro di origine (specifica delle coordinate di trama) per texld può anche essere un registro temporaneo (r \# ), nel qual caso il contenuto del registro temporaneo viene usato come coordinate di trama.

-   I registri colori contengono valori di colore per pixel. I valori vengono ottenuti per iterazione per pixel dei valori di colore a tinta unita e speculare nei dati del vertice. Per gli shader pixel shader versione 1 \_ 4, i registri colori sono disponibili solo durante la seconda fase.

    Se la modalità ombreggiatura è impostata su D3DSHADE \_ Flat, l'iterazione di entrambi i colori dei vertici (diffusa e speculare) è disabilitata. Indipendentemente dalla modalità di ombreggiatura, la pipeline verrà ancora iterata dalla pipeline se è abilitata la nebbia dei pixel. Tenere presente che la nebbia viene applicata in un secondo momento nella pipeline rispetto a PixelShader.

    È in genere necessario caricare il registro V0 con i dati di colore con diffusione dei vertici. È anche normale caricare il registro V1 con i dati dei colori speculari del vertice.

    I valori dei dati del colore di input vengono bloccati (saturi) nell'intervallo compreso tra 0 e 1 poiché si tratta dell'intervallo di input valido per i registri colori nel pixel shader.

    I pixel shader hanno accesso in sola lettura ai registri colori. Il contenuto di questi registri è un valore iterato, ma l'iterazione può essere eseguita con una precisione più bassa rispetto alle coordinate di trama.

## <a name="read-port-limit"></a>Limite di lettura della porta

Il limite di lettura della porta specifica il numero di registri diversi di ogni tipo di registro che possono essere utilizzati come registro di origine in un'unica istruzione.



|      |                    | Versioni |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nome | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registro costanti  | 2        | 2    | 2    | 2            |
| r\#  | Registro temporaneo | 2        | 2    | 2    | 3            |
| t\#  | Registro trama   | 2        | 3    | 3    | 1            |
| v\#  | Registro colori     | 2        | 2    | 2    | 2 nella fase 2 |



 

Ad esempio, i registri colori per quasi tutte le versioni hanno un limite di porta di lettura pari a due. Ciò significa che una singola istruzione può usare un massimo di due registri colori diversi (V0 e V1 per l'istanza) come registri di origine. Questo esempio mostra due registri colori usati nella stessa istruzione:


```
mad r0, v1, c2, v0
```



## <a name="read-only-readwrite"></a>Sola lettura, lettura/scrittura

I tipi di registro vengono identificati in base alla funzionalità di sola lettura (RO) o alla funzionalità di lettura/scrittura (RW) nella tabella seguente. I registri di sola lettura possono essere utilizzati solo come registri di origine in un'istruzione. non possono mai essere usati come registro di destinazione.



|      |                    | Versioni |      |      |                    |
|------|--------------------|----------|------|------|--------------------|
| Nome | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4               |
| c\#  | Registro costanti  | RO       | RO   | RO   | RO                 |
| r\#  | Registro temporaneo | LS       | LS   | LS   | LS                 |
| t\#  | Registro trama   | LS       | LS   | LS   | Vedere la nota seguente |
| v\#  | Registro colori     | RO       | RO   | RO   | RO                 |



 

I registri che supportano RW possono essere utilizzati per archiviare i risultati intermedi. Sono inclusi i registri temporanei e i registri di trama per alcune delle versioni dello shader.

> [!Note]  
>
> -   Per pixel shader versione 1 \_ 4, i registri di trama sono ro per le istruzioni di indirizzamento della trama e i registri di trama non possono essere letti né scritti da istruzioni aritmetiche. Inoltre, poiché i registri di trama sono diventati registri delle coordinate di trama, l'accesso RO non è una regressione delle funzionalità precedenti.

 

## <a name="range"></a>Range

L'intervallo è il valore massimo e minimo per i dati di registro. Gli intervalli variano in base al tipo di registro. È possibile eseguire query sugli intervalli per alcuni dei registri dal dispositivo Caps usando [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).



| Nome | Tipo               | Range                                               | Versioni     |
|------|--------------------|-----------------------------------------------------|--------------|
| c\#  | Registro costanti  | da-1 a + 1                                            | Tutte le versioni |
| r\#  | Registro temporaneo | \- Da PixelShader1xMaxValue a + PixelShader1xMaxValue | Tutte le versioni |
| t\#  | Registro trama   | \- Da MaxTextureRepeat a + MaxTextureRepeat           | Tutte le versioni |
| v\#  | Registro colori     | da 0 a 1                                              | Tutte le versioni |



 

Early pixel shader hardware rappresenta i dati nei registri utilizzando un numero a virgola fissa. Questo limita la precisione a un massimo di circa otto bit per la parte frazionaria di un numero. Tenere presente questo aspetto quando si progetta uno shader.

Per pixel shader versione 1 \_ 1 a 1 \_ 3, MaxTextureRepeat deve essere almeno uno. Per 1 \_ 4, MaxTextureRepeat deve essere un minimo di otto.

Per ulteriori informazioni su PixelShader1xMaxValue, vedere [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 