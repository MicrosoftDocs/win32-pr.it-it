---
description: Questa tabella esegue il mapping dei codici FVF a una struttura D3DVERTEXELEMENT9.
ms.assetid: de865481-2a08-4d25-967c-8e68b7affe8d
title: Mapping dei codici FVF a una dichiarazione Direct3D 9 (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8ef4d5e8e29c4c7f6af8d82b650b4898c57d900b92b8dd45ca2368bb9eacce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799077"
---
# <a name="mapping-fvf-codes-to-a-direct3d-9-declaration-direct3d-9"></a>Mapping dei codici FVF a una dichiarazione Direct3D 9 (Direct3D 9)

Questa tabella esegue il mapping dei codici FVF a [**una struttura D3DVERTEXELEMENT9.**](d3dvertexelement9.md)



| FVF                                                   | Tipo di dati                                                           | Utilizzo                                                                         | Indice di utilizzo |
|-------------------------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|
| D3DFVF \_ XYZ                                           | D3DDECLTYPE \_ FLOAT3                                                 | POSIZIONE D3DDECLUSAGE \_                                                        | 0           |
| D3DFVF \_ XYZRHW                                        | D3DDECLTYPE \_ FLOAT4                                                 | D3DDECLUSAGE \_ POSITIONT                                                       | 0           |
| D3DFVF \_ XYZW                                          | D3DDECLTYPE \_ FLOAT4                                                 | POSIZIONE D3DDECLUSAGE \_                                                        | 0           |
| D3DFVF \_ XYZB5 e D3DFVF \_ LASTBETA \_ UBYTE4            | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ UBYTE4                   | POSIZIONE D3DDECLUSAGE, \_ D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5 e D3DFVF \_ LASTBETA \_ D3DCOLOR          | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ D3DCOLOR                 | POSIZIONE D3DDECLUSAGE, \_ D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5                                         | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT4, D3DDECLTYPE \_ FLOAT1       | POSIZIONE D3DDECLUSAGE, \_ D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n=1..4)                                | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOATn                            | POSIZIONE D3DDECLUSAGE, \_ D3DDECLUSAGE \_ BLENDWEIGHT                             | 0           |
| D3DFVF \_ XYZBn (n=1..4) e D3DFVF \_ LASTBETA \_ UBYTE4   | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT(n-1), D3DDECLTYPE \_ UBYTE4   | POSIZIONE D3DDECLUSAGE, \_ D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n=1..4) e D3DFVF \_ LASTBETA \_ D3DCOLOR | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT(n-1), D3DDECLTYPE \_ D3DCOLOR | POSIZIONE D3DDECLUSAGE, \_ D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ NORMAL                                        | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ NORMAL                                                          | 0           |
| D3DFVF \_ PSIZE                                         | D3DDECLTYPE \_ FLOAT1                                                 | D3DDECLUSAGE \_ PSIZE                                                           | 0           |
| D3DFVF \_ DIFFUSE                                       | D3DDECLTYPE \_ D3DCOLOR                                               | COLORE D3DDECLUSAGE \_                                                           | 0           |
| SPECULARE D3DFVF \_                                      | D3DDECLTYPE \_ D3DCOLOR                                               | COLORE D3DDECLUSAGE \_                                                           | 1           |
| D3DFVF \_ TEXCOORDSIZEm(n)                              | D3DDECLTYPE \_ FLOATm                                                 | D3DDECLUSAGE \_ TEXCOORD                                                        | n           |



 

## <a name="vertex-declarations-with-d3ddeclusage_positiont"></a>Dichiarazioni di vertici con D3DDECLUSAGE \_ POSITIONT

La presenza di un elemento vertice con (D3DUSAGE POSITIONT, 0) viene usata per indicare al dispositivo che i dati dei vertici in arrivo sono già stati tramite l'elaborazione dei vertici (ad esempio un FVF con set di \_ bit D3DFVF \_ XYZRHW). In fase di disegno, se la dichiarazione attualmente impostata include un elemento con semantica (D3DUSAGE POSITIONT, 0), l'intera elaborazione dei vertici viene ignorata (proprio come se fosse stato impostato un \_ FVF con bit D3DFVF \_ XYZRHW).

Esistono alcune restrizioni sulle dichiarazioni di vertici con (D3DDECLUSAGE \_ POSITIONT, 0):

