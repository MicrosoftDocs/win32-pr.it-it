---
title: sync (sm5 - asm)
description: Sincronizzazione del gruppo di thread o barriera di memoria.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c64532669fc94d7d2109c39e501af0825e56434f66b79e20e1641c787a1a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852861"
---
# <a name="sync-sm5---asm"></a>sync (sm5 - asm)

Sincronizzazione del gruppo di thread o barriera di memoria.



| sync \[ \_ uglobal\|\_ugroup \] \[ \_ g \] \[ \_ t\] |
|-------------------------------------------|



 

## <a name="remarks"></a>Commenti

**La** sincronizzazione include \_ opzioni uglobal, \_ ugroup, \_ g e \_ t.

Nel pixel shader è consentito solo **\_ l'uglobal di** sincronizzazione.

Nello shader di calcolo è necessario specificare ( \_ uglobal o \_ ugroup \* ) \_ e/o g. \_t è anche facoltativo.

### <a name="_uglobal"></a>\_uglobal

Recinto di memoria \# U (UAV) globale.

Tutte le operazioni di lettura/scrittura di memoria u precedenti da parte di questo thread nell'ordine del programma vengono rese visibili a tutti i thread nell'intera GPU prima di qualsiasi successivo accesso alla memoria \# u da parte di questo \# thread. L'intera parte DELLA GPU della definizione viene sostituita da un ambito meno globale in un caso, descritto di seguito.

Ciò si applica a tutta la memoria UAV associata alla fase corrente dello shader.

\_uglobal è disponibile nello shader di calcolo o nella pixel shader.

Per qualsiasi UAV associato che non è stato dichiarato dallo shader come Globally Coherent, il recinto uglobal u memory ha visibilità solo all'interno del gruppo di thread dello shader di calcolo corrente per tale UAV, come se fosse ugroup anziché \_ \# \_ \_ uglobal. Questo problema si applica solo allo shader di calcolo, perché il pixel shader deve dichiarare tutti gli UAV come globalmente coerenti.

### <a name="_ugroup"></a>\_ugroup

Limite di memoria \# u (UAV) dell'ambito del gruppo di thread.

Tutte le operazioni di lettura o scrittura di memoria u precedenti da parte di questo thread nell'ordine del programma vengono rese visibili a tutti i thread nel gruppo di thread prima di qualsiasi successivo accesso alla memoria \# u da parte di questo \# thread.

Ciò si applica a tutta la memoria UAV associata alla fase corrente dello shader.

\_ugroup è disponibile solo nello shader di calcolo.

Se \_ ugroup è esposto, per alcune implementazioni. Il vantaggio di specificare \_ ugroup anziché \_ uglobal è che l'operazione **di** sincronizzazione può essere completata più rapidamente.

Altre implementazioni non distinguono ugroup da uglobal, quindi entrambe le operazioni sono \_ \_ equivalenti e si comportano come \_ uglobal. Le applicazioni possono specificare la finalità richiedendo l'ambito di **sincronizzazione** più ristretto necessario.

Anche se un determinato UAV viene dichiarato globalmente coerente, un'operazione di sincronizzazione ugroup funzionerà in modo più efficiente su tale UAV se non è necessaria una barriera \_ globale. 

### <a name="_g"></a>\_G

g \# (memoria condivisa del gruppo di thread).

Tutte le operazioni precedenti di lettura o scrittura di memoria g da parte di questo thread nell'ordine del programma vengono rese visibili a tutti i thread nel gruppo di thread prima di qualsiasi successivo accesso alla memoria \# g da parte di questo \# thread.

Ciò si applica a tutta la memoria condivisa g del gruppo di thread \# corrente.

\_g è disponibile solo nello shader di calcolo.

### <a name="_t"></a>\_t

Sincronizzazione del gruppo di thread. Tutti i thread all'interno di un singolo gruppo di thread (quelli che possono condividere l'accesso a un set comune di spazio di registro condiviso) verranno eseguiti fino al punto in cui raggiungono questa istruzione prima che qualsiasi thread possa continuare.

\_t non può essere inserito nel controllo dinamico del flusso (rami che possono variare all'interno di un gruppo di thread), ma può essere presente in un controllo di flusso uniforme, in cui tutti i thread nel gruppo selezionano lo stesso percorso.

\_t è disponibile solo nello shader di calcolo.

Di seguito è riportato un elenco delle varianti di "sincronizzazione" dello shader di calcolo.

-   sync \_ g
-   sync \_ ugroup\*
-   sincronizzare \_ uglobal
-   sync \_ g \_ t
-   sync \_ ugroup \_ t\*
-   sincronizzare \_ uglobal \_ t
-   sync \_ ugroup \_ g\*
-   sincronizzare \_ uglobal \_ g
-   sync \_ ugroup \_ g \_ t\*
-   sincronizzare \_ uglobal \_ g \_ t

\*Le varianti con ugroup potrebbero non essere destinate dal compilatore HLSL, come descritto in precedenza nella sezione \_ \_ ugroup precedente.

L'elenco pixel shader varianti di sincronizzazione includono solo \_ l'uglobal di sincronizzazione.

I recinti di memoria impediscono che le istruzioni interessate vengano riordinate dai compilatori o dall'hardware attraverso il recinto.

È possibile comprimere più operazioni di lettura dallo stesso indirizzo tramite una chiamata dello shader non separate da barriere di memoria o scritture nell'indirizzo. Lo stesso vale per le operazioni di scrittura. Gli accessi separati da una barriera non possono essere uniti o spostati attraverso la barriera.

I recinti di memoria non sono necessari per il corretto funzionamento delle operazioni atomiche a un determinato indirizzo da parte di thread diversi. I recinti sono necessari quando le operazioni atomiche e/o di caricamento/archiviazione devono essere sincronizzate l'una rispetto all'altra come appaiono nei singoli thread dal punto di vista di altri thread.

Nell'pixel shader, le istruzioni [discard](discard--sm4---asm-.md) implicano un recinto uglobal di sincronizzazione, in cui le istruzioni non possono essere riordinate \_ **nell'oggetto discard.** la sincronizzazione di uglobal in pixel helper (che vengono eseguiti solo per supportare i derivati) o i pixel eliminati possono avere \_ o meno alcun effetto. Non è consentito che i pixel helper o eliminati scrivono in UAV se, nel caso di discard, le scritture vengono rilasciate dopo l'eliminazione. I valori restituiti dagli UAV non possono contribuire ai calcoli derivati. Di conseguenza, la sincronizzazione u viene rispettata per i pixel helper o \_ quando viene emessa dopo un discard.

Cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché gli UAV sono disponibili in tutte le fasi dello shader per Direct3D 11.1, la variante **\_ uglobal** di sincronizzazione di questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11.1, disponibile a partire da Windows 8.



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




