---
description: Questa tabella esegue il mapping di codici FVF a una struttura D3DVERTEXELEMENT9.
ms.assetid: de865481-2a08-4d25-967c-8e68b7affe8d
title: Mapping di codici FVF a una dichiarazione Direct3D 9 (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85442cf1c92c78aa1a37f4d4a4ec3de154f5b8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745367"
---
# <a name="mapping-fvf-codes-to-a-direct3d-9-declaration-direct3d-9"></a>Mapping di codici FVF a una dichiarazione Direct3D 9 (Direct3D 9)

Questa tabella esegue il mapping di codici FVF a una struttura [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .



| FVF                                                   | Tipo di dati                                                           | Utilizzo                                                                         | Indice di utilizzo |
|-------------------------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|
| D3DFVF \_ XYZ                                           | \_FLOAT3 D3DDECLTYPE                                                 | \_Posizione D3DDECLUSAGE                                                        | 0           |
| \_XYZRHW D3DFVF                                        | \_Float4 D3DDECLTYPE                                                 | \_Posizione D3DDECLUSAGE                                                       | 0           |
| \_XYZW D3DFVF                                          | \_Float4 D3DDECLTYPE                                                 | \_Posizione D3DDECLUSAGE                                                        | 0           |
| D3DFVF \_ XYZB5 e D3DFVF \_ LASTBETA \_ UBYTE4            | D3DVSDT \_ FLOAT3, D3DVSDT \_ float4, D3DVSDT \_ UBYTE4                   | \_Posizione D3DDECLUSAGE, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5 e D3DFVF \_ LASTBETA \_ D3DCOLOR          | D3DVSDT \_ FLOAT3, D3DVSDT \_ float4, D3DVSDT \_ D3DCOLOR                 | \_Posizione D3DDECLUSAGE, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| \_XYZB5 D3DFVF                                         | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float4, D3DDECLTYPE \_ FLOAT1       | \_Posizione D3DDECLUSAGE, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4)                                | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ floatn                            | \_Posizione D3DDECLUSAGE, D3DDECLUSAGE \_ BLENDWEIGHT                             | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4) e D3DFVF \_ LASTBETA \_ UBYTE4   | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float (n-1), D3DDECLTYPE \_ UBYTE4   | \_Posizione D3DDECLUSAGE, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n = 1.. 4) e D3DFVF \_ LASTBETA \_ D3DCOLOR | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float (n-1), D3DDECLTYPE \_ D3DCOLOR | \_Posizione D3DDECLUSAGE, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ normale                                        | \_FLOAT3 D3DDECLTYPE                                                 | D3DDECLUSAGE \_ normale                                                          | 0           |
| \_PSIZE D3DFVF                                         | \_FLOAT1 D3DDECLTYPE                                                 | \_PSIZE D3DDECLUSAGE                                                           | 0           |
| D3DFVF \_ diffuse                                       | \_D3DCOLOR D3DDECLTYPE                                               | \_Colore D3DDECLUSAGE                                                           | 0           |
| D3DFVF \_ speculare                                      | \_D3DCOLOR D3DDECLTYPE                                               | \_Colore D3DDECLUSAGE                                                           | 1           |
| D3DFVF \_ TEXCOORDSIZEm (n)                              | \_Float D3DDECLTYPE                                                 | \_TEXCOORD D3DDECLUSAGE                                                        | n           |



 

## <a name="vertex-declarations-with-d3ddeclusage_positiont"></a>Dichiarazioni dei vertici con D3DDECLUSAGE \_ posizionale

La presenza di un elemento Vertex con (D3DUSAGE \_ positiont, 0) viene usata per indicare al dispositivo che i dati dei vertici in arrivo sono già stati attraverso l'elaborazione del vertice (ad esempio un FVF con D3DFVF \_ XYZRHW bit set). In fase di estrazione, se la dichiarazione attualmente impostata include un elemento con la \_ semantica (D3DUSAGE positiont, 0), l'intera elaborazione del vertice viene ignorata (come se fosse stato impostato un FVF con D3DFVF \_ XYZRHW bit).

Esistono alcune restrizioni per le dichiarazioni dei vertici con (D3DDECLUSAGE \_ positiont, 0):

