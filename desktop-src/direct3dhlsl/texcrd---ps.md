---
title: texcrd-PS
description: Copia i dati delle coordinate di trama dal registro iteratore delle coordinate di trama di origine come dati di colore nel registro di destinazione.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993400"
---
# <a name="texcrd---ps"></a><span data-ttu-id="77660-103">texcrd-PS</span><span class="sxs-lookup"><span data-stu-id="77660-103">texcrd - ps</span></span>

<span data-ttu-id="77660-104">Copia i dati delle coordinate di trama dal registro iteratore delle coordinate di trama di origine come dati di colore nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="77660-104">Copies texture coordinate data from the source texture coordinate iterator register as color data in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="77660-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77660-105">Syntax</span></span>



| <span data-ttu-id="77660-106">texcrd DST, src</span><span class="sxs-lookup"><span data-stu-id="77660-106">texcrd dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="77660-107">dove</span><span class="sxs-lookup"><span data-stu-id="77660-107">where</span></span>

-   <span data-ttu-id="77660-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="77660-108">dst is the destination register.</span></span>
-   <span data-ttu-id="77660-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="77660-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="77660-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="77660-110">Remarks</span></span>



| <span data-ttu-id="77660-111">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="77660-111">Pixel shader versions</span></span> | <span data-ttu-id="77660-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="77660-112">1\_1</span></span> | <span data-ttu-id="77660-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="77660-113">1\_2</span></span> | <span data-ttu-id="77660-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77660-114">1\_3</span></span> | <span data-ttu-id="77660-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="77660-115">1\_4</span></span> | <span data-ttu-id="77660-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77660-116">2\_0</span></span> | <span data-ttu-id="77660-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="77660-117">2\_x</span></span> | <span data-ttu-id="77660-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="77660-118">2\_sw</span></span> | <span data-ttu-id="77660-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77660-119">3\_0</span></span> | <span data-ttu-id="77660-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="77660-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="77660-121">texcrd</span><span class="sxs-lookup"><span data-stu-id="77660-121">texcrd</span></span>                |      |      |      | <span data-ttu-id="77660-122">x</span><span class="sxs-lookup"><span data-stu-id="77660-122">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="77660-123">Questa istruzione interpreta i dati delle coordinate come dati di colore (RGBA).</span><span class="sxs-lookup"><span data-stu-id="77660-123">This instruction interprets coordinate data as color data (RGBA).</span></span>

