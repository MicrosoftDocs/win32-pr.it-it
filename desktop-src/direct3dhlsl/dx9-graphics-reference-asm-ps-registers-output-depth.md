---
title: Registro profondità output
description: Il registro di profondità dell'output pixel shader (oDepth) è un registro scalare di sola scrittura con l'intervallo \ 0.. 1 \ che restituisce un nuovo valore di profondità per un test di profondità sul buffer di stencil di profondità.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332604"
---
# <a name="output-depth-register"></a>Registro profondità output

Il registro di profondità dell'output pixel shader (oDepth) è un registro scalare di sola scrittura con l'intervallo \[ 0.. 1 \] che restituisce un nuovo valore di profondità per un test di profondità sul buffer dello stencil di profondità.

Sintassi



| oDepth |
|--------|



 

Dove:



| Nome   | Descrizione                                                       |
|--------|-------------------------------------------------------------------|
| oDepth | Nuovo valore di profondità per un test di profondità sul buffer di stencil Depth |



 

È importante tenere presente che la scrittura in oDepth causa la perdita di tutti gli algoritmi di ottimizzazione del buffer di profondità specifici dell'hardware (ovvero la Z gerarchica) che accelerano le prestazioni dei test di profondità.

La replica di swizzle di origine (con estensione x. \| \| z. \| w) è obbligatoria quando si scrive in oDepth. Non sono consentite maschere di scrittura esplicite.

La scrittura nel registro oDepth sostituisce il valore di profondità interpolata (ignorando eventuali distorsioni di profondità/slopescale renderstates). Se non è stato creato o collegato alcun buffer di profondità al dispositivo, la scrittura in oDepth viene ignorata.

Se si esegue il campionamento multiplo e si scrive in oDepth, poiché il pixel shader viene eseguito una sola volta per pixel, il valore di profondità viene replicato per tutte le posizioni sottocampionate coperte. Il test di profondità si verifica ancora per campione, ma non è presente un valore di profondità per campione che entra nel confronto dal pixel shader come se non fosse stato scritto oDepth.

Se un'applicazione dispone di un w-buffer impostato come buffer di profondità, è necessario prenderlo in considerazione durante la scrittura in oDepth. Potrebbe potenzialmente dover inviare informazioni di intervallo w al pixel shader e calcolare l'intervallo w per ridimensionare i valori w scritti in oDepth.

### <a name="ps_2_0-and-ps_2_x-restrictions"></a>\_restrizioni PS 2 \_ 0 e PS \_ 2 \_ x

-   oDepth può essere scritto solo con l'istruzione [MOV-PS](mov---ps.md) e può essere eseguito solo una volta.
-   Non è consentito alcun modificatore di origine durante la scrittura in oDepth.
-   Nessun modificatore di istruzione consentito durante la scrittura in oDepth.
-   Nessuna scrittura in oDepth dall'interno di un costrutto di controllo di flusso o quando si usa predicazione.

### <a name="ps_3_0-restrictions"></a>Restrizioni di PS \_ 3 \_ 0

-   Per PS \_ 3 \_ 0, i registri di output OC # e od \# possono essere scritti un numero qualsiasi di volte. L'output del pixel shader deriva dal contenuto dei registri di output alla fine dell'esecuzione dello shader. Se non si verifica una scrittura in un registro di output, probabilmente a causa del controllo di flusso o se lo shader non lo scrive, non viene aggiornata anche la destinazione di rendering corrispondente. Se viene scritto un subset dei canali in un registro di output, i valori non definiti verranno scritti nei canali rimanenti.
-   È possibile scrivere in oDepth all'interno del controllo di flusso o predicazione a condizione che tutti i percorsi possibili vengano scritti nel registro.
-   Non è possibile eseguire alcun calcolo sfumato (o operazioni che richiamano in modo implicito i calcoli delle sfumature, ad esempio [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) all'interno delle istruzioni di controllo di flusso le cui condizioni di diramazione variano in base alle primitive (ad esempio, istruzioni di controllo dinamico del flusso). L'istruzione predicazione non è considerata il controllo dinamico del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




