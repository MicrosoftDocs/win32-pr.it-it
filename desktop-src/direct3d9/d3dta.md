---
description: "Le costanti dell'argomento Texture vengono usate come valori per i membri seguenti del tipo enumerato D3DTEXTURESTAGESTATETYPE:"
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db520bee7e4352b3242824819cc579acd82b1d013d290b2155d54170bc478c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527315"
---
# <a name="d3dta"></a>D3DTA

Le costanti dell'argomento Texture vengono usate come valori per i membri seguenti del [**tipo enumerato D3DTEXTURESTAGESTATETYPE:**](./d3dtexturestagestatetype.md)

-   D3DTSS \_ ALPHAARG0
-   D3DTSS \_ ALPHAARG1
-   D3DTSS \_ ALPHAARG2
-   D3DTSS \_ COLORARG0
-   D3DTSS \_ COLORARG1
-   D3DTSS \_ COLORARG2
-   D3DTSS \_ RESULTARG

Impostare e recuperare gli argomenti della trama chiamando [**i metodi SetTextureStageState**](/windows/desktop/api) [**e GetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)

Flag di argomento

È possibile combinare un flag di argomento con un modificatore, ma non è possibile combinare due flag di argomento.



| \#Definire          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COSTANTE D3DTA \_   | Selezionare una costante da una fase della trama. Il valore predefinito è 0xffffffff.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| D3DTA \_ CURRENT    | L'argomento texture è il risultato della fase di fusione precedente. Nella prima fase della trama (fase 0), questo argomento è equivalente a D3DTA \_ DIFFUSE. Se la fase di fusione precedente usa una trama della mappa di rilievo (operazione D3DTOP BUMPENVMAP), il sistema sceglie la trama dalla fase prima della trama della mappa di \_ rilievo. Se s rappresenta la fase della trama corrente e s - 1 contiene una trama della mappa di urto, questo argomento diventa l'output del risultato dalla fase della trama s - 2. Le autorizzazioni sono di lettura/scrittura. |
| D3DTA \_ DIFFUSE    | L'argomento texture è il colore diffuso interpolato dai componenti dei vertici durante l'ombreggiatura Gouraud. Se il vertice non contiene un colore diffuso, il colore predefinito è 0xffffffff. Le autorizzazioni sono di sola lettura.                                                                                                                                                                                                                                                                                          |
| D3DTA \_ SELECTMASK | Mascherare il valore per tutti gli argomenti; non viene usato quando si impostano gli argomenti della trama.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| D3DTA \_ SPECULAR   | L'argomento texture è il colore speculare interpolato dai componenti dei vertici durante l'ombreggiatura gouraud. Se il vertice non contiene un colore speculare, il colore predefinito è 0xffffffff. Le autorizzazioni sono di sola lettura.                                                                                                                                                                                                                                                                                        |
| D3DTA \_ TEMP       | L'argomento texture è un colore di registro temporaneo per la lettura o la scrittura. D3DTA TEMP è supportato se è presente la funzionalità del dispositivo \_ [D3DPMISCCAPS \_ TSSARGTEMP.](d3dpmisccaps.md) Il valore predefinito per il registro è (0.0, 0.0, 0.0, 0.0). Le autorizzazioni sono di lettura/scrittura.                                                                                                                                                                                                                                   |
| TRAMA D3DTA \_    | L'argomento texture è il colore della trama per questa fase della trama. Le autorizzazioni sono di sola lettura.                                                                                                                                                                                                                                                                                                                                                                                                               |
| D3DTA \_ TFACTOR    | L'argomento texture è il fattore di trama impostato in una chiamata precedente a [**SetRenderState**](/windows/desktop/api) con il valore dello stato di rendering [**\_ TEXTUREFACTOR D3DRS.**](./d3drenderstatetype.md) Le autorizzazioni sono di sola lettura.                                                                                                                                                                                                                                                       |



 

Flag di modifica

Un flag di argomento può essere combinato con uno dei flag di modifica seguenti.



| \#Definire              | Descrizione                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| D3DTA \_ ALPHAREPLICATE | Replicare le informazioni alfa in tutti i canali di colore prima del completamento dell'operazione. Si tratta di un modificatore di lettura. |
| COMPLEMENTO D3DTA \_     | Accetta il complemento dell'argomento x, (1.0 - x). Si tratta di un modificatore di lettura.                                     |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|   Requisito                       |  Valore           |
|--------------------------|-------------|
| Intestazione                   | d3d9types.h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
