---
title: Output Depth Register
description: Il registro di profondità di output di pixel shader (oDepth) è un registro scalare di sola scrittura con l'intervallo \ 0..1\ che restituisce un nuovo valore di profondità per un test di profondità rispetto al buffer depth-stencil.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 041ffccb3301831c91554ef3cda835d3f2e79204730e838b25f26660e76d9a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119725"
---
# <a name="output-depth-register"></a>Output Depth Register

Il registro di profondità di output di pixel shader (oDepth) è un registro scalare di sola scrittura con intervallo 0..1 che restituisce un nuovo valore di profondità per un test di profondità rispetto al \[ \] buffer depth-stencil.

Sintassi



| oDepth |
|--------|



 

Dove:



| Nome   | Descrizione                                                       |
|--------|-------------------------------------------------------------------|
| oDepth | Nuovo valore di profondità per un test di profondità rispetto al buffer depth-stencil |



 

È importante tenere presente che la scrittura in oDepth causa la perdita di qualsiasi algoritmo di ottimizzazione del buffer di profondità specifico dell'hardware (ad esempio Z gerarchico) che accelera le prestazioni dei test di profondità.

Lo swizzle di origine di replica (.x \| \| .y .z \| .w) è obbligatorio durante la scrittura in oDepth. Le maschere di scrittura esplicite non sono consentite.

La scrittura nel registro oDepth sostituisce il valore di profondità interpolata e ignora eventuali stati di rendering di distorsione/inclinazione della profondità. Se non è stato creato alcun buffer di profondità o collegato al dispositivo, la scrittura in oDepth viene ignorata.

Se si esegue il multicampionamento e si scrive in oDepth, poiché il pixel shader viene eseguito solo una volta per pixel, il valore di profondità viene replicato per tutte le posizioni di sottocampionamento coperte. Il test di profondità viene comunque eseguito per ogni campione, ma non si ha un valore di profondità per campione nel confronto dal pixel shader come si farebbe se non si scrivesse oDepth.

Se un'applicazione ha un buffer w impostato come buffer di profondità, è necessario prenderne in considerazione durante la scrittura in oDepth. È potenzialmente necessario inviare informazioni w-range al pixel shader e calcolare l'intervallo w per ridimensionare i valori w scritti in oDepth.

### <a name="ps_2_0-and-ps_2_x-restrictions"></a>ps \_ 2 \_ 0 e ps \_ 2 \_ x Restrizioni

-   oDepth può essere scritto solo con [l'istruzione mov - ps](mov---ps.md) e può essere eseguito una sola volta.
-   Durante la scrittura in oDepth non è consentito alcun modificatore di origine.
-   Durante la scrittura in oDepth non è consentito alcun modificatore di istruzione.
-   Nessuna scrittura in oDepth dall'interno di un costrutto di controllo di flusso o quando si usa la predicazione.

### <a name="ps_3_0-restrictions"></a>Ps \_ 3 \_ 0 Restrizioni

-   Per ps \_ 3 \_ 0, i registri di output oC# e oD \# possono essere scritti un numero qualsiasi di volte. L'output del pixel shader deriva dal contenuto dei registri di output alla fine dell'esecuzione dello shader. Se non si verifica una scrittura in un registro di output, ad esempio a causa del controllo di flusso o se lo shader non lo ha appena scritto, anche la destinazione di rendering corrispondente non viene aggiornata. Se viene scritto un subset dei canali in un registro di output, i valori non definiti verranno scritti nei canali rimanenti.
-   È possibile scrivere in oDepth all'interno del controllo di flusso o della predicazione, purché tutti i percorsi possibili scrivono nel registro.
-   Non è possibile eseguire calcoli delle sfumature (o operazioni che richiamano in modo implicito i calcoli delle sfumature, ad esempio [texld - ps \_ 2 \_ 0](texld---ps-2-0.md)e up , [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) all'interno di istruzioni di controllo di flusso le cui condizioni di diramazione variano in base alle primitive (ad esempio, istruzioni di controllo dinamico del flusso). Il predicato dell'istruzione non è considerato controllo dinamico del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