<span data-ttu-id="77660-124">Questa istruzione non consente di campionare alcuna trama.</span><span class="sxs-lookup"><span data-stu-id="77660-124">No texture is sampled by this instruction.</span></span> <span data-ttu-id="77660-125">Sono rilevanti solo le coordinate di trama impostate in questa fase della trama.</span><span class="sxs-lookup"><span data-stu-id="77660-125">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="77660-126">Quando si usa texcrd, tenere presente i dettagli seguenti sulla modalità di copia dei dati dal registro di origine al registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="77660-126">When using texcrd, keep in mind the following detail about how data is copied from the source register to the destination register.</span></span> <span data-ttu-id="77660-127">Il registro delle coordinate di trama di origine (t \# ) include i dati nell'intervallo \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , mentre il registro di destinazione (r \# ) può conservare i dati solo nell'intervallo (probabilmente inferiore) \[ -D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] .</span><span class="sxs-lookup"><span data-stu-id="77660-127">The source texture coordinate register (t\#) holds data in the range \[-D3DCAPS9.MaxTextureRepeat, D3DCAPS9.MaxTextureRepeat\], while the destination register (r\#) can hold data only in the (likely smaller) range \[-D3DCAPS9.PixelShader1xMaxValue, D3DCAPS9.PixelShader1xMaxValue\].</span></span> <span data-ttu-id="77660-128">Si noti che per pixel shader versione \_ 4 D3DCAPS9. PixelShader1xMaxValue deve essere un minimo di otto.</span><span class="sxs-lookup"><span data-stu-id="77660-128">Note that for pixel shader version 1\_4, D3DCAPS9.PixelShader1xMaxValue must be a minimum of eight.</span></span> <span data-ttu-id="77660-129">È probabile che l'istruzione texcrd, nel processo di blocco dei dati di origine non compreso nell'intervallo del registro di destinazione, si comporti in modo diverso su hardware diverso.</span><span class="sxs-lookup"><span data-stu-id="77660-129">The texcrd instruction, in the process of clamping source data that is out of range of the destination register, is likely to behave differently on different hardware.</span></span> <span data-ttu-id="77660-130">Il primo hardware pixel shader versione 1 \_ 4 sul mercato eseguirà un morsetto speciale per i valori non compresi nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="77660-130">The first pixel shader version 1\_4 hardware on the market will perform a special clamp for values outside of range.</span></span> <span data-ttu-id="77660-131">Questo morsetto è stato progettato per produrre un numero che può essere inserito nel registro di destinazione, ma anche per mantenere il comportamento di indirizzamento della trama per i dati fuori intervallo (vedere [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) se i dati devono essere usati successivamente per il campionamento di trama.</span><span class="sxs-lookup"><span data-stu-id="77660-131">This clamp is designed to produce a number that can fit into the destination register, but also to preserve texture addressing behavior for out-of-range data (see [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) if the data were to be subsequently used for texture sampling.</span></span> <span data-ttu-id="77660-132">Tuttavia, un nuovo hardware di produttori diversi potrebbe non presentare questo comportamento e potrebbe solo tagliare i dati per adattarsi all'intervallo di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="77660-132">However, new hardware from different manufacturers might not exhibit this behavior and might just chop data to fit the destination register range.</span></span> <span data-ttu-id="77660-133">Pertanto, il modo più sicuro di agire quando si usa pixel shader versione 1 \_ 4 texcrd è fornire i dati delle coordinate di trama solo nel pixel shader che è già compreso nell'intervallo \[ -8, 8, in \] modo da non basarsi sul modo in cui i morsetti hardware vengono usati.</span><span class="sxs-lookup"><span data-stu-id="77660-133">Therefore, the safest course of action when using pixel shader version 1\_4 texcrd is to supply texture coordinate data only into the pixel shader that is already within the range \[-8,8\] so that you do not rely on the way hardware clamps.</span></span>

<span data-ttu-id="77660-134">A differenza \_ di TEXCOORD, texcrd non blocca i valori compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="77660-134">Unlike texcoord\_, texcrd does not clamp values between 0 and 1.</span></span>

<span data-ttu-id="77660-135">Regole per l'uso di texcrd:</span><span class="sxs-lookup"><span data-stu-id="77660-135">Rules for using texcrd :</span></span>

1.  <span data-ttu-id="77660-136">Lo stesso modificatore. xyz o. XYW deve essere applicato a ogni lettura di un singolo registro t (n) in un'istruzione texcrd o texld.</span><span class="sxs-lookup"><span data-stu-id="77660-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within a texcrd or texld instruction.</span></span>
2.  <span data-ttu-id="77660-137">Il quarto risultato del canale di texcrd viene annullato o non definito in tutti i casi.</span><span class="sxs-lookup"><span data-stu-id="77660-137">The fourth channel result of texcrd is unset/undefined in all cases.</span></span>
3.  <span data-ttu-id="77660-138">Il terzo canale non è definito o non è definito per il \_ case XYW DW.</span><span class="sxs-lookup"><span data-stu-id="77660-138">The third channel is unset/undefined for the xyw\_dw case.</span></span>

## <a name="examples"></a><span data-ttu-id="77660-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="77660-139">Examples</span></span>

<span data-ttu-id="77660-140">Di seguito è riportato il set completo di sintassi consentita per texcrd, che tiene conto di tutte le combinazioni di modificatori di origine valide e di una maschera di scrittura di destinazione.</span><span class="sxs-lookup"><span data-stu-id="77660-140">The complete set of allowed syntax for texcrd, taking into account all valid source modifier/selector and destination write mask combinations, is shown below.</span></span> <span data-ttu-id="77660-141">Si noti che la notazione. RGBA e. xyzw può essere usata in modo interscambiabile.</span><span class="sxs-lookup"><span data-stu-id="77660-141">Note that the .rgba and .xyzw notation can be used interchangeably.</span></span>

<span data-ttu-id="77660-142">Copia i primi tre canali del registro iteratore delle coordinate di trama, t (n), in r (m).</span><span class="sxs-lookup"><span data-stu-id="77660-142">Copies first three channels of texture coordinate iterator register, t(n), into r(m).</span></span> <span data-ttu-id="77660-143">Il quarto canale di r (m) non è inizializzato.</span><span class="sxs-lookup"><span data-stu-id="77660-143">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



<span data-ttu-id="77660-144">Inserisce il primo, il secondo e il quarto componente di t (n) nei primi tre canali di r (m).</span><span class="sxs-lookup"><span data-stu-id="77660-144">Puts first, second, and fourth components of t(n) into first three channels of r(m).</span></span> <span data-ttu-id="77660-145">Il quarto canale di r (m) non è inizializzato.</span><span class="sxs-lookup"><span data-stu-id="77660-145">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyw
```



<span data-ttu-id="77660-146">Di seguito è riportato un esempio di suddivisione proiettiva usando il \_ modificatore DW.</span><span class="sxs-lookup"><span data-stu-id="77660-146">Here is a projective divide example using the \_dw modifier.</span></span>

<span data-ttu-id="77660-147">Questo esempio copia x/w e y/w da t (n) nei primi due canali di r (m).</span><span class="sxs-lookup"><span data-stu-id="77660-147">This example copies x/w and y/w from t(n) into the first two channels of r(m).</span></span> <span data-ttu-id="77660-148">Il terzo e il quarto canale di r (m) non sono inizializzati.</span><span class="sxs-lookup"><span data-stu-id="77660-148">The third and fourth channels of r(m) are uninitialized.</span></span> <span data-ttu-id="77660-149">Tutti i dati scritti in precedenza nel terzo canale di r (m) andranno perduti.</span><span class="sxs-lookup"><span data-stu-id="77660-149">Any data previously written to the third channel of r(m) will be lost.</span></span> <span data-ttu-id="77660-150">I dati nel quarto canale di r (m) andranno perduti a causa del marcatore di fase.</span><span class="sxs-lookup"><span data-stu-id="77660-150">Data in the fourth channel of r(m) is lost due to the phase marker.</span></span> <span data-ttu-id="77660-151">Per la versione 1 \_ 4, il \_ flag D3DTTFF proiettato viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="77660-151">For version 1\_4, the D3DTTFF\_PROJECTED flag is ignored.</span></span>


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a><span data-ttu-id="77660-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77660-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77660-153">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="77660-153">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 