-   Nelle dichiarazioni di questo tipo è possibile utilizzare solo il flusso zero.
-   Gli elementi Vertex devono essere ordinati aumentando l'offset del flusso.
-   L'offset del flusso deve essere DWORD allineato.
-   La stessa coppia (utilizzo, indice di utilizzo) deve essere elencata una sola volta.
-   \_È possibile utilizzare solo il metodo predefinito D3DDECLMETHOD.
-   Gli altri elementi Vertex non possono avere la \_ semantica (position D3DDECLUSAGE, 0).

Inoltre, esistono alcune restrizioni su tale dichiarazione correlate alla versione del driver di dispositivo. Queste restrizioni sono attive perché Direct3D invia tali dichiarazioni direttamente al driver senza eseguire alcuna conversione.

## <a name="vertex-declarations-without-d3ddeclusage_positiont"></a>Dichiarazioni di vertici senza D3DDECLUSAGE \_ posizionale

Il runtime convalida la creazione di dichiarazioni. Di seguito sono riportate le regole generali per le dichiarazioni legali.

-   Tutti gli elementi Vertex per un flusso devono essere consecutivi e ordinati in base all'offset.
-   L'offset del flusso deve essere DWORD allineato.
-   La stessa coppia (utilizzo, indice di utilizzo) deve essere elencata una sola volta.
-   Se \_ viene impostato il VERTEXELEMENTSCANSHARESTREAMOFFSET D3DDEVCAPS2,
    -   Più elementi Vertex possono condividere lo stesso offset in un flusso.
    -   Gli elementi Vertex possono essere tutti di tipi diversi che possono avere dimensioni diverse.
    -   Gli elementi Vertex possono sovrapporsi in modo arbitrario. Ad esempio, un elemento può iniziare in una posizione di un flusso che, allo stesso tempo, si trova al centro di un altro elemento.
    -   Gli elementi Vertex possono avere un offset del flusso in qualsiasi ordine.
-   Il numero di elementi Vertex non può essere maggiore di 64.
-   UsageIndex deve essere compreso nell'intervallo \[ 0-15 \] .
-   La dichiarazione, usata con l'API DrawPrimitive, non deve avere elementi Vertex diversi da D3DDECLMETHOD \_ default, D3DDECLMETHOD \_ LOOKUPPRESAMPLED o D3DDECLMETHOD \_ Lookup.
-   La dichiarazione, che contiene D3DDECLMETHOD \_ Lookup o LOOKUPPRESAMPLED, deve essere utilizzata solo con la pipeline di vertex programmabile.
-   La dichiarazione, usata con l'API DrawRectPatch/DrawTriPatch, non può avere elementi Vertex con D3DDECLMETHOD \_ LOOKUPPRESAMPLED o D3DDECLMETHOD \_ Lookup.
-   La dichiarazione deve avere un solo elemento con il \_ Metodo D3DDECLMETHOD Lookup o D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   La dichiarazione con D3DDECLMETHOD \_ Lookup o D3DDECLMETHOD \_ LOOKUPPRESAMPLED non deve avere elementi diversi da D3DDECLMETHOD \_ default, perché il mapping di spostamento viene eseguito solo per N-patch.
-   Gli elementi Vertex con D3DDECLMETHOD \_ Lookup o D3DDECLMETHOD \_ LOOKUPPRESAMPLED possono essere usati solo con la \_ semantica (D3DDECLUSAGE Sample, n) e viceversa.
-   Se un elemento Vertex con \_ metodo di ricerca D3DDECLMETHOD ha un indice del flusso e un offset di un elemento Vertex già esistente, questo elemento Vertex deve avere lo stesso tipo di dati.
-   Un elemento Vertex con il \_ metodo di ricerca D3DDECLMETHOD deve avere il \_ tipo di dati D3DDECLTYPE FLOAT2/3/4
-   Gli elementi Vertex con i tipi D3DDECLMETHOD \_ CROSSUV, D3DDECLMETHOD \_ partial e D3DDECLMETHOD \_ PARTIALV devono avere un offset di un elemento Vertex con un tipo di dati compatibile.
-   Un elemento Vertex con il metodo D3DDECLMETHOD \_ UV o D3DDECLMETHOD \_ LOOKUPPRESAMPLED deve essere di tipo D3DDECLTYPE \_ inutilizzato, Stream index zero e Stream offset zero.
-   Le dichiarazioni con i metodi D3DDECLMETHOD \_ UV, D3DDECLMETHOD \_ partial e D3DDECLMETHOD \_ PARTIALV possono essere utilizzate solo con DrawRectPatch.
-   Usage D3DDECLUSAGE \_ TESSFACTOR deve essere usato solo con il tipo di dati D3DDECLTYPE \_ FLOAT1 e Usage index 0.
-   Quando una dichiarazione viene utilizzata per la suddivisione a mosaico (DrawRectPatch, DrawTriPatch, N-patches), il tipo di dati deve essere minore o uguale a D3DDECLTYPE \_ SHORT4.
-   È possibile creare dichiarazioni che contengono metodi che richiedono determinate funzionalità del dispositivo, ad esempio il mapping di spostamento, le patch RT, solo se sono supportate dal dispositivo.
-   Una dichiarazione del vertice utilizzata per creare punti e linee non può avere metodi diversi da D3DDECLMETHOD \_ default.
-   Anche le dichiarazioni che è possibile creare dipendono dalle funzionalità del driver.