-   In tali dichiarazioni è possibile usare solo il flusso zero.
-   Gli elementi vertice devono essere ordinati aumentando l'offset del flusso.
-   L'offset del flusso deve essere allineato con DWORD.
-   La stessa coppia (Usage, Usage Index) deve essere elencata una sola volta.
-   È possibile usare solo il metodo D3DDECLMETHOD \_ DEFAULT.
-   Altri elementi vertice non possono avere la semantica (D3DDECLUSAGE \_ POSITION, 0).

Esistono inoltre alcune restrizioni su tale dichiarazione correlate alla versione del driver di dispositivo. Queste restrizioni sono effettive perché Direct3D invia tali dichiarazioni direttamente al driver senza eseguire alcuna conversione.

## <a name="vertex-declarations-without-d3ddeclusage_positiont"></a>Dichiarazioni di vertici senza D3DDECLUSAGE \_ POSITIONT

Il runtime convalida la creazione di dichiarazioni. Di seguito sono riportate le regole generali per le dichiarazioni legali.

-   Tutti gli elementi vertice per un flusso devono essere consecutivi e ordinati in base all'offset.
-   L'offset del flusso deve essere allineato con DWORD.
-   La stessa coppia (Usage, Usage Index) deve essere elencata una sola volta.
-   Se l'opzione D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET è impostata,
    -   Più elementi vertice possono condividere lo stesso offset in un flusso.
    -   Gli elementi vertice possono essere tutti di tipi diversi, che possono avere dimensioni diverse.
    -   Gli elementi vertice possono sovrapporsi in modo arbitrario. Ad esempio, un elemento può iniziare da una posizione di un flusso che si trova, contemporaneamente, al centro di un altro elemento.
    -   Agli elementi vertice è consentito l'offset del flusso in qualsiasi ordine.
-   Il numero di elementi vertice non può essere maggiore di 64.
-   UsageIndex deve essere compreso nell'intervallo \[ 0-15. \]
-   La dichiarazione, usata con l'API DrawPrimitive, non deve avere elementi vertice diversi da D3DDECLMETHOD \_ DEFAULT, D3DDECLMETHOD \_ LOOKUPPRESAMPLED o D3DDECLMETHOD \_ LOOKUP.
-   La dichiarazione , che contiene D3DDECLMETHOD LOOKUP o LOOKUPPRESAMPLED, deve essere usata solo con la \_ pipeline di vertici programmabili.
-   La dichiarazione, usata con l'API DrawRectPatch/DrawTriPatch, non può avere elementi vertice con D3DDECLMETHOD \_ LOOKUPPRESAMPLED o D3DDECLMETHOD \_ LOOKUP.
-   La dichiarazione deve avere un solo elemento con il metodo D3DDECLMETHOD \_ LOOKUP o D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   La dichiarazione con D3DDECLMETHOD LOOKUP o D3DDECLMETHOD LOOKUPPRESAMPLED non deve avere elementi diversi da \_ \_ D3DDECLMETHOD DEFAULT, perché il mapping dello spostamento viene eseguito solo per \_ le patch N.
-   Gli elementi vertice con D3DDECLMETHOD LOOKUP o D3DDECLMETHOD LOOKUPPRESAMPLED possono essere usati solo con la \_ \_ semantica (D3DDECLUSAGE \_ SAMPLE, n) e viceversa.
-   Se un elemento vertice con metodo D3DDECLMETHOD LOOKUP ha un indice di flusso e un offset di un elemento vertice già esistente, questo elemento vertice deve \_ avere lo stesso tipo di dati.
-   Un elemento vertice con il metodo D3DDECLMETHOD LOOKUP deve avere il tipo di dati \_ D3DDECLTYPE \_ FLOAT2/3/4
-   Gli elementi vertice con tipi D3DDECLMETHOD \_ CROSSUV, D3DDECLMETHOD PARTIALU e \_ D3DDECLMETHOD PARTIALV devono avere un offset di un elemento vertice con un tipo di dati \_ compatibile.
-   Un elemento vertice con il metodo D3DDECLMETHOD UV o \_ D3DDECLMETHOD LOOKUPPRESAMPLED deve avere il tipo \_ D3DDECLTYPE UNUSED, l'indice di flusso zero e l'offset del flusso \_ zero.
-   Le dichiarazioni con metodi D3DDECLMETHOD \_ UV, D3DDECLMETHOD PARTIALU e \_ D3DDECLMETHOD PARTIALV possono essere usate solo con \_ DrawRectPatch.
-   L'utilizzo di D3DDECLUSAGE TESSFACTOR deve essere usato solo con il tipo di dati \_ D3DDECLTYPE FLOAT1 e l'indice \_ di utilizzo 0.
-   Quando si usa una dichiarazione per lo schema a squame (DrawRectPatch, DrawTriPatch, N patch), il tipo di dati deve essere minore o uguale a D3DDECLTYPE \_ SHORT4.
-   Le dichiarazioni che contengono metodi che richiedono determinate funzionalità del dispositivo (ad esempio, mapping di spostamento, patch RT) possono essere create solo se il dispositivo le supporta.
-   Una dichiarazione di vertice usata per disegnare punti e linee non può avere metodi diversi da D3DDECLMETHOD \_ DEFAULT.
-   Le dichiarazioni che possono essere create dipendono anche dalle funzionalità del driver.

