---
description: 'Le costanti degli argomenti di trama vengono usate come valori per i membri seguenti del tipo enumerato D3DTEXTURESTAGESTATETYPE:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58d4d5665b1a098b84eaa95294e69220d6ea4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305186"
---
# <a name="d3dta"></a>D3DTA

Le costanti degli argomenti di trama vengono usate come valori per i membri seguenti del tipo enumerato [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) :

-   \_ALPHAARG0 D3DTSS
-   \_ALPHAARG1 D3DTSS
-   \_ALPHAARG2 D3DTSS
-   \_COLORARG0 D3DTSS
-   \_COLORARG1 D3DTSS
-   \_COLORARG2 D3DTSS
-   \_RESULTARG D3DTSS

Impostare e recuperare gli argomenti di trama chiamando i metodi [**SetTextureStageState**](/windows/desktop/api) e [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) .

Flag di argomento

È possibile combinare un flag di argomento con un modificatore, ma non è possibile combinare due flag di argomento.



|                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_Costante D3DTA   | Selezionare una costante da una fase della trama. Il valore predefinito è 0xFFFFFFFF.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| D3DTA \_ corrente    | L'argomento trama è il risultato della fase di fusione precedente. Nella prima fase della trama (fase 0), questo argomento è equivalente a D3DTA \_ Diffusion. Se la fase di fusione precedente usa una trama con mappa Bump (l' \_ operazione D3DTOP BUMPENVMAP), il sistema sceglie la trama dalla fase prima della trama del bump-map. Se s rappresenta la fase della trama corrente e s-1 contiene una trama con mappa Bump, questo argomento diventa l'output del risultato in base alla fase di trama s-2. Le autorizzazioni sono di lettura/scrittura. |
| D3DTA \_ diffuse    | L'argomento trama è il colore diffuso interpolato dai componenti del vertice durante l'ombreggiatura Gouraud. Se il vertice non contiene un colore diffuso, il colore predefinito è 0xFFFFFFFF. Le autorizzazioni sono di sola lettura.                                                                                                                                                                                                                                                                                          |
| \_SELECTMASK D3DTA | Valore della maschera per tutti gli argomenti; non utilizzato quando si impostano argomenti di trama.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| D3DTA \_ speculare   | L'argomento trama è il colore speculare interpolato dai componenti del vertice durante l'ombreggiatura Gouraud. Se il vertice non contiene un colore speculare, il colore predefinito è 0xFFFFFFFF. Le autorizzazioni sono di sola lettura.                                                                                                                                                                                                                                                                                        |
| D3DTA \_ Temp       | L'argomento trama è un colore di registro temporaneo per la lettura o la scrittura. D3DTA \_ Temp è supportato se è presente la funzionalità del dispositivo [D3DPMISCCAPS \_ TSSARGTEMP](d3dpmisccaps.md) . Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0). Le autorizzazioni sono di lettura/scrittura.                                                                                                                                                                                                                                   |
| \_Trama D3DTA    | L'argomento texture è il colore della trama per questa fase della trama. Le autorizzazioni sono di sola lettura.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_TFACTOR D3DTA    | L'argomento trama è il fattore di trama impostato in una chiamata precedente a [**SetRenderState**](/windows/desktop/api) con il valore di stato di rendering [**D3DRS \_ TEXTUREFACTOR**](./d3drenderstatetype.md) . Le autorizzazioni sono di sola lettura.                                                                                                                                                                                                                                                       |



 

Flag di modifica

Un flag di argomento può essere combinato con uno dei flag di modifica seguenti.



|                       |                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| \#definire              | Descrizione                                                                                                    |
| \_ALPHAREPLICATE D3DTA | Replicare le informazioni alfa in tutti i canali di colore prima del completamento dell'operazione. Si tratta di un modificatore Read. |
| \_Complemento D3DTA     | Eseguire il complemento dell'argomento x, (1,0-x). Si tratta di un modificatore Read.                                     |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |             |
|--------------------------|-------------|
| Intestazione                   | d3d9types. h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
