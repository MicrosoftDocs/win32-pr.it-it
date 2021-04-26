---
title: ps_1_1__ps_1_2__ps_1_3__ps_1_4 registri
description: I pixel shader dipendono dai registri per ottenere i dati dei vertici, per l'output dei dati pixel, per contenere risultati temporanei durante i calcoli e per identificare le fasi di campionamento delle trame.
ms.assetid: ca25a030-b4da-4893-b9f3-e3bb12f18d83
keywords:
- 'Registri : ps_1_1 per ps_1_4'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 291f78b8bf74a20dfecf4a74ed65173a895bcc1b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998638"
---
# <a name="ps_1_1__ps_1_2__ps_1_3__ps_1_4-registers"></a>ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registri

I pixel shader dipendono dai registri per ottenere i dati dei vertici, per l'output dei dati pixel, per contenere risultati temporanei durante i calcoli e per identificare le fasi di campionamento delle trame. Esistono diversi tipi di registri, ognuno con una funzionalità univoca. Questa sezione contiene informazioni di riferimento per i registri di input e output implementati da pixel shader versione 1 \_ X.

Registra i dati di conservazione per l'uso da parte del pixel shader. I registri sono descritti in modo completo nelle sezioni seguenti.

-   I tipi di registro descrivono i quattro tipi di registri disponibili e i relativi scopi.
-   In Read Port Limit sono dettagliate le restrizioni relative all'uso di più registri in una singola istruzione.
-   Lettura in sola lettura descrive quali registri possono essere usati per la lettura, la scrittura o entrambi.
-   L'intervallo dettaglia l'intervallo dei dati del componente.

## <a name="register-types"></a>Registrare i tipi



|      |                    | Versioni |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nome | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registro costanti  | 8        | 8    | 8    | 8            |
| R\#  | Registro temporaneo | 2        | 2    | 2    | 6            |
| t\#  | Registro trame   | 4        | 4    | 4    | 6            |
| Presso\#  | Registro colori     | 2        | 2    | 2    | 2 nella fase 2 |



 

-   I registri costanti contengono dati costanti. I dati possono essere caricati in un registro costante usando [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) oppure possono essere definiti usando [def - ps](def---ps.md). I registri costanti non sono utilizzabili dalle istruzioni dell'indirizzo di trama. L'unica eccezione è l'istruzione [texm3x3spec - ps,](texm3x3spec---ps.md) che usa un registro costante per fornire un vettore di raggio oculare.
-   I registri temporanei vengono usati per archiviare i risultati intermedi. r0 funge anche da output pixel shader output. Il valore in r0 alla fine dello shader è il colore pixel per lo shader.

    La convalida dello shader avrà esito negativo [**per CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) in qualsiasi shader che tenta di leggere da un registro temporaneo che non è stato scritto da un'istruzione precedente. [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) avrà esito negativo in modo analogo, presupponendo che la convalida sia abilitata (non usare D3DXSHADER \_ SKIPVALIDATION).

-   Registri di trama

    Ad pixel shader versione 1 \_ da 1 a 1 3, i registri delle trame contengono dati di trama \_ o coordinate di trama. I dati della trama vengono caricati in un registro di trama quando viene campionata una trama. Il campionamento trame usa le coordinate della trama per cercare, o campionare, un valore di colore in corrispondenza delle coordinate specificate (u,v,w,q) tenendo conto degli attributi dello stato della fase della trama. I dati delle coordinate della trama vengono interpolati dai dati delle coordinate della trama dei vertici e sono associati a una fase di trama specifica. Esiste un'associazione uno-a-uno predefinita tra il numero della fase della trama e l'ordine di dichiarazione delle coordinate della trama. Per impostazione predefinita, il primo set di coordinate di trama definito nel formato vertice è associato alla fase di trama 0.

    Per queste pixel shader, i registri di trama si comportano esattamente come i registri temporanei quando vengono usati da istruzioni aritmetiche.

    Ad pixel shader versione 1 4, i registri di trama (t ) contengono dati delle coordinate di \_ \# trama di sola lettura. Ciò significa che il set di coordinate della trama e il numero di fase della trama sono indipendenti l'uno dall'altro. Il numero di fase della trama (da cui campionare una trama) è determinato dal numero di registro di destinazione (da r0 a r5). Per l'istruzione texld, il set di coordinate della trama è determinato dal registro di origine (da t0 a t5), quindi il set di coordinate di trama può essere mappato a qualsiasi fase della trama. Inoltre, il registro di origine (che specifica le coordinate della trama) per texld può anche essere un registro temporaneo (r ), nel qual caso il contenuto del registro temporaneo viene usato come coordinate \# di trama.

