---
description: Opzioni di compilazione HLSL.
ms.assetid: vs|directx_sdk|~\d3d10_shader.htm
title: D3D10_SHADER costanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e965c050d3643e80b493875b27ba5a9b774b351487e191584f40297819758f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303524"
---
# <a name="d3d10_shader-constants"></a>Costanti D3D10 \_ SHADER

Opzioni di compilazione HLSL.



| \#Definire                                        | Descrizione                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ SHADER \_ AVOID \_ FLOW \_ CONTROL             | Indicare al compilatore di non consentire il controllo di flusso (quando possibile).                                                                                                                                                                                       |
| DEBUG DELLO SHADER D3D10 \_ \_                            | Inserire informazioni sul file/riga/tipo/simbolo di debug.                                                                                                                                                                                                |
| D3D10 \_ SHADER \_ ENABLE \_ STRICTNESS               | Per impostazione predefinita, il compilatore HLSL disabilita la rigidità nella sintassi deprecata. Se si specifica questo flag, viene abilitata la rigidità che potrebbe non consentire la sintassi legacy.                                                                                         |
| D3D10 \_ SHADER ABILITA LA \_ \_ COMPATIBILITÀ CON LE VERSIONI \_ PRECEDENTI | Ciò consente agli shader meno recenti di compilare fino a 4 \_ destinazioni 0.                                                                                                                                                                                         |
| D3D10 \_ SHADER \_ FORCE \_ VS \_ SOFTWARE \_ NO \_ OPT     | Compilare un vertex shader per il profilo shader più alto successivo. Questa opzione attiva il debug (e le ottimizzazioni sono disattivate).                                                                                                                           |
| D3D10 \_ SHADER \_ FORCE \_ PS \_ SOFTWARE \_ NO \_ OPT     | Compilare un pixel shader per il profilo shader più alto successivo. Questa opzione attiva il debug (e le ottimizzazioni sono disattivate).                                                                                                                            |
| D3D10 \_ SHADER \_ IEEE \_ STRICTNESS                 | Abilita la rigidità IEEE.                                                                                                                                                                                                                       |
| D3D10 \_ SHADER \_ NO \_ PRESHADER                    | Disabilita i preshader. Se si usa questo flag, il compilatore non estrae l'espressione statica per la valutazione.                                                                                                                                 |
| LIVELLO DI OTTIMIZZAZIONE \_ DELLO SHADER D3D10000 \_ \_             | Livello di ottimizzazione più basso. Può produrre codice più lento, ma lo farà più rapidamente. Questo può essere utile in un ciclo di sviluppo shader altamente iterativo.                                                                                             |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL1             | Secondo livello di ottimizzazione più basso.                                                                                                                                                                                                              |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL2             | Secondo livello di ottimizzazione più alto.                                                                                                                                                                                                             |
| LIVELLO DI OTTIMIZZAZIONE DELLO SHADER D3D103 \_ \_ \_             | Livello di ottimizzazione più alto. Produrrà il codice migliore possibile, ma potrebbe richiedere molto più tempo. Ciò sarà utile per le compilazioni finali di un'applicazione in cui le prestazioni sono il fattore più importante.                                 |
| D3D10 \_ SHADER PACK MATRICE ROW \_ \_ \_ \_ MAJOR         | A meno che non vengano specificate in modo esplicito, le matrici verranno imballate in ordine principale di riga in base all'input e all'output dello shader.                                                                                                                                   |
| D3D10 \_ SHADER \_ PACK \_ MATRIX \_ COLUMN \_ MAJOR      | A meno che non vengano specificate in modo esplicito, le matrici verranno imballate nell'ordine principale della colonna in base all'input e all'output dello shader. Questa operazione è in genere più efficiente, perché consente di eseguire la moltiplicazione di matrice vettoriale usando una serie di prodotti a punti. |
| PRECISIONE PARZIALE DELLO SHADER D3D10 \_ \_ \_               | Forzare l'esecuzione di tutti i calcoli con precisione parziale. questa operazione può essere eseguita più velocemente in alcuni componenti hardware.                                                                                                                                                |
| D3D10 \_ SHADER PREFERISCE IL CONTROLLO DI \_ \_ \_ FLUSSO            | Indicare al compilatore di usare il controllo di flusso (quando possibile).                                                                                                                                                                                             |
| OTTIMIZZAZIONE SKIP DELLO SHADER D3D10 \_ \_ \_               | Ignorare l'ottimizzazione durante la generazione del codice; in genere consigliato solo per il debug.                                                                                                                                                                |
| CONVALIDA SKIP DELLO SHADER D3D10 \_ \_ \_                 | Non convalidare il codice generato in base alle funzionalità e ai vincoli noti. Usare questa opzione solo con gli shader compilati correttamente in passato. Gli shader vengono sempre convalidati da DirectX prima di essere impostati sul dispositivo.         |
| GLI AVVISI DELLO SHADER D3D10 \_ \_ SONO \_ \_ ERRORI            | Informare il compilatore HLSL di considerare tutti gli avvisi come errori durante la compilazione del codice shader. Per il nuovo codice shader, è consigliabile usare questa opzione in modo da poter risolvere tutti gli avvisi e garantire il numero minimo di difetti di codice difficili da trovare.             |



 

Queste costanti sono definite come macro in d3d10shader.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti shader](d3d10-graphics-reference-d3d10-shader-constants.md)
</dt> </dl>

 

 