## <a name="driver-considerations"></a>Considerazioni sui driver

### <a name="pre-direct3d-9-drivers"></a>Driver precedenti a Direct3D 9

-   La dichiarazione di input deve essere convertibile in un FVF valido (avere lo stesso ordine di elementi Vertex e i relativi tipi di dati).
-   Non sono consentiti gap nelle coordinate di trama. Ciò significa che se è presente un elemento Vertex con (D3DDECLUSAGE \_ TEXCOORD, n), deve essere presente anche un elemento Vertex con (D3DDECLUSAGE \_ TEXCOORD, n-1).

### <a name="direct3d-9-drivers-without-pixel-shader-version-3-support"></a>Driver Direct3D 9 senza supporto di pixel shader versione 3

-   La dichiarazione di input deve essere convertibile in un FVF valido (avere lo stesso ordine di elementi Vertex e i relativi tipi di dati).
-   Sono consentiti gap nelle coordinate di trama.

### <a name="direct3d-9-drivers-with-pixel-shader-version-3-support"></a>Driver Direct3D 9 con supporto di pixel shader versione 3

Sono consentite più dichiarazioni generali.

-   Gli elementi Vertex possono essere in ordine arbitrario e possono avere qualsiasi tipo di dati.
-   Più elementi Vertex possono condividere lo stesso offset del flusso ed essere di un tipo diverso nello stesso momento se D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET è impostato dal dispositivo.

## <a name="vertex-declaration-usage-with-the-programmable-vertex-pipeline"></a>Utilizzo delle dichiarazioni dei vertici con la pipeline di vertex programmabile

-   In fase di estrazione, Direct3D cerca la stessa combinazione "Indice utilizzo utilizzo" nella dichiarazione del vertice corrente e nella funzione vertex shader corrente. Quando viene rilevata la combinazione, viene usato il registro della funzione di shader DCL come destinazione per l'elemento vertex.
-   Quando un elemento vertice nella dichiarazione del vertice corrente ha un utilizzo non trovato nel vertex shader corrente, tale elemento del vertice viene ignorato.
-   Quando si usa una versione di vertex shader inferiore a 2,0, è necessario che tutte le semantiche indicate nel codice dello shader siano presenti nella dichiarazione associata al momento dell'estrazione. Quando si usano vertex shader 2,0 e versioni successive, questa restrizione che consente alle applicazioni di usare dichiarazioni di vertici diverse con lo stesso vertex shader non esiste. Questa operazione è utile quando un vertex shader legge i dati di input in base alle condizioni statiche. I registri vertex shader non sono inizializzati perché avranno valori non definiti.

Sono presenti restrizioni aggiuntive quando si usa con l'elaborazione dei vertici hardware in un driver DirectX 8:

-   Gli elementi Vertex non possono sovrapporsi o condividere lo stesso offset.
-   I tipi di dati sono limitati a ciò che il driver DirectX 8 può comprendere.

CreateVertexDeclaration potrebbe non riuscire se la dichiarazione fornita non può essere convertita in una dichiarazione di tipo DirectX 8. Per un dispositivo in modalità mista, questo errore si verificherà in fase di estrazione, \* perché questo è l'unico caso in cui è possibile sapere se lo shader viene usato con l'elaborazione dei vertici hardware o software.

## <a name="vertex-declaration-usage-with-the-fixed-function-pipeline"></a>Utilizzo della dichiarazione vertex con la pipeline della funzione fissa

È possibile utilizzare solo le dichiarazioni che rispettano le regole seguenti:

-   Non devono esserci gap tra gli elementi del vertice (SKIP non è consentito in una dichiarazione di DirectX 8, che viene usata per la pipeline della funzione fissa).
-   È necessario specificare la semantica ( \_ posizione D3DDECLUSAGE, 0) e il \_ tipo di dati D3DDECLTYPE FLOAT3.
-   Un elemento Vertex con il metodo D3DDECLMETHOD \_ UV deve specificare l'utilizzo D3DDECLUSAGE \_ TEXCOORD o D3DDECLUSAGE \_ BLENDWEIGHT.
-   Un elemento Vertex con il metodo D3DDECLMETHOD \_ , \_ PARTIALV o \_ CROSSUV può essere usato solo con la posizione D3DDECLUSAGE \_ , \_ Normal, \_ BLENDWEIGHT o \_ TEXCOORD e deve usare il tipo di input D3DDECLTYPE \_ FLOAT3.

Quando si usa una dichiarazione con l'elaborazione del vertice hardware in un driver DirectX 8, il runtime Direct3D lo converte in una dichiarazione di tipo DirectX 8 con le regole seguenti:

-   Gli elementi Vertex non possono condividere lo stesso offset in un flusso e non possono sovrapporsi.
-   Il tipo di dati deve essere minore o uguale a D3DDECLTYPE \_ SHORT4.
-   Sono consentiti solo i metodi seguenti: D3DDECLMETHOD \_ default, D3DDECLMETHOD \_ CROSSUV e D3DDECLMETHOD \_ UV
-   [Il mapping tra una dichiarazione Direct3D 9 e una dichiarazione Direct3D 8 (Direct3D 9)](mapping-between-a-directx-9-declaration-and-directx-8.md) indica quale semantica Direct3D 9 potrebbe essere convertita in una dichiarazione di tipo DirectX 8. Usage e UsageIndex vengono convertiti in un valore di registro.
-   Se sono presenti n elementi Vertex in una dichiarazione e 0-m (m < n) viene mappato a un FVF (elementi descritti nel [mapping tra una dichiarazione Direct3D e i codici FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md)), ma m + 1 non lo è:
    -   Se una qualsiasi di m + 2 fino a n-1 elementi Vertex viene mappata a FVF/dx8decl, la dichiarazione non è valida.
    -   Gli elementi da 0 a m vengono convertiti (dal runtime per i driver DirectX 8 e versioni precedenti e dai driver Direct3D 9) utilizzando il [mapping tra una dichiarazione Direct3D e i codici FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md), m + 1, m + 2 fino a n-1 viene mappato a TEXCOORD contigui (k), TEXCOORD (k + 1), a partire da qualsiasi TEXCOORD negli elementi 0
    -   Si presuppone che il tipo di dati in un TEXCOORD mappato sia float \[ 1234 \] sostituendo qualsiasi tipo di dati contenuto nell'elemento corrente, ma le stesse dimensioni. Pertanto, il tipo di dati esistente può essere un elemento che non si trova nel [mapping tra una dichiarazione Direct3D e i codici FVF (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md).
    -   Se k raggiunge 8, la dichiarazione non è valida per FVF/dx8decl.
    -   Se si sono verificati mapping a TexCoords, è necessario che l'intera dichiarazione non includa elementi con un metodo di generazione diverso da DEFAULT o che la dichiarazione non sia valida per FVF/dx8decl.

## <a name="using-vertex-declarations-with-processvertices"></a>Uso di dichiarazioni di vertici con ProcessVertices

Per descrivere l'output di ProcessVertices, è possibile usare una dichiarazione di vertice. Tale dichiarazione deve rispettare le regole seguenti:

-   È necessario utilizzare solo il flusso 0.
-   \_Sono consentiti solo i metodi predefiniti D3DDECLMETHOD.
-   \_È possibile utilizzare solo i tipi di dati D3DDECLTYPE Floated o D3DDECLTYPE \_ D3DCOLOR.
-   Gli elementi Vertex non possono condividere lo stesso offset o sovrapporsi.
-   Gli elementi Vertex con ( \_ posizione D3DDECLUSAGE, 0) o (D3DDECLUSAGE \_ positiont, 0) non sono obbligatori.
-   Gli elementi Vertex con ( \_ posizione D3DDECLUSAGE, 0) e (D3DDECLUSAGE \_ positiont, 0) non possono essere presenti nella stessa dichiarazione.
-   Quando viene usata questa dichiarazione, il vertex shader corrente deve essere la versione 3,0 o successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione vertici](vertex-declaration.md)
</dt> </dl>

 

 