-   I registri colori contengono valori di colore per pixel. I valori vengono ottenuti dall'iterazione per pixel dei valori di colore diffusi e speculari nei dati dei vertici. Per pixel shader shader versione \_ 1 4, i registri colori sono disponibili solo durante la seconda fase.

    Se la modalità ombreggiatura è impostata su D3DSHADE FLAT, l'iterazione di entrambi i colori dei vertici (diffuse e \_ speculari) è disabilitata. Indipendentemente dalla modalità ombreggiatura, la nebbia verrà comunque iterata dalla pipeline se è abilitata la nebbia pixel. Tenere presente che la nebbia viene applicata in un secondo momento nella pipeline rispetto al pixelshader.

    È comune caricare il registro v0 con i dati sui colori diffusi dei vertici. È anche comune caricare il registro v1 con i dati sui colori speculari dei vertici.

    I valori dei dati dei colori di input vengono definiti (saturati) nell'intervallo compreso tra 0 e 1 perché si tratta dell'intervallo di input valido per i registri colori nel pixel shader.

    I pixel shader hanno accesso in sola lettura ai registri colori. Il contenuto di questi registri è un valore iterato, ma l'iterazione può essere eseguita a una precisione molto inferiore rispetto alle coordinate della trama.

## <a name="read-port-limit"></a>Limite di porte di lettura

Il limite di porte di lettura specifica il numero di registri diversi di ogni tipo di registro che possono essere usati come registro di origine in una singola istruzione.



|      |                    | Versioni |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nome | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registro costanti  | 2        | 2    | 2    | 2            |
| R\#  | Registro temporaneo | 2        | 2    | 2    | 3            |
| t\#  | Registro delle trame   | 2        | 3    | 3    | 1            |
| Presso\#  | Registro colori     | 2        | 2    | 2    | 2 nella fase 2 |



 

Ad esempio, i registri colori per quasi tutte le versioni hanno un limite di porte di lettura di due. Ciò significa che una singola istruzione può usare un massimo di due registri colori diversi (v0 e v1, ad esempio) come registri di origine. Questo esempio mostra due registri colori usati nella stessa istruzione:


```
mad r0, v1, c2, v0
```



## <a name="read-only-readwrite"></a>Sola lettura, Lettura/Scrittura

I tipi di registro vengono identificati in base alla funzionalità di sola lettura (RO) o alla funzionalità di lettura/scrittura (RW) nella tabella seguente. I registri di sola lettura possono essere usati solo come registri di origine in un'istruzione . non possono mai essere usati come registro di destinazione.



|      |                    | Versioni |      |      |                    |
|------|--------------------|----------|------|------|--------------------|
| Nome | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4               |
| c\#  | Registro delle costanti  | RO       | RO   | RO   | RO                 |
| R\#  | Registro temporaneo | LS       | LS   | LS   | LS                 |
| t\#  | Registro delle trame   | LS       | LS   | LS   | Vedere la nota seguente |
| Presso\#  | Registro colori     | RO       | RO   | RO   | RO                 |



 

I registri che supportano RW possono essere usati per archiviare i risultati intermedi. Sono inclusi i registri temporanei e i registri delle trame per alcune versioni dello shader.

> [!Note]  
>
> -   Per pixel shader versione 1 4, i registri di trama sono ro per le istruzioni di indirizzamento delle trame e i registri di trama non possono essere né letti né scritti da istruzioni \_ aritmetiche. Inoltre, poiché i registri trame sono diventati registri delle coordinate di trama, l'accesso ro non è una regressione delle funzionalità precedenti.

 

## <a name="range"></a>Intervallo

L'intervallo è il valore massimo e minimo dei dati del registro. Gli intervalli variano in base al tipo di registro. Gli intervalli per alcuni registri possono essere sottoposti a query dai limiti del dispositivo usando [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).



| Nome | Tipo               | Intervallo                                               | Versioni     |
|------|--------------------|-----------------------------------------------------|--------------|
| c\#  | Registro costanti  | Da -1 a +1                                            | Tutte le versioni |
| R\#  | Registro temporaneo | \- PixelShader1xMaxValue in + PixelShader1xMaxValue | Tutte le versioni |
| t\#  | Registro trame   | \- MaxTextureRepeat a + MaxTextureRepeat           | Tutte le versioni |
| Presso\#  | Registro colori     | Da 0 a 1                                              | Tutte le versioni |



 

L pixel shader hardware rappresenta i dati nei registri usando un numero a virgola fissa. Ciò limita la precisione a un massimo di circa otto bit per la parte frazionaria di un numero. Tenere presente questo problema durante la progettazione di uno shader.

Per pixel shader versione \_ 1 da 1 \_ a 1 3, MaxTextureRepeat deve essere almeno uno. Per 1 \_ 4, MaxTextureRepeat deve essere almeno otto.

Per altre informazioni su PixelShader1xMaxValue, vedere [**D3DCAPS9.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
