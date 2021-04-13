---
title: Fase input-assembler
description: L'API Direct3D 10 e versioni successive separa le aree funzionali della pipeline in fasi. la prima fase della pipeline è la fase di input-assembler (IA).
ms.assetid: 71141a5e-2d79-4b02-8370-c0cbc8618908
keywords:
- fase assembler input (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121d98ca66bbe42f6eaa3023150203ce0538445b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399973"
---
# <a name="input-assembler-stage"></a>Fase input-assembler

L'API Direct3D 10 e versioni successive separa le aree funzionali della pipeline in fasi. la prima fase della pipeline è la fase di input-assembler (IA).

Lo scopo della fase input-assembler è leggere i dati primitivi (punti, linee e/o triangoli) dai buffer riempiti dall'utente e assemblare i dati nelle primitive che verranno usate dalle altre fasi della pipeline. La fase IA può assemblare i vertici in più [tipi primitivi](d3d10-graphics-programming-guide-primitive-topologies.md) diversi, ad esempio elenchi di righe, strisce triangolari o primitive con adiacenza. Sono stati aggiunti nuovi tipi primitivi, ad esempio un elenco di linee con adiacenza o un elenco di triangolo con adiacenza, per supportare il geometry shader.

Le informazioni adiacenza sono visibili a un'applicazione solo in un geometry shader. Se un geometry shader è stato richiamato con un triangolo che include adiacenza, ad esempio, i dati di input contengono 3 vertici per ogni triangolo e 3 vertici per i dati adiacenza per triangolo.

Quando viene richiesta la fase input-assembler per l'output dei dati di adiacenza, i dati di input devono includere i dati adiacenza. Potrebbe essere necessario fornire un vertice fittizio (formando un triangolo degenerato) oppure contrassegnando uno degli attributi dei vertici se il vertice esiste o meno. Questa operazione dovrebbe anche essere rilevata e gestita da un geometry shader, anche se l'abbattimento della geometria degenerata verrà eseguita nella fase di rasterizzazione.

Durante l'assemblaggio di primitive, uno scopo secondario dell'IA consiste nell'alleghire [i valori generati dal sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) per rendere più efficienti gli shader. I valori generati dal sistema sono stringhe di testo denominate anche semantica. Tutte e tre le fasi dello shader sono costruite da un core shader comune e il nucleo dello shader usa i valori generati dal sistema, ad esempio un ID primitivo, un ID istanza o un ID vertice, in modo che una fase shader possa ridurre l'elaborazione solo a quelle primitive, istanze o vertici che non sono già state elaborate.

Come illustrato nel [diagramma di blocco della pipeline](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages), una volta che la fase IA legge i dati dalla memoria (assembla i dati in primitive e connette i valori generati dal sistema), i dati vengono restituiti alla [fase vertex shader](/previous-versions//bb205146(v=vs.85)).


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introduzione con la fase di Input-Assembler](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)<br/> | Sono necessari alcuni passaggi per inizializzare la fase di input-assembler (IA). Ad esempio, è necessario creare risorse del buffer con i dati dei vertici necessari per la pipeline, indicare la fase IA in cui si trovano i buffer e il tipo di dati che contengono e specificare il tipo di primitive da assemblare dai dati.<br/> |
| [Topologie primitive](d3d10-graphics-programming-guide-primitive-topologies.md)<br/>                                            | Direct3D 10 e versioni successive supporta diversi tipi primitivi (o topologie) rappresentati dal tipo enumerato della [**\_ \_ topologia primitiva D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) . Questi tipi definiscono il modo in cui i vertici vengono interpretati e sottoposti a rendering dalla pipeline.<br/>                                                          |
| [Uso della fase Input-Assembler senza buffer](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)<br/>     | La creazione e l'associazione dei buffer non sono necessari se gli shader non richiedono buffer. Questa sezione contiene un esempio di semplici Vertex e pixel shader che delineano un singolo triangolo.<br/>                                                                                                                                  |
| [Utilizzo di valori System-Generated](d3d10-graphics-programming-guide-input-assembler-stage-using.md)<br/>                            | I valori generati dal sistema vengono generati dalla fase IA (in base alla [semantica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)di input fornita dall'utente) per consentire una certa efficienza nelle operazioni dello shader. <br/>                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

