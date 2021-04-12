---
description: Opzioni di compilazione HLSL.
ms.assetid: vs|directx_sdk|~\d3d10_shader.htm
title: Costanti D3D10_SHADER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16480e2aceada7f5ed05912eca59cc88886ac9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483581"
---
# <a name="d3d10_shader-constants"></a>\_Costanti shader D3D10

Opzioni di compilazione HLSL.



| \#definire                                        | Descrizione                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ shader per \_ evitare \_ il \_ controllo di flusso             | Indica al compilatore di non consentire il controllo del flusso (quando possibile).                                                                                                                                                                                       |
| \_Debug dello shader \_ D3D10                            | Inserire le informazioni relative al file di debug, alla riga, al tipo o al simbolo.                                                                                                                                                                                                |
| D3D10 \_ shader \_ Abilita la \_ rigorosità               | Per impostazione predefinita, il compilatore HLSL Disabilita la limitazione della sintassi deprecata. La specifica di questo flag Abilita la rigidità che potrebbe non consentire la sintassi legacy.                                                                                         |
| D3D10 \_ shader Abilita la compatibilità con le \_ \_ versioni precedenti \_ | In questo modo gli shader meno recenti vengono compilati in 4 \_ 0 destinazioni.                                                                                                                                                                                         |
| D3D10 \_ shader \_ Force \_ vs \_ software \_ No \_ opt     | Compila un vertex shader per il profilo shader più alto successivo. Questa opzione attiva il debug (e le ottimizzazioni non sono disponibili).                                                                                                                           |
| D3D10 \_ shader \_ Force \_ PS \_ software \_ No \_ opt     | Compilare un pixel shader per il profilo shader più alto successivo. Questa opzione attiva il debug (e le ottimizzazioni non sono disponibili).                                                                                                                            |
| \_ \_ Limitazione IEEE dello shader \_ D3D10                 | Abilita la rigidità IEEE.                                                                                                                                                                                                                       |
| D3D10 \_ shader \_ senza \_ preshader                    | Disabilita i preshader. Se si usa questo flag, il compilatore non estrae l'espressione statica per la valutazione.                                                                                                                                 |
| \_Ottimizzazione D3D10 shader \_ \_ level0             | Livello di ottimizzazione più basso. Può produrre codice più lento, ma sarà più rapido. Questa operazione può essere utile in un ciclo di sviluppo di shader altamente iterativo.                                                                                             |
| \_Ottimizzazione D3D10 shader \_ \_ Level1             | Secondo livello di ottimizzazione più basso.                                                                                                                                                                                                              |
| \_Ottimizzazione D3D10 shader \_ \_ Level2             | Secondo livello di ottimizzazione più alto.                                                                                                                                                                                                             |
| \_Ottimizzazione D3D10 shader \_ \_ Level3             | Livello massimo di ottimizzazione. Produrrà il migliore codice possibile, ma potrebbe richiedere molto più tempo. Questa operazione sarà utile per le compilazioni finali di un'applicazione in cui le prestazioni sono il fattore più importante.                                 |
| D3D10 \_ shader \_ pack \_ matrice \_ riga \_ principale         | A meno che non venga specificato in modo esplicito, le matrici verranno compresse in ordine di riga, in base all'input e all'output dello shader.                                                                                                                                   |
| D3D10 \_ \_ \_ colonna matrice di matrici \_ shader \_      | A meno che non venga specificato in modo esplicito, le matrici verranno compresse in base all'ordine delle colonne nell'input e nell'output dello shader. Questa operazione è in genere più efficiente, in quanto consente di eseguire la moltiplicazione di matrici di vettori usando una serie di prodotti punto. |
| \_ \_ Precisione parziale dello shader \_ D3D10               | Forzare l'esecuzione di tutti i calcoli con precisione parziale; Questa operazione può essere eseguita più velocemente su hardware.                                                                                                                                                |
| D3D10 \_ shader \_ preferisce il \_ controllo di flusso \_            | Indicare al compilatore di usare il controllo di flusso (quando possibile).                                                                                                                                                                                             |
| \_ \_ Ottimizzazione ignora D3D10 shader \_               | Ignora ottimizzazione durante la generazione del codice; generalmente consigliato solo per il debug.                                                                                                                                                                |
| D3D10 lo \_ shader \_ Ignora la \_ convalida                 | Non convalidare il codice generato in base alle funzionalità note e ai vincoli. Utilizzare questa operazione solo con gli shader che sono stati compilati correttamente in precedenza. Gli shader vengono sempre convalidati da DirectX prima che siano impostati sul dispositivo.         |
| Gli \_ avvisi di D3D10 shader \_ \_ sono \_ errori            | Informare il compilatore HLSL di considerare tutti gli avvisi come errori durante la compilazione del codice dello shader. Per il nuovo codice shader, è consigliabile usare questa opzione per poter risolvere tutti gli avvisi e garantire il minor numero possibile di errori del codice di difficile individuazione.             |



 

Queste costanti sono definite come macro in d3d10shader. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti shader](d3d10-graphics-reference-d3d10-shader-constants.md)
</dt> </dl>

 

 



