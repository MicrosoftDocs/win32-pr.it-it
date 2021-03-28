---
title: sincronizzazione (SM5-ASM)
description: Sincronizzazione del gruppo di thread o barriera di memoria.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993264"
---
# <a name="sync-sm5---asm"></a>sincronizzazione (SM5-ASM)

Sincronizzazione del gruppo di thread o barriera di memoria.



| uglobal di sincronizzazione \[ \_ \|\_ugroup \] \[ \_ g \] \[ \_ t\] |
|-------------------------------------------|



 

## <a name="remarks"></a>Commenti

Per la **sincronizzazione** sono disponibili \_ le opzioni uglobal, \_ ugroup, \_ g e \_ t.

Nel pixel shader è consentito solo **\_ uglobal di sincronizzazione** .

Nel compute shader, \_ è necessario specificare (uglobal o \_ ugroup \* ) e/o \_ g. \_t è inoltre facoltativo.

### <a name="_uglobal"></a>\_uglobal

\#Recinzione della memoria globale u (UAV).

Tutte le \# letture e scritture di memoria u precedenti eseguite da questo thread nell'ordine del programma vengono rese visibili a tutti i thread sull'intera GPU prima di qualsiasi accesso alla memoria u successivo da parte del \# thread. L'intera parte GPU della definizione viene sostituita da un ambito meno globale in un caso, descritta di seguito.

Si applica a tutti i limiti di memoria UAV nella fase corrente dello shader.

\_uglobal è disponibile nel compute shader o pixel shader.

Per tutti gli UAV associati che non sono stati dichiarati dallo shader come coerenti a livello globale, il limite di \_ memoria uglobal u \# è visibile solo all'interno del gruppo di thread del compute shader corrente per tale UAV, come se fosse \_ ugroup anziché \_ uglobal. Questo problema si applica solo al compute shader, perché il pixel shader deve dichiarare tutti i UAV come coerenti a livello globale.

### <a name="_ugroup"></a>\_ugroup

Limite di memoria u \# (UAV) dell'ambito del gruppo di thread.

Tutte le \# letture o scritture della memoria u precedenti da questo thread nell'ordine del programma vengono rese visibili a tutti i thread del gruppo di thread prima di qualsiasi accesso alla memoria u successivo da parte del \# thread.

Si applica a tutti i limiti di memoria UAV nella fase corrente dello shader.

\_ugroup è disponibile solo nel compute shader.

Se \_ ugroup è esposto, per alcune implementazioni. Il vantaggio di specificare \_ ugroup anziché \_ uglobal è che l'operazione di **sincronizzazione** può essere completata più rapidamente.

Altre implementazioni non distinguono \_ ugroup da \_ uglobal, pertanto entrambe le operazioni sono equivalenti e si comportano come \_ uglobal. Le applicazioni possono specificare il loro scopo richiedendo l'ambito di **sincronizzazione** più restrittivo necessario.

Anche se un determinato UAV viene dichiarato come coerente a livello globale, un' \_ operazione di **sincronizzazione** ugroup funzionerà in modo più efficiente in tale UAV se non è necessaria una barriera globale.

### <a name="_g"></a>\_g

limite di \# memoria condivisa del gruppo di thread.

Tutte le operazioni \# di lettura o scrittura di memoria precedenti da parte di questo thread nell'ordine del programma vengono rese visibili a tutti i thread del gruppo di thread prima di eventuali accessi successivi alla memoria g da parte del \# thread.

Questo vale per tutti i file di memoria condivisa g del gruppo di thread corrente \# .

\_g è disponibile solo nel compute shader.

### <a name="_t"></a>\_t

Sincronizzazione del gruppo di thread. Tutti i thread all'interno di un singolo gruppo di thread (quelli che possono condividere l'accesso a un set comune di spazio del registro condiviso) verranno eseguiti fino al punto in cui raggiungono questa istruzione prima che un thread possa continuare.

\_t non può essere inserito nel controllo dinamico del flusso, (rami che possono variare all'interno di un gruppo di thread), ma può essere presente in un controllo di flusso uniforme, in cui tutti i thread del gruppo scelgono lo stesso percorso.

\_t è disponibile solo nel compute shader.

Di seguito è riportato un elenco di varianti di Compute Shader "Sync".

-   Sincronizza \_ g
-   Sincronizza \_ ugroup\*
-   Sincronizza \_ uglobal
-   Sincronizza \_ g \_ t
-   ugroup di sincronizzazione \_ \_ t\*
-   uglobal di sincronizzazione \_ \_ t
-   Sincronizza \_ ugroup \_ g\*
-   Sincronizza \_ uglobal \_ g
-   ugroup di sincronizzazione \_ \_ g \_ t\*
-   uglobal di sincronizzazione \_ \_ g \_ t

\*Le varianti con \_ ugroup potrebbero non essere destinate al compilatore HLSL, in base alla precedente discussione nella \_ sezione ugroup precedente.

L'elenco di pixel shader varianti di sincronizzazione include \_ solo uglobal di sincronizzazione.

Le barriere di memoria impediscono il riordinamento delle istruzioni interessate da parte dei compilatori o dell'hardware attraverso la recinzione.

Più letture dallo stesso indirizzo tramite una chiamata dello shader che non sono separate da barriere di memoria o scritture nell'indirizzo possono essere compresse insieme. Lo stesso vale per le operazioni di scrittura. Gli accessi separati da una barriera non possono essere Uniti o spostati attraverso la barriera.

Le barriere di memoria non sono necessarie per il corretto funzionamento delle operazioni atomiche per un determinato indirizzo da thread diversi. I limiti sono necessari quando le operazioni atomiche e/o di caricamento/archiviazione devono essere sincronizzate l'una rispetto all'altra, perché appaiono nei singoli thread dal punto di vista di altri thread.

Nel pixel shader, le istruzioni di [eliminazione](discard--sm4---asm-.md) implicano un limite di sincronizzazione \_ uglobal, in quanto non è possibile riordinare le istruzioni in uno **scarto**. sincronizzare \_ uglobal nei pixel Helper (che vengono eseguiti solo per supportare i derivati) o i pixel rimossi possono avere o meno alcun effetto. Non è consentito per l'helper o i pixel scartati di scrivere in UAV se, nel caso di scarto, le scritture vengono rilasciate dopo l'eliminazione. I valori restituiti da UAV non possono contribuire ai calcoli derivati. Per questo motivo, se \_ la sincronizzazione u viene rispettata per i pixel helper o quando viene rilasciata, dopo uno scarto è discutibile.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, la variante **\_ uglobal di sincronizzazione** di questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




