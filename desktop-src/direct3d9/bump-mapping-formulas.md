---
description: Direct3D applica le formule seguenti ai componenti DU e DV in ogni pixel della mappa Bump.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Formule di mapping di Bump (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127779"
---
# <a name="bump-mapping-formulas-direct3d-9"></a><span data-ttu-id="6a092-103">Formule di mapping di Bump (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6a092-103">Bump Mapping Formulas (Direct3D 9)</span></span>

<span data-ttu-id="6a092-104">Direct3D applica le formule seguenti ai componenti D<sub>U</sub> e d<sub>V</sub> in ogni pixel della mappa.</span><span class="sxs-lookup"><span data-stu-id="6a092-104">Direct3D applies the following formulas to the D<sub>U</sub> and D<sub>V</sub> components in each bump map pixel.</span></span>

![formule di trasformazioni di matrici di mapping Bump](images/dudv-transform.png)

<span data-ttu-id="6a092-106">In queste formule, le variabili D<sub>u</sub> e d<sub>v</sub> vengono ricavate direttamente da un pixel della mappa a urto e trasformate da una matrice 2x2 per produrre i valori delta di output D<sub>U</sub>"e d<sub>V</sub>".</span><span class="sxs-lookup"><span data-stu-id="6a092-106">In these formulas, the D<sub>U</sub> and D<sub>V</sub> variables are taken directly from a bump map pixel and transformed by a 2x2 matrix to produce the output delta values D<sub>U</sub>' and D<sub>V</sub>'.</span></span> <span data-ttu-id="6a092-107">Il sistema usa i valori di output per modificare le coordinate di trama che indirizzano la mappa dell'ambiente nella fase di trama successiva.</span><span class="sxs-lookup"><span data-stu-id="6a092-107">The system uses the output values to modify the texture coordinates that address the environment map in the next texture stage.</span></span> <span data-ttu-id="6a092-108">I coefficienti della matrice di trasformazione vengono impostati tramite gli \_ Stati della fase della trama D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 e D3DTSS BUMPENVMAT11 \_ .</span><span class="sxs-lookup"><span data-stu-id="6a092-108">The coefficients of the transformation matrix are set though the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT10, D3DTSS\_BUMPENVMAT01, and D3DTSS\_BUMPENVMAT11 texture stage states.</span></span>

<span data-ttu-id="6a092-109">Oltre ai valori Delta utente e v, il sistema è in grado di calcolare un valore di luminanza utilizzato per modulare il colore della mappa dell'ambiente nella fase di Blend successiva, come illustrato nella formula seguente.</span><span class="sxs-lookup"><span data-stu-id="6a092-109">In addition to the u and v delta values, the system can compute a luminance value that it uses to modulate the color of the environment map in the next blending stage, as shown in the following formula.</span></span>

![formula per la luminanza di output, calcolata dal fattore di scala e dall'offset](images/l-transform.png)

<span data-ttu-id="6a092-111">In questa formula, L'è la luminanza di output calcolata.</span><span class="sxs-lookup"><span data-stu-id="6a092-111">In this formula, L' is the output luminance being computed.</span></span> <span data-ttu-id="6a092-112">La variabile L è il valore di luminanza tratto da un pixel della mappa Bump, moltiplicato per il fattore di scala, S e offset in base al valore nella variabile O. Gli \_ Stati della fase D3DTSS BUMPENVLSCALE e D3DTSS \_ BUMPENVLOFFSET texture controllano i valori per le variabili S e O nella formula.</span><span class="sxs-lookup"><span data-stu-id="6a092-112">The L variable is the luminance value taken from a bump map pixel, which is multiplied by the scaling factor, S, and offset by the value in the variable O. The D3DTSS\_BUMPENVLSCALE and D3DTSS\_BUMPENVLOFFSET texture stage states control the values for the S and O variables in the formula.</span></span> <span data-ttu-id="6a092-113">Questa formula viene applicata solo quando l'operazione di combinazione di trame per la fase che contiene la mappa Bump è impostata su D3DTOP \_ BUMPENVMAPLUMINANCE.</span><span class="sxs-lookup"><span data-stu-id="6a092-113">This formula is only applied when the texture blending operation for the stage that contains the bump map is set to D3DTOP\_BUMPENVMAPLUMINANCE.</span></span> <span data-ttu-id="6a092-114">Quando si usa D3DTOP \_ BUMPENVMAP, il sistema usa un valore di 1,0 per L.</span><span class="sxs-lookup"><span data-stu-id="6a092-114">When using D3DTOP\_BUMPENVMAP, the system uses a value of 1.0 for L'.</span></span>

<span data-ttu-id="6a092-115">Dopo aver calcolato i valori delta di output D<sub>U</sub>e d<sub>V</sub>, il sistema li aggiunge alle coordinate di trama nella successiva fase della trama e modula il colore scelto dalla luminanza per produrre il colore applicato al poligono.</span><span class="sxs-lookup"><span data-stu-id="6a092-115">After computing the output delta values D<sub>U</sub>' and D<sub>V</sub>', the system adds them to the texture coordinates in the next texture stage, and modulates the chosen color by the luminance to produce the color applied to the polygon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a092-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a092-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a092-117">Bump mapping</span><span class="sxs-lookup"><span data-stu-id="6a092-117">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