## <a name="driver-considerations"></a>Considerazioni sui driver

### <a name="pre-direct3d-9-drivers"></a>Driver pre-Direct3D 9

-   La dichiarazione di input deve essere traducibile in un FVF valido (avere lo stesso ordine di elementi vertice e i relativi tipi di dati).
-   Gli spazi vuoti nelle coordinate della trama non sono consentiti. Ciò significa che se è presente un elemento vertice con (D3DDECLUSAGE TEXCOORD, n), deve essere presente anche un elemento vertice con \_ (D3DDECLUSAGE \_ TEXCOORD, n-1).

### <a name="direct3d-9-drivers-without-pixel-shader-version-3-support"></a>Driver Direct3D 9 senza supporto per Pixel Shader versione 3

-   La dichiarazione di input deve essere traducibile in un FVF valido (avere lo stesso ordine di elementi vertice e i relativi tipi di dati).
-   Sono consentiti gap nelle coordinate della trama.

### <a name="direct3d-9-drivers-with-pixel-shader-version-3-support"></a>Driver Direct3D 9 con supporto pixel shader versione 3

Sono consentite dichiarazioni più generali.

-   Gli elementi vertice possono essere in ordine arbitrario e possono avere qualsiasi tipo di dati.
-   Più elementi vertice possono condividere lo stesso offset del flusso e essere di un tipo diverso nello stesso momento se D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET è impostato dal dispositivo.

## <a name="vertex-declaration-usage-with-the-programmable-vertex-pipeline"></a>Utilizzo della dichiarazione dei vertici con la pipeline dei vertici programmabili

-   In fase di disegno Direct3D cerca la stessa combinazione di "utilizzo - indice di utilizzo" nella dichiarazione del vertice corrente e nella funzione vertex shader corrente. Quando viene trovata la combinazione, il registro della DCL della funzione shader viene usato come destinazione per l'elemento vertice.
-   Quando un elemento vertice nella dichiarazione del vertice corrente ha un utilizzo che non viene trovato nel vertex shader corrente, tale elemento vertice viene ignorato.
-   Quando si usa una versione dei vertex shader precedente alla 2.0, tutta la semantica indicata nel codice dello shader deve essere presente nella dichiarazione associata in fase di disegno. Quando si usano vertex shader 2.0 e versioni successive, questa restrizione che consente alle applicazioni di usare dichiarazioni di vertice diverse con lo stesso vertex shader non esiste. Ciò è utile quando un vertex shader legge i dati di input in base a condizioni statiche. I registri vertex shader non sono inizializzati perché avranno valori non definiti.

Esistono restrizioni aggiuntive quando si usa con l'elaborazione dei vertici hardware in un driver DirectX 8:

-   Gli elementi vertice non possono sovrapporsi o condividere lo stesso offset.
-   I tipi di dati sono limitati a ciò che il driver DirectX 8 è in grado di comprendere.

CreateVertexDeclaration potrebbe non riuscire se la dichiarazione specificata non può essere convertita in una dichiarazione di tipo DirectX 8. Per un dispositivo in modalità mista, questo errore si verifica in fase di disegno perché è l'unica volta che è possibile sapere se questo shader viene usato con l'elaborazione \* di vertici hardware o software.

## <a name="vertex-declaration-usage-with-the-fixed-function-pipeline"></a>Utilizzo della dichiarazione dei vertici con la pipeline di funzioni fisse

È possibile usare solo dichiarazioni conformi alle regole seguenti:

-   Non devono essere presenti gap tra gli elementi vertice (SKIP non è consentito in una dichiarazione DirectX 8, usata per la pipeline di funzioni fisse).
-   È necessario specificare semantico (D3DDECLUSAGE POSITION, 0) e il tipo di dati \_ D3DDECLTYPE \_ FLOAT3.
-   Un elemento vertice con metodo D3DDECLMETHOD UV deve specificare l'utilizzo \_ di D3DDECLUSAGE \_ TEXCOORD o D3DDECLUSAGE \_ BLENDWEIGHT.
-   Un elemento vertice con metodo D3DDECLMETHOD PARTIALU, PARTIALV o CROSSUV può essere usato solo con \_ \_ \_ D3DDECLUSAGE POSITION, NORMAL, BLENDWEIGHT o TEXCOORD e deve usare il tipo di \_ input \_ \_ \_ D3DDECLTYPE \_ FLOAT3.

Quando una dichiarazione viene usata con l'elaborazione dei vertici hardware in un driver DirectX 8, il runtime Direct3D la converte in una dichiarazione di tipo DirectX 8 con le regole seguenti:

-   Gli elementi vertice non possono condividere lo stesso offset in un flusso e non possono sovrapporsi.
-   Il tipo di dati deve essere minore o uguale a D3DDECLTYPE \_ SHORT4.
-   Sono consentiti solo i metodi seguenti: D3DDECLMETHOD \_ DEFAULT, D3DDECLMETHOD \_ CROSSUV e D3DDECLMETHOD \_ UV
-   Il mapping tra una dichiarazione Direct3D 9 e una dichiarazione [Direct3D 8 (Direct3D 9)](mapping-between-a-directx-9-declaration-and-directx-8.md) indica quale semantica Direct3D 9 può essere convertita in dichiarazione di tipo DirectX 8. Usage e UsageIndex vengono convertiti in un valore di registro.
-   Se sono presenti n elementi vertice in una dichiarazione e 0 - m (m < n) esegue il mapping a un FVF (elementi descritti in Mapping tra una dichiarazione Direct3D e codici [FVF (Direct3D 9),](mapping-between-a-directx-9-declaration-and-fvf-codes.md)ma m + 1 no, allora:
    -   Se uno degli elementi m + 2 fino a n - 1 elementi vertice è mappato a FVF/dx8decl, la dichiarazione non è valida.
    -   Gli elementi da 0 a m vengono convertiti (dal runtime per i driver DirectX 8 e versioni precedenti e dai driver Direct3D 9) usando il mapping tra una dichiarazione Direct3D e i codici [FVF (Direct3D 9),](mapping-between-a-directx-9-declaration-and-fvf-codes.md)m + 1, m + 2 fino a n - 1 vengono mappati a texcoord(k) contigui, texcoord (k+1), a partire da qualsiasi texcoord negli elementi 0 - m.
    -   Si presuppone che il tipo di dati in un texcoord mappato sia float 1234 sostituendo il tipo di dati contenuto nell'elemento corrente (ma con \[ \] le stesse dimensioni). Pertanto, il tipo di dati esistente può essere un elemento che non è in Mapping tra una dichiarazione Direct3D e i codici [FVF (Direct3D 9).](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
    -   Se k raggiunge 8, la dichiarazione non è valida per FVF/dx8decl.
    -   Se si sono verificati mapping a texcoord, è necessario che l'intera dichiarazione non abbia elementi con un metodo di generazione diverso da DEFAULT o che la dichiarazione non sia valida per FVF/dx8decl.

## <a name="using-vertex-declarations-with-processvertices"></a>Uso delle dichiarazioni dei vertici con ProcessVertices

È possibile usare una dichiarazione di vertice per descrivere l'output di ProcessVertices. Tale dichiarazione deve rispettare le regole seguenti:

-   È necessario usare solo il flusso 0.
-   Sono consentiti solo metodi D3DDECLMETHOD \_ DEFAULT.
-   È possibile utilizzare solo i tipi di dati \_ D3DDECLTYPE FLOATn o D3DDECLTYPE \_ D3DCOLOR.
-   Gli elementi vertice non possono condividere lo stesso offset o sovrapporsi tra loro.
-   Gli elementi vertice con (D3DDECLUSAGE \_ POSITION, 0) o (D3DDECLUSAGE \_ POSITIONT,0) non sono necessari.
-   Gli elementi vertice con (D3DDECLUSAGE \_ POSITION, 0) e (D3DDECLUSAGE POSITIONT,0) non possono essere \_ presenti nella stessa dichiarazione.
-   Quando si usa tale dichiarazione, il vertex shader corrente deve essere versione 3.0 o successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione dei vertici](vertex-declaration.md)
</dt> </dl>

 

 



