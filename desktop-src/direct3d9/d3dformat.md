---
description: Definisce i vari tipi di formati di superficie.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFORMAT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 228884435322992b8c87d20a9f351161f945c43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762107"
---
# <a name="d3dformat"></a><span data-ttu-id="02b4e-103">D3DFORMAT</span><span class="sxs-lookup"><span data-stu-id="02b4e-103">D3DFORMAT</span></span>

<span data-ttu-id="02b4e-104">Definisce i vari tipi di formati di superficie.</span><span class="sxs-lookup"><span data-stu-id="02b4e-104">Defines the various types of surface formats.</span></span>

``` syntax
typedef enum _D3DFORMAT {
    D3DFMT_UNKNOWN              =  0,

    D3DFMT_R8G8B8               = 20,
    D3DFMT_A8R8G8B8             = 21,
    D3DFMT_X8R8G8B8             = 22,
    D3DFMT_R5G6B5               = 23,
    D3DFMT_X1R5G5B5             = 24,
    D3DFMT_A1R5G5B5             = 25,
    D3DFMT_A4R4G4B4             = 26,
    D3DFMT_R3G3B2               = 27,
    D3DFMT_A8                   = 28,
    D3DFMT_A8R3G3B2             = 29,
    D3DFMT_X4R4G4B4             = 30,
    D3DFMT_A2B10G10R10          = 31,
    D3DFMT_A8B8G8R8             = 32,
    D3DFMT_X8B8G8R8             = 33,
    D3DFMT_G16R16               = 34,
    D3DFMT_A2R10G10B10          = 35,
    D3DFMT_A16B16G16R16         = 36,

    D3DFMT_A8P8                 = 40,
    D3DFMT_P8                   = 41,

    D3DFMT_L8                   = 50,
    D3DFMT_A8L8                 = 51,
    D3DFMT_A4L4                 = 52,

    D3DFMT_V8U8                 = 60,
    D3DFMT_L6V5U5               = 61,
    D3DFMT_X8L8V8U8             = 62,
    D3DFMT_Q8W8V8U8             = 63,
    D3DFMT_V16U16               = 64,
    D3DFMT_A2W10V10U10          = 67,

    D3DFMT_UYVY                 = MAKEFOURCC('U', 'Y', 'V', 'Y'),
    D3DFMT_R8G8_B8G8            = MAKEFOURCC('R', 'G', 'B', 'G'),
    D3DFMT_YUY2                 = MAKEFOURCC('Y', 'U', 'Y', '2'),
    D3DFMT_G8R8_G8B8            = MAKEFOURCC('G', 'R', 'G', 'B'),
    D3DFMT_DXT1                 = MAKEFOURCC('D', 'X', 'T', '1'),
    D3DFMT_DXT2                 = MAKEFOURCC('D', 'X', 'T', '2'),
    D3DFMT_DXT3                 = MAKEFOURCC('D', 'X', 'T', '3'),
    D3DFMT_DXT4                 = MAKEFOURCC('D', 'X', 'T', '4'),
    D3DFMT_DXT5                 = MAKEFOURCC('D', 'X', 'T', '5'),

    D3DFMT_D16_LOCKABLE         = 70,
    D3DFMT_D32                  = 71,
    D3DFMT_D15S1                = 73,
    D3DFMT_D24S8                = 75,
    D3DFMT_D24X8                = 77,
    D3DFMT_D24X4S4              = 79,
    D3DFMT_D16                  = 80,

    D3DFMT_D32F_LOCKABLE        = 82,
    D3DFMT_D24FS8               = 83,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_D32_LOCKABLE         = 84,
    D3DFMT_S8_LOCKABLE          = 85,
#endif // !D3D_DISABLE_9EX

    D3DFMT_L16                  = 81,

    D3DFMT_VERTEXDATA           =100,
    D3DFMT_INDEX16              =101,
    D3DFMT_INDEX32              =102,

    D3DFMT_Q16W16V16U16         =110,

    D3DFMT_MULTI2_ARGB8         = MAKEFOURCC('M','E','T','1'),

    D3DFMT_R16F                 = 111,
    D3DFMT_G16R16F              = 112,
    D3DFMT_A16B16G16R16F        = 113,

    D3DFMT_R32F                 = 114,
    D3DFMT_G32R32F              = 115,
    D3DFMT_A32B32G32R32F        = 116,

    D3DFMT_CxV8U8               = 117,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_A1                   = 118,
    D3DFMT_A2B10G10R10_XR_BIAS  = 119,
    D3DFMT_BINARYBUFFER         = 199,
#endif // !D3D_DISABLE_9EX

    D3DFMT_FORCE_DWORD          =0x7fffffff
} D3DFORMAT;
```

## <a name="remarks"></a><span data-ttu-id="02b4e-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="02b4e-105">Remarks</span></span>

<span data-ttu-id="02b4e-106">Esistono diversi tipi di formati:</span><span class="sxs-lookup"><span data-stu-id="02b4e-106">There are several types of formats:</span></span>

-   [<span data-ttu-id="02b4e-107">Formati di visualizzazione o backBuffer</span><span class="sxs-lookup"><span data-stu-id="02b4e-107">BackBuffer or Display Formats</span></span>](#backbuffer-or-display-formats)
-   [<span data-ttu-id="02b4e-108">Formati di buffer</span><span class="sxs-lookup"><span data-stu-id="02b4e-108">Buffer Formats</span></span>](#buffer-formats)
-   [<span data-ttu-id="02b4e-109">Formati di trama compressi DXTn</span><span class="sxs-lookup"><span data-stu-id="02b4e-109">DXTn Compressed Texture Formats</span></span>](#dxtn-compressed-texture-formats)
-   [<span data-ttu-id="02b4e-110">Formati a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="02b4e-110">Floating-Point Formats</span></span>](#floating-point-formats)
-   [<span data-ttu-id="02b4e-111">Formati FOURCC</span><span class="sxs-lookup"><span data-stu-id="02b4e-111">FOURCC Formats</span></span>](#fourcc-formats)
-   [<span data-ttu-id="02b4e-112">Formati IEEE</span><span class="sxs-lookup"><span data-stu-id="02b4e-112">IEEE Formats</span></span>](#ieee-formats)
-   [<span data-ttu-id="02b4e-113">Formati misti</span><span class="sxs-lookup"><span data-stu-id="02b4e-113">Mixed Formats</span></span>](#mixed-formats)
-   [<span data-ttu-id="02b4e-114">Formati firmati</span><span class="sxs-lookup"><span data-stu-id="02b4e-114">Signed Formats</span></span>](#signed-formats)
-   [<span data-ttu-id="02b4e-115">Formati non firmati</span><span class="sxs-lookup"><span data-stu-id="02b4e-115">Unsigned Formats</span></span>](#unsigned-formats)
-   [<span data-ttu-id="02b4e-116">Altri</span><span class="sxs-lookup"><span data-stu-id="02b4e-116">Other</span></span>](#other)

<span data-ttu-id="02b4e-117">Tutti i formati sono elencati da sinistra a destra, da un bit più significativo a un bit meno significativo.</span><span class="sxs-lookup"><span data-stu-id="02b4e-117">All formats are listed from left to right, most-significant bit to least-significant bit.</span></span> <span data-ttu-id="02b4e-118">Ad esempio, **D3DFORMAT \_ ARGB** viene ordinato dal canale di bit più significativo a (alfa) al canale di bit meno significativo B (blu).</span><span class="sxs-lookup"><span data-stu-id="02b4e-118">For example, **D3DFORMAT\_ARGB** is ordered from the most-significant bit channel A (alpha), to the least-significant bit channel B (blue).</span></span> <span data-ttu-id="02b4e-119">Quando si attraversano i dati della superficie, i dati vengono archiviati in memoria dal bit meno significativo al bit più significativo, il che significa che l'ordine dei canali in memoria è da un bit meno significativo (blu) a un bit più significativo (alfa).</span><span class="sxs-lookup"><span data-stu-id="02b4e-119">When traversing surface data, the data is stored in memory from least-significant bit to most-significant bit, which means that the channel order in memory is from least-significant bit (blue) to most-significant bit (alpha).</span></span>

<span data-ttu-id="02b4e-120">Il valore predefinito per i formati che contengono canali non definiti (G16R16, A8 e così via) è 1.</span><span class="sxs-lookup"><span data-stu-id="02b4e-120">The default value for formats that contain undefined channels (G16R16, A8, and so on) is 1.</span></span> <span data-ttu-id="02b4e-121">L'unica eccezione è il formato A8, che viene inizializzato a 000 per i tre canali dei colori.</span><span class="sxs-lookup"><span data-stu-id="02b4e-121">The only exception is the A8 format, which is initialized to 000 for the three color channels.</span></span>

<span data-ttu-id="02b4e-122">L'ordine dei bit è primo dal byte più significativo, quindi D3DFMT \_ A8L8 indica che il byte elevato del formato a 2 byte è alfa.</span><span class="sxs-lookup"><span data-stu-id="02b4e-122">The order of the bits is from the most significant byte first, so D3DFMT\_A8L8 indicates that the high byte of this 2-byte format is alpha.</span></span> <span data-ttu-id="02b4e-123">**D3DFMT \_ D16** indica un valore integer a 16 bit e una superficie bloccabile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="02b4e-123">**D3DFMT\_D16** indicates a 16-bit integer value and an application-lockable surface.</span></span>

<span data-ttu-id="02b4e-124">Sono stati scelti formati pixel per abilitare l'espressione dei formati di estensione definiti dal fornitore di hardware, oltre a includere il metodo FOURCC ben definito.</span><span class="sxs-lookup"><span data-stu-id="02b4e-124">Pixel formats have been chosen to enable the expression of hardware-vendor-defined extension formats, as well as to include the well-established FOURCC method.</span></span> <span data-ttu-id="02b4e-125">Il set di formati riconosciuto dal runtime Direct3D è definito da D3DFORMAT.</span><span class="sxs-lookup"><span data-stu-id="02b4e-125">The set of formats understood by the Direct3D runtime is defined by D3DFORMAT.</span></span>

<span data-ttu-id="02b4e-126">Si noti che i formati sono forniti da fornitori di hardware indipendenti (IHV) e molti codici FOURCC non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="02b4e-126">Note that formats are supplied by independent hardware vendors (IHVs) and many FOURCC codes are not listed.</span></span> <span data-ttu-id="02b4e-127">I formati in questa enumerazione sono univoci in quanto sono approvati dal runtime, vale a dire che l'rasterizzazione dei riferimenti funzionerà su tutti questi tipi.</span><span class="sxs-lookup"><span data-stu-id="02b4e-127">The formats in this enumeration are unique in that they are sanctioned by the runtime, meaning that the reference rasterizer will operate on all these types.</span></span> <span data-ttu-id="02b4e-128">I formati forniti da IHV saranno supportati dai singoli IHV in base a una scheda.</span><span class="sxs-lookup"><span data-stu-id="02b4e-128">IHV-supplied formats will be supported by the individual IHVs on a card-by-card basis.</span></span>

### <a name="backbuffer-or-display-formats"></a><span data-ttu-id="02b4e-129">Formati di visualizzazione o backBuffer</span><span class="sxs-lookup"><span data-stu-id="02b4e-129">BackBuffer or Display Formats</span></span>

<span data-ttu-id="02b4e-130">Questi formati sono gli unici formati validi per un buffer nascosto o una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="02b4e-130">These formats are the only valid formats for a back buffer or a display.</span></span>



| <span data-ttu-id="02b4e-131">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-131">Format</span></span>      | <span data-ttu-id="02b4e-132">Buffer nascosto</span><span class="sxs-lookup"><span data-stu-id="02b4e-132">Back buffer</span></span> | <span data-ttu-id="02b4e-133">Visualizza</span><span class="sxs-lookup"><span data-stu-id="02b4e-133">Display</span></span>                   |
|-------------|-------------|---------------------------|
| <span data-ttu-id="02b4e-134">A2R10G10B10</span><span class="sxs-lookup"><span data-stu-id="02b4e-134">A2R10G10B10</span></span> | <span data-ttu-id="02b4e-135">x</span><span class="sxs-lookup"><span data-stu-id="02b4e-135">x</span></span>           | <span data-ttu-id="02b4e-136">x (solo modalità schermo intero)</span><span class="sxs-lookup"><span data-stu-id="02b4e-136">x (full-screen mode only)</span></span> |
| <span data-ttu-id="02b4e-137">A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="02b4e-137">A8R8G8B8</span></span>    | <span data-ttu-id="02b4e-138">x</span><span class="sxs-lookup"><span data-stu-id="02b4e-138">x</span></span>           |                           |
| <span data-ttu-id="02b4e-139">X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="02b4e-139">X8R8G8B8</span></span>    | <span data-ttu-id="02b4e-140">x</span><span class="sxs-lookup"><span data-stu-id="02b4e-140">x</span></span>           | <span data-ttu-id="02b4e-141">x</span><span class="sxs-lookup"><span data-stu-id="02b4e-141">x</span></span>                         |
| <span data-ttu-id="02b4e-142">A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="02b4e-142">A1R5G5B5</span></span>    | <span data-ttu-id="02b4e-143">x</span><span class="sxs-lookup"><span data-stu-id="02b4e-143">x</span></span>           |                           |
| <span data-ttu-id="02b4e-144">X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="02b4e-144">X1R5G5B5</span></span>    | <span data-ttu-id="02b4e-145">x</span><span class="sxs-lookup"><span data-stu-id="02b4e-145">x</span></span>           | <span data-ttu-id="02b4e-146">x</span><span class="sxs-lookup"><span data-stu-id="02b4e-146">x</span></span>                         |
| <span data-ttu-id="02b4e-147">R5G6B5</span><span class="sxs-lookup"><span data-stu-id="02b4e-147">R5G6B5</span></span>      | <span data-ttu-id="02b4e-148">x</span><span class="sxs-lookup"><span data-stu-id="02b4e-148">x</span></span>           | <span data-ttu-id="02b4e-149">x</span><span class="sxs-lookup"><span data-stu-id="02b4e-149">x</span></span>                         |



 

### <a name="buffer-formats"></a><span data-ttu-id="02b4e-150">Formati di buffer</span><span class="sxs-lookup"><span data-stu-id="02b4e-150">Buffer Formats</span></span>

<span data-ttu-id="02b4e-151">I buffer di profondità, stencil, vertex e index hanno formati univoci.</span><span class="sxs-lookup"><span data-stu-id="02b4e-151">Depth, stencil, vertex, and index buffers each have unique formats.</span></span>



| <span data-ttu-id="02b4e-152">Flag del buffer</span><span class="sxs-lookup"><span data-stu-id="02b4e-152">Buffer flags</span></span>               | <span data-ttu-id="02b4e-153">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-153">Value</span></span> | <span data-ttu-id="02b4e-154">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-154">Format</span></span>                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b4e-155">**D3DFMT \_ D16 \_ lockable**</span><span class="sxs-lookup"><span data-stu-id="02b4e-155">**D3DFMT\_D16\_LOCKABLE**</span></span>  | <span data-ttu-id="02b4e-156">70</span><span class="sxs-lookup"><span data-stu-id="02b4e-156">70</span></span>    | <span data-ttu-id="02b4e-157">profondità di bit del buffer z a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-157">16-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="02b4e-158">**\_D32 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-158">**D3DFMT\_D32**</span></span>            | <span data-ttu-id="02b4e-159">71</span><span class="sxs-lookup"><span data-stu-id="02b4e-159">71</span></span>    | <span data-ttu-id="02b4e-160">profondità di bit del buffer z a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-160">32-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="02b4e-161">**\_D15S1 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-161">**D3DFMT\_D15S1**</span></span>          | <span data-ttu-id="02b4e-162">73</span><span class="sxs-lookup"><span data-stu-id="02b4e-162">73</span></span>    | <span data-ttu-id="02b4e-163">profondità di bit del buffer z a 16 bit, dove 15 bit sono riservati per il canale di profondità e 1 bit è riservato per il canale dello stencil.</span><span class="sxs-lookup"><span data-stu-id="02b4e-163">16-bit z-buffer bit depth where 15 bits are reserved for the depth channel and 1 bit is reserved for the stencil channel.</span></span>                     |
| <span data-ttu-id="02b4e-164">**\_D24S8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-164">**D3DFMT\_D24S8**</span></span>          | <span data-ttu-id="02b4e-165">75</span><span class="sxs-lookup"><span data-stu-id="02b4e-165">75</span></span>    | <span data-ttu-id="02b4e-166">profondità di bit del buffer z a 32 bit con 24 bit per il canale di profondità e 8 bit per il canale dello stencil.</span><span class="sxs-lookup"><span data-stu-id="02b4e-166">32-bit z-buffer bit depth using 24 bits for the depth channel and 8 bits for the stencil channel.</span></span>                                             |
| <span data-ttu-id="02b4e-167">**\_D24X8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-167">**D3DFMT\_D24X8**</span></span>          | <span data-ttu-id="02b4e-168">77</span><span class="sxs-lookup"><span data-stu-id="02b4e-168">77</span></span>    | <span data-ttu-id="02b4e-169">profondità di bit del buffer z a 32 bit con 24 bit per il canale di profondità.</span><span class="sxs-lookup"><span data-stu-id="02b4e-169">32-bit z-buffer bit depth using 24 bits for the depth channel.</span></span>                                                                                |
| <span data-ttu-id="02b4e-170">**\_D24X4S4 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-170">**D3DFMT\_D24X4S4**</span></span>        | <span data-ttu-id="02b4e-171">79</span><span class="sxs-lookup"><span data-stu-id="02b4e-171">79</span></span>    | <span data-ttu-id="02b4e-172">profondità di bit del buffer z a 32 bit con 24 bit per il canale di profondità e 4 bit per il canale dello stencil.</span><span class="sxs-lookup"><span data-stu-id="02b4e-172">32-bit z-buffer bit depth using 24 bits for the depth channel and 4 bits for the stencil channel.</span></span>                                             |
| <span data-ttu-id="02b4e-173">**D3DFMT \_ D32F \_ lockable**</span><span class="sxs-lookup"><span data-stu-id="02b4e-173">**D3DFMT\_D32F\_LOCKABLE**</span></span> | <span data-ttu-id="02b4e-174">82</span><span class="sxs-lookup"><span data-stu-id="02b4e-174">82</span></span>    | <span data-ttu-id="02b4e-175">Formato bloccabile in cui il valore di profondità viene rappresentato come numero a virgola mobile IEEE standard.</span><span class="sxs-lookup"><span data-stu-id="02b4e-175">A lockable format where the depth value is represented as a standard IEEE floating-point number.</span></span>                                              |
| <span data-ttu-id="02b4e-176">**\_D24FS8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-176">**D3DFMT\_D24FS8**</span></span>         | <span data-ttu-id="02b4e-177">83</span><span class="sxs-lookup"><span data-stu-id="02b4e-177">83</span></span>    | <span data-ttu-id="02b4e-178">Formato non bloccabile che contiene 24 bit di profondità (in un formato a virgola mobile a 24 bit-20E4) e 8 bit di stencil.</span><span class="sxs-lookup"><span data-stu-id="02b4e-178">A non-lockable format that contains 24 bits of depth (in a 24-bit floating point format - 20e4) and 8 bits of stencil.</span></span>                        |
| <span data-ttu-id="02b4e-179">**D3DFMT \_ D32 \_ lockable**</span><span class="sxs-lookup"><span data-stu-id="02b4e-179">**D3DFMT\_D32\_LOCKABLE**</span></span>  | <span data-ttu-id="02b4e-180">84</span><span class="sxs-lookup"><span data-stu-id="02b4e-180">84</span></span>    | <span data-ttu-id="02b4e-181">Buffer di profondità a 32 bit bloccabile.</span><span class="sxs-lookup"><span data-stu-id="02b4e-181">A lockable 32-bit depth buffer.</span></span> <span data-ttu-id="02b4e-182">**Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="02b4e-182">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>  |
| <span data-ttu-id="02b4e-183">**D3DFMT \_ S8 \_ bloccabile**</span><span class="sxs-lookup"><span data-stu-id="02b4e-183">**D3DFMT\_S8\_LOCKABLE**</span></span>   | <span data-ttu-id="02b4e-184">85</span><span class="sxs-lookup"><span data-stu-id="02b4e-184">85</span></span>    | <span data-ttu-id="02b4e-185">Buffer di stencil a 8 bit bloccabile.</span><span class="sxs-lookup"><span data-stu-id="02b4e-185">A lockable 8-bit stencil buffer.</span></span> <span data-ttu-id="02b4e-186">**Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="02b4e-186">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/> |
| <span data-ttu-id="02b4e-187">**\_D16 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-187">**D3DFMT\_D16**</span></span>            | <span data-ttu-id="02b4e-188">80</span><span class="sxs-lookup"><span data-stu-id="02b4e-188">80</span></span>    | <span data-ttu-id="02b4e-189">profondità di bit del buffer z a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-189">16-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="02b4e-190">**\_VERTEXDATA D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-190">**D3DFMT\_VERTEXDATA**</span></span>     | <span data-ttu-id="02b4e-191">100</span><span class="sxs-lookup"><span data-stu-id="02b4e-191">100</span></span>   | <span data-ttu-id="02b4e-192">Descrive una superficie del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="02b4e-192">Describes a vertex buffer surface.</span></span>                                                                                                            |
| <span data-ttu-id="02b4e-193">**\_INDEX16 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-193">**D3DFMT\_INDEX16**</span></span>        | <span data-ttu-id="02b4e-194">101</span><span class="sxs-lookup"><span data-stu-id="02b4e-194">101</span></span>   | <span data-ttu-id="02b4e-195">profondità dei bit del buffer di indice a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-195">16-bit index buffer bit depth.</span></span>                                                                                                                |
| <span data-ttu-id="02b4e-196">**\_INDEX32 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-196">**D3DFMT\_INDEX32**</span></span>        | <span data-ttu-id="02b4e-197">102</span><span class="sxs-lookup"><span data-stu-id="02b4e-197">102</span></span>   | <span data-ttu-id="02b4e-198">profondità di bit del buffer dell'indice a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-198">32-bit index buffer bit depth.</span></span>                                                                                                                |



 

<span data-ttu-id="02b4e-199">Tutti i formati di stencil Depth, ad eccezione \_ di D3DFMT D16 \_ lockable, non indicano alcun ordine di bit specifico per pixel e il driver è autorizzato a utilizzare un numero di canali superiore al numero indicato di bit per profondità (ma non il canale dello stencil).</span><span class="sxs-lookup"><span data-stu-id="02b4e-199">All depth-stencil formats except D3DFMT\_D16\_LOCKABLE indicate no particular bit ordering per pixel, and the driver is allowed to consume more than the indicated number of bits-per-depth channel (but not stencil channel).</span></span>

### <a name="dxtn-compressed-texture-formats"></a><span data-ttu-id="02b4e-200">Formati di trama compressi DXTn</span><span class="sxs-lookup"><span data-stu-id="02b4e-200">DXTn Compressed Texture Formats</span></span>

<span data-ttu-id="02b4e-201">Questi flag vengono usati per le trame compresse:</span><span class="sxs-lookup"><span data-stu-id="02b4e-201">These flags are used for compressed textures:</span></span>



| <span data-ttu-id="02b4e-202">Flag di trama compressi DXTn</span><span class="sxs-lookup"><span data-stu-id="02b4e-202">DXTn Compressed Texture flags</span></span> | <span data-ttu-id="02b4e-203">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-203">Value</span></span>                          | <span data-ttu-id="02b4e-204">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-204">Format</span></span>                          |
|-------------------------------|--------------------------------|---------------------------------|
| <span data-ttu-id="02b4e-205">**\_DXT1 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-205">**D3DFMT\_DXT1**</span></span>              | <span data-ttu-id="02b4e-206">MAKEFOURCC (' D',' X ',' T',' 1')</span><span class="sxs-lookup"><span data-stu-id="02b4e-206">MAKEFOURCC('D', 'X', 'T', '1')</span></span> | <span data-ttu-id="02b4e-207">Formato trama compressione DXT1</span><span class="sxs-lookup"><span data-stu-id="02b4e-207">DXT1 compression texture format</span></span> |
| <span data-ttu-id="02b4e-208">**\_DXT2 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-208">**D3DFMT\_DXT2**</span></span>              | <span data-ttu-id="02b4e-209">MAKEFOURCC (' D',' X ',' T',' 2')</span><span class="sxs-lookup"><span data-stu-id="02b4e-209">MAKEFOURCC('D', 'X', 'T', '2')</span></span> | <span data-ttu-id="02b4e-210">Formato trama compressione DXT2</span><span class="sxs-lookup"><span data-stu-id="02b4e-210">DXT2 compression texture format</span></span> |
| <span data-ttu-id="02b4e-211">**\_DXT3 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-211">**D3DFMT\_DXT3**</span></span>              | <span data-ttu-id="02b4e-212">MAKEFOURCC (' D',' X ',' T',' 3')</span><span class="sxs-lookup"><span data-stu-id="02b4e-212">MAKEFOURCC('D', 'X', 'T', '3')</span></span> | <span data-ttu-id="02b4e-213">Formato trama compressione DXT3</span><span class="sxs-lookup"><span data-stu-id="02b4e-213">DXT3 compression texture format</span></span> |
| <span data-ttu-id="02b4e-214">**\_DXT4 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-214">**D3DFMT\_DXT4**</span></span>              | <span data-ttu-id="02b4e-215">MAKEFOURCC (' D',' X ',' T',' 4')</span><span class="sxs-lookup"><span data-stu-id="02b4e-215">MAKEFOURCC('D', 'X', 'T', '4')</span></span> | <span data-ttu-id="02b4e-216">Formato trama compressione DXT4</span><span class="sxs-lookup"><span data-stu-id="02b4e-216">DXT4 compression texture format</span></span> |
| <span data-ttu-id="02b4e-217">**\_DXT5 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-217">**D3DFMT\_DXT5**</span></span>              | <span data-ttu-id="02b4e-218">MAKEFOURCC (' D',' X ',' T',' 5')</span><span class="sxs-lookup"><span data-stu-id="02b4e-218">MAKEFOURCC('D', 'X', 'T', '5')</span></span> | <span data-ttu-id="02b4e-219">Formato trama compressione DXT5</span><span class="sxs-lookup"><span data-stu-id="02b4e-219">DXT5 compression texture format</span></span> |



 

<span data-ttu-id="02b4e-220">Il runtime non consentirà a un'applicazione di creare una superficie utilizzando un formato DXTn, a meno che le dimensioni della superficie non siano multipli di 4.</span><span class="sxs-lookup"><span data-stu-id="02b4e-220">The runtime will not allow an application to create a surface using a DXTn format unless the surface dimensions are multiples of 4.</span></span> <span data-ttu-id="02b4e-221">Questo vale per le superfici semplici Offscreen, le destinazioni di rendering, le trame 2D, le trame del cubo e le trame del volume.</span><span class="sxs-lookup"><span data-stu-id="02b4e-221">This applies to offscreen-plain surfaces, render targets, 2D textures, cube textures, and volume textures.</span></span>

### <a name="floating-point-formats"></a><span data-ttu-id="02b4e-222">Formati di Floating-Point</span><span class="sxs-lookup"><span data-stu-id="02b4e-222">Floating-Point Formats</span></span>

<span data-ttu-id="02b4e-223">Questi flag vengono utilizzati per i formati di superficie a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="02b4e-223">These flags are used for floating-point surface formats.</span></span> <span data-ttu-id="02b4e-224">Questi formati a 16 bit per canale sono noti anche come formati s10e5.</span><span class="sxs-lookup"><span data-stu-id="02b4e-224">These 16-bits-per-channel formats are also known as s10e5 formats.</span></span>



| <span data-ttu-id="02b4e-225">Flag a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="02b4e-225">Floating-point flags</span></span>      | <span data-ttu-id="02b4e-226">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-226">Value</span></span> | <span data-ttu-id="02b4e-227">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-227">Format</span></span>                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b4e-228">**\_R16F D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-228">**D3DFMT\_R16F**</span></span>          | <span data-ttu-id="02b4e-229">111</span><span class="sxs-lookup"><span data-stu-id="02b4e-229">111</span></span>   | <span data-ttu-id="02b4e-230">formato float a 16 bit con 16 bit per il canale rosso.</span><span class="sxs-lookup"><span data-stu-id="02b4e-230">16-bit float format using 16 bits for the red channel.</span></span>                                   |
| <span data-ttu-id="02b4e-231">**\_G16R16F D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-231">**D3DFMT\_G16R16F**</span></span>       | <span data-ttu-id="02b4e-232">112</span><span class="sxs-lookup"><span data-stu-id="02b4e-232">112</span></span>   | <span data-ttu-id="02b4e-233">formato float a 32 bit con 16 bit per il canale rosso e 16 bit per il canale verde.</span><span class="sxs-lookup"><span data-stu-id="02b4e-233">32-bit float format using 16 bits for the red channel and 16 bits for the green channel.</span></span> |
| <span data-ttu-id="02b4e-234">**\_A16B16G16R16F D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-234">**D3DFMT\_A16B16G16R16F**</span></span> | <span data-ttu-id="02b4e-235">113</span><span class="sxs-lookup"><span data-stu-id="02b4e-235">113</span></span>   | <span data-ttu-id="02b4e-236">formato float a 64 bit con 16 bit per ogni canale (alfa, blu, verde, rosso).</span><span class="sxs-lookup"><span data-stu-id="02b4e-236">64-bit float format using 16 bits for the each channel (alpha, blue, green, red).</span></span>        |



 

### <a name="fourcc-formats"></a><span data-ttu-id="02b4e-237">Formati FOURCC</span><span class="sxs-lookup"><span data-stu-id="02b4e-237">FOURCC Formats</span></span>

<span data-ttu-id="02b4e-238">I dati in un formato FOURCC sono dati compressi.</span><span class="sxs-lookup"><span data-stu-id="02b4e-238">Data in a FOURCC format is compressed data.</span></span>

### <a name="makefourcc"></a><span data-ttu-id="02b4e-239">MAKEFOURCC</span><span class="sxs-lookup"><span data-stu-id="02b4e-239">MAKEFOURCC</span></span>

<span data-ttu-id="02b4e-240">Di seguito è riportata una macro per la generazione di codici di quattro caratteri:</span><span class="sxs-lookup"><span data-stu-id="02b4e-240">A macro for generating four-character codes follows:</span></span>

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

<span data-ttu-id="02b4e-241">Di seguito sono riportati i formati FOURCC definiti:</span><span class="sxs-lookup"><span data-stu-id="02b4e-241">Here are the defined FOURCC formats:</span></span>



| <span data-ttu-id="02b4e-242">Flag FOURCC</span><span class="sxs-lookup"><span data-stu-id="02b4e-242">FOURCC flags</span></span>              | <span data-ttu-id="02b4e-243">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-243">Value</span></span>                          | <span data-ttu-id="02b4e-244">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-244">Format</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b4e-245">**D3DFMT \_ MULTi2 \_ ARGB8**</span><span class="sxs-lookup"><span data-stu-id="02b4e-245">**D3DFMT\_MULTI2\_ARGB8**</span></span> | <span data-ttu-id="02b4e-246">MAKEFOURCC (' M',' È,' T',' 1')</span><span class="sxs-lookup"><span data-stu-id="02b4e-246">MAKEFOURCC('M','E','T','1')</span></span>    | <span data-ttu-id="02b4e-247">Trama a più elementi (non compresso)</span><span class="sxs-lookup"><span data-stu-id="02b4e-247">MultiElement texture (not compressed)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="02b4e-248">**D3DFMT \_ G8R8 \_ G8B8**</span><span class="sxs-lookup"><span data-stu-id="02b4e-248">**D3DFMT\_G8R8\_G8B8**</span></span>    | <span data-ttu-id="02b4e-249">MAKEFOURCC (' G ',' R ',' G ',' B ')</span><span class="sxs-lookup"><span data-stu-id="02b4e-249">MAKEFOURCC('G', 'R', 'G', 'B')</span></span> | <span data-ttu-id="02b4e-250">Formato RGB compresso a 16 bit analogo a YUY2 (Y0U0, Y1V0, Y2U2 e così via).</span><span class="sxs-lookup"><span data-stu-id="02b4e-250">A 16-bit packed RGB format analogous to YUY2 (Y0U0, Y1V0, Y2U2, and so on).</span></span> <span data-ttu-id="02b4e-251">Richiede una coppia di pixel per rappresentare correttamente il valore del colore.</span><span class="sxs-lookup"><span data-stu-id="02b4e-251">It requires a pixel pair in order to properly represent the color value.</span></span> <span data-ttu-id="02b4e-252">Il primo pixel della coppia contiene 8 bit di verde (negli 8 bit alti) e 8 bit di rosso (negli 8 bit bassi).</span><span class="sxs-lookup"><span data-stu-id="02b4e-252">The first pixel in the pair contains 8 bits of green (in the high 8 bits) and 8 bits of red (in the low 8 bits).</span></span> <span data-ttu-id="02b4e-253">Il secondo pixel contiene 8 bit di verde (negli 8 bit alti) e 8 bit di blu (negli 8 bit bassi).</span><span class="sxs-lookup"><span data-stu-id="02b4e-253">The second pixel contains 8 bits of green (in the high 8 bits) and 8 bits of blue (in the low 8 bits).</span></span> <span data-ttu-id="02b4e-254">Insieme, i due pixel condividono i componenti rosso e blu, mentre ognuno ha un componente verde univoco (G0R0, G1B0, G2R2 e così via).</span><span class="sxs-lookup"><span data-stu-id="02b4e-254">Together, the two pixels share the red and blue components, while each has a unique green component (G0R0, G1B0, G2R2, and so on).</span></span> <span data-ttu-id="02b4e-255">Il campionatore di trame non normalizza i colori durante la ricerca in un pixel shader; rimangono nell'intervallo da 0,0 f a 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="02b4e-255">The texture sampler does not normalize the colors when looking up into a pixel shader; they remain in the range of 0.0f to 255.0f.</span></span> <span data-ttu-id="02b4e-256">Questo vale per tutti i modelli di pixel shader programmabili.</span><span class="sxs-lookup"><span data-stu-id="02b4e-256">This is true for all programmable pixel shader models.</span></span> <span data-ttu-id="02b4e-257">Per la funzione Fixed pixel shader, l'hardware deve normalizzarsi nell'intervallo da 0. f a 1. f e essenzialmente considerarlo come trama YUY2.</span><span class="sxs-lookup"><span data-stu-id="02b4e-257">For the fixed function pixel shader, the hardware should normalize to the 0.f to 1.f range and essentially treat it as the YUY2 texture.</span></span> <span data-ttu-id="02b4e-258">Per l'hardware che espone questo formato il membro PixelShader1xMaxValue di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) deve essere impostato su un valore in grado di gestire tale intervallo.</span><span class="sxs-lookup"><span data-stu-id="02b4e-258">Hardware that exposes this format must have the PixelShader1xMaxValue member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) set to a value capable of handling that range.</span></span> |
| <span data-ttu-id="02b4e-259">**D3DFMT \_ R8G8 \_ B8G8**</span><span class="sxs-lookup"><span data-stu-id="02b4e-259">**D3DFMT\_R8G8\_B8G8**</span></span>    | <span data-ttu-id="02b4e-260">MAKEFOURCC (' R ',' G ',' B ',' G ')</span><span class="sxs-lookup"><span data-stu-id="02b4e-260">MAKEFOURCC('R', 'G', 'B', 'G')</span></span> | <span data-ttu-id="02b4e-261">Formato RGB compresso a 16 bit analogo a UYVY (U0Y0, V0Y1, U2Y2 e così via).</span><span class="sxs-lookup"><span data-stu-id="02b4e-261">A 16-bit packed RGB format analogous to UYVY (U0Y0, V0Y1, U2Y2, and so on).</span></span> <span data-ttu-id="02b4e-262">Richiede una coppia di pixel per rappresentare correttamente il valore del colore.</span><span class="sxs-lookup"><span data-stu-id="02b4e-262">It requires a pixel pair in order to properly represent the color value.</span></span> <span data-ttu-id="02b4e-263">Il primo pixel della coppia contiene 8 bit di verde (negli 8 bit bassi) e 8 bit di rosso (negli 8 bit superiori).</span><span class="sxs-lookup"><span data-stu-id="02b4e-263">The first pixel in the pair contains 8 bits of green (in the low 8 bits) and 8 bits of red (in the high 8 bits).</span></span> <span data-ttu-id="02b4e-264">Il secondo pixel contiene 8 bit di verde (negli 8 bit bassi) e 8 bit di blu (negli 8 bit superiori).</span><span class="sxs-lookup"><span data-stu-id="02b4e-264">The second pixel contains 8 bits of green (in the low 8 bits) and 8 bits of blue (in the high 8 bits).</span></span> <span data-ttu-id="02b4e-265">Insieme, i due pixel condividono i componenti rosso e blu, mentre ognuno ha un componente verde univoco (R0G0, B0G1, R2G2 e così via).</span><span class="sxs-lookup"><span data-stu-id="02b4e-265">Together, the two pixels share the red and blue components, while each has a unique green component (R0G0, B0G1, R2G2, and so on).</span></span> <span data-ttu-id="02b4e-266">Il campionatore di trame non normalizza i colori durante la ricerca in un pixel shader; rimangono nell'intervallo da 0,0 f a 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="02b4e-266">The texture sampler does not normalize the colors when looking up into a pixel shader; they remain in the range of 0.0f to 255.0f.</span></span> <span data-ttu-id="02b4e-267">Questo vale per tutti i modelli di pixel shader programmabili.</span><span class="sxs-lookup"><span data-stu-id="02b4e-267">This is true for all programmable pixel shader models.</span></span> <span data-ttu-id="02b4e-268">Per la funzione Fixed pixel shader, l'hardware deve normalizzarsi nell'intervallo da 0. f a 1. f e essenzialmente considerarlo come trama YUY2.</span><span class="sxs-lookup"><span data-stu-id="02b4e-268">For the fixed function pixel shader, the hardware should normalize to the 0.f to 1.f range and essentially treat it as the YUY2 texture.</span></span> <span data-ttu-id="02b4e-269">Per l'hardware che espone questo formato il membro PixelShader1xMaxValue di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) deve essere impostato su un valore in grado di gestire tale intervallo.</span><span class="sxs-lookup"><span data-stu-id="02b4e-269">Hardware that exposes this format must have PixelShader1xMaxValue member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) set to a value capable of handling that range.</span></span>     |
| <span data-ttu-id="02b4e-270">**\_UYVY D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-270">**D3DFMT\_UYVY**</span></span>          | <span data-ttu-id="02b4e-271">MAKEFOURCC (' U ',' Y ',' V',' Y ')</span><span class="sxs-lookup"><span data-stu-id="02b4e-271">MAKEFOURCC('U', 'Y', 'V', 'Y')</span></span> | <span data-ttu-id="02b4e-272">Formato UYVY (conformità PC98)</span><span class="sxs-lookup"><span data-stu-id="02b4e-272">UYVY format (PC98 compliance)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="02b4e-273">**\_YUY2 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-273">**D3DFMT\_YUY2**</span></span>          | <span data-ttu-id="02b4e-274">MAKEFOURCC (' Y ',' U ',' Y ',' 2')</span><span class="sxs-lookup"><span data-stu-id="02b4e-274">MAKEFOURCC('Y', 'U', 'Y', '2')</span></span> | <span data-ttu-id="02b4e-275">Formato YUY2 (conformità PC98)</span><span class="sxs-lookup"><span data-stu-id="02b4e-275">YUY2 format (PC98 compliance)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a><span data-ttu-id="02b4e-276">Formati IEEE</span><span class="sxs-lookup"><span data-stu-id="02b4e-276">IEEE Formats</span></span>

<span data-ttu-id="02b4e-277">Questi flag vengono utilizzati per i formati di superficie a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="02b4e-277">These flags are used for floating-point surface formats.</span></span> <span data-ttu-id="02b4e-278">Questi formati 32-bits per canale sono noti anche come formati s23e8.</span><span class="sxs-lookup"><span data-stu-id="02b4e-278">These 32-bits-per-channel formats are also known as s23e8 formats.</span></span>



| <span data-ttu-id="02b4e-279">Flag a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="02b4e-279">Floating-point flags</span></span>      | <span data-ttu-id="02b4e-280">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-280">Value</span></span> | <span data-ttu-id="02b4e-281">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-281">Format</span></span>                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b4e-282">**\_R32F D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-282">**D3DFMT\_R32F**</span></span>          | <span data-ttu-id="02b4e-283">114</span><span class="sxs-lookup"><span data-stu-id="02b4e-283">114</span></span>   | <span data-ttu-id="02b4e-284">formato float a 32 bit con 32 bit per il canale rosso.</span><span class="sxs-lookup"><span data-stu-id="02b4e-284">32-bit float format using 32 bits for the red channel.</span></span>                                   |
| <span data-ttu-id="02b4e-285">**\_G32R32F D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-285">**D3DFMT\_G32R32F**</span></span>       | <span data-ttu-id="02b4e-286">115</span><span class="sxs-lookup"><span data-stu-id="02b4e-286">115</span></span>   | <span data-ttu-id="02b4e-287">formato float a 64 bit con 32 bit per il canale rosso e 32 bit per il canale verde.</span><span class="sxs-lookup"><span data-stu-id="02b4e-287">64-bit float format using 32 bits for the red channel and 32 bits for the green channel.</span></span> |
| <span data-ttu-id="02b4e-288">**\_A32B32G32R32F D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-288">**D3DFMT\_A32B32G32R32F**</span></span> | <span data-ttu-id="02b4e-289">116</span><span class="sxs-lookup"><span data-stu-id="02b4e-289">116</span></span>   | <span data-ttu-id="02b4e-290">formato float a 128 bit con 32 bit per ogni canale (alfa, blu, verde, rosso).</span><span class="sxs-lookup"><span data-stu-id="02b4e-290">128-bit float format using 32 bits for the each channel (alpha, blue, green, red).</span></span>       |



 

### <a name="mixed-formats"></a><span data-ttu-id="02b4e-291">Formati misti</span><span class="sxs-lookup"><span data-stu-id="02b4e-291">Mixed Formats</span></span>

<span data-ttu-id="02b4e-292">I dati in formati misti possono contenere una combinazione di dati non firmati e dati firmati.</span><span class="sxs-lookup"><span data-stu-id="02b4e-292">Data in mixed formats can contain a combination of unsigned data and signed data.</span></span>



| <span data-ttu-id="02b4e-293">Flag di formato misto</span><span class="sxs-lookup"><span data-stu-id="02b4e-293">Mixed format flags</span></span>      | <span data-ttu-id="02b4e-294">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-294">Value</span></span> | <span data-ttu-id="02b4e-295">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-295">Format</span></span>                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b4e-296">**\_L6V5U5 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-296">**D3DFMT\_L6V5U5**</span></span>      | <span data-ttu-id="02b4e-297">61</span><span class="sxs-lookup"><span data-stu-id="02b4e-297">61</span></span>    | <span data-ttu-id="02b4e-298">formato di mappa Bump a 16 bit con luminanza usando 6 bit per la luminanza e 5 bit per v e l'utente.</span><span class="sxs-lookup"><span data-stu-id="02b4e-298">16-bit bump-map format with luminance using 6 bits for luminance, and 5 bits each for v and u.</span></span> |
| <span data-ttu-id="02b4e-299">**\_X8L8V8U8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-299">**D3DFMT\_X8L8V8U8**</span></span>    | <span data-ttu-id="02b4e-300">62</span><span class="sxs-lookup"><span data-stu-id="02b4e-300">62</span></span>    | <span data-ttu-id="02b4e-301">formato di mappa Bump a 32 bit con luminanza con 8 bit per ogni canale.</span><span class="sxs-lookup"><span data-stu-id="02b4e-301">32-bit bump-map format with luminance using 8 bits for each channel.</span></span>                           |
| <span data-ttu-id="02b4e-302">**\_A2W10V10U10 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-302">**D3DFMT\_A2W10V10U10**</span></span> | <span data-ttu-id="02b4e-303">67</span><span class="sxs-lookup"><span data-stu-id="02b4e-303">67</span></span>    | <span data-ttu-id="02b4e-304">formato di mappa Bump a 32 bit che usa 2 bit per Alpha e 10 bit ciascuno per w, v e l'utente.</span><span class="sxs-lookup"><span data-stu-id="02b4e-304">32-bit bump-map format using 2 bits for alpha and 10 bits each for w, v, and u.</span></span>                |



 

### <a name="signed-formats"></a><span data-ttu-id="02b4e-305">Formati firmati</span><span class="sxs-lookup"><span data-stu-id="02b4e-305">Signed Formats</span></span>

<span data-ttu-id="02b4e-306">I dati in un formato firmato possono essere sia positivi che negativi.</span><span class="sxs-lookup"><span data-stu-id="02b4e-306">Data in a signed format can be both positive and negative.</span></span> <span data-ttu-id="02b4e-307">I formati firmati usano combinazioni di dati (U), (V), (W) e (Q).</span><span class="sxs-lookup"><span data-stu-id="02b4e-307">Signed formats use combinations of (U), (V), (W), and (Q) data.</span></span>



| <span data-ttu-id="02b4e-308">Flag di formato firmato</span><span class="sxs-lookup"><span data-stu-id="02b4e-308">Signed format flags</span></span>      | <span data-ttu-id="02b4e-309">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-309">Value</span></span> | <span data-ttu-id="02b4e-310">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-310">Format</span></span>                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b4e-311">**\_V8U8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-311">**D3DFMT\_V8U8**</span></span>         | <span data-ttu-id="02b4e-312">60</span><span class="sxs-lookup"><span data-stu-id="02b4e-312">60</span></span>    | <span data-ttu-id="02b4e-313">formato della mappa Bump a 16 bit con 8 bit ciascuno per i dati utente e v.</span><span class="sxs-lookup"><span data-stu-id="02b4e-313">16-bit bump-map format using 8 bits each for u and v data.</span></span>                                                |
| <span data-ttu-id="02b4e-314">**\_Q8W8V8U8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-314">**D3DFMT\_Q8W8V8U8**</span></span>     | <span data-ttu-id="02b4e-315">63</span><span class="sxs-lookup"><span data-stu-id="02b4e-315">63</span></span>    | <span data-ttu-id="02b4e-316">formato di mappa Bump a 32 bit con 8 bit per ogni canale.</span><span class="sxs-lookup"><span data-stu-id="02b4e-316">32-bit bump-map format using 8 bits for each channel.</span></span>                                                     |
| <span data-ttu-id="02b4e-317">**\_V16U16 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-317">**D3DFMT\_V16U16**</span></span>       | <span data-ttu-id="02b4e-318">64</span><span class="sxs-lookup"><span data-stu-id="02b4e-318">64</span></span>    | <span data-ttu-id="02b4e-319">formato di mappa Bump a 32 bit con 16 bit per ogni canale.</span><span class="sxs-lookup"><span data-stu-id="02b4e-319">32-bit bump-map format using 16 bits for each channel.</span></span>                                                    |
| <span data-ttu-id="02b4e-320">**\_Q16W16V16U16 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-320">**D3DFMT\_Q16W16V16U16**</span></span> | <span data-ttu-id="02b4e-321">110</span><span class="sxs-lookup"><span data-stu-id="02b4e-321">110</span></span>   | <span data-ttu-id="02b4e-322">formato di mappa Bump a 64 bit con 16 bit per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="02b4e-322">64-bit bump-map format using 16 bits for each component.</span></span>                                                  |
| <span data-ttu-id="02b4e-323">**\_CXV8U8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-323">**D3DFMT\_CxV8U8**</span></span>       | <span data-ttu-id="02b4e-324">117</span><span class="sxs-lookup"><span data-stu-id="02b4e-324">117</span></span>   | <span data-ttu-id="02b4e-325">formato di compressione normale a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-325">16-bit normal compression format.</span></span> <span data-ttu-id="02b4e-326">Il campionatore di trame calcola il canale C da: C = sqrt (1-U ²-V ²).</span><span class="sxs-lookup"><span data-stu-id="02b4e-326">The texture sampler computes the C channel from: C = sqrt(1 - U² - V²).</span></span> |



 

### <a name="unsigned-formats"></a><span data-ttu-id="02b4e-327">Formati non firmati</span><span class="sxs-lookup"><span data-stu-id="02b4e-327">Unsigned Formats</span></span>

<span data-ttu-id="02b4e-328">I dati in un formato senza segno devono essere positivi.</span><span class="sxs-lookup"><span data-stu-id="02b4e-328">Data in an unsigned format must be positive.</span></span> <span data-ttu-id="02b4e-329">I formati non firmati usano combinazioni di dati (R) ed, (G) reen, (B) lue, (A) lpha, (L) uminance e (P) alette dei colori.</span><span class="sxs-lookup"><span data-stu-id="02b4e-329">Unsigned formats use combinations of (R)ed, (G)reen, (B)lue, (A)lpha, (L)uminance, and (P)alette data.</span></span> <span data-ttu-id="02b4e-330">I dati della tavolozza sono anche denominati dati indicizzati a colori perché i dati vengono utilizzati per indicizzare una tavolozza dei colori.</span><span class="sxs-lookup"><span data-stu-id="02b4e-330">Palette data is also referred to as color indexed data because the data is used to index a color palette.</span></span>



| <span data-ttu-id="02b4e-331">Flag di formato senza segno</span><span class="sxs-lookup"><span data-stu-id="02b4e-331">Unsigned format flags</span></span>             | <span data-ttu-id="02b4e-332">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-332">Value</span></span> | <span data-ttu-id="02b4e-333">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-333">Format</span></span>                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b4e-334">**\_R8G8B8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-334">**D3DFMT\_R8G8B8**</span></span>                | <span data-ttu-id="02b4e-335">20</span><span class="sxs-lookup"><span data-stu-id="02b4e-335">20</span></span>    | <span data-ttu-id="02b4e-336">formato pixel RGB a 24 bit con 8 bit per canale.</span><span class="sxs-lookup"><span data-stu-id="02b4e-336">24-bit RGB pixel format with 8 bits per channel.</span></span>                                                                                                                          |
| <span data-ttu-id="02b4e-337">**\_A8R8G8B8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-337">**D3DFMT\_A8R8G8B8**</span></span>              | <span data-ttu-id="02b4e-338">21</span><span class="sxs-lookup"><span data-stu-id="02b4e-338">21</span></span>    | <span data-ttu-id="02b4e-339">formato pixel ARGB a 32 bit con Alpha, con 8 bit per canale.</span><span class="sxs-lookup"><span data-stu-id="02b4e-339">32-bit ARGB pixel format with alpha, using 8 bits per channel.</span></span>                                                                                                            |
| <span data-ttu-id="02b4e-340">**\_X8R8G8B8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-340">**D3DFMT\_X8R8G8B8**</span></span>              | <span data-ttu-id="02b4e-341">22</span><span class="sxs-lookup"><span data-stu-id="02b4e-341">22</span></span>    | <span data-ttu-id="02b4e-342">formato pixel RGB a 32 bit, dove 8 bit sono riservati per ogni colore.</span><span class="sxs-lookup"><span data-stu-id="02b4e-342">32-bit RGB pixel format, where 8 bits are reserved for each color.</span></span>                                                                                                        |
| <span data-ttu-id="02b4e-343">**\_R5G6B5 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-343">**D3DFMT\_R5G6B5**</span></span>                | <span data-ttu-id="02b4e-344">23</span><span class="sxs-lookup"><span data-stu-id="02b4e-344">23</span></span>    | <span data-ttu-id="02b4e-345">formato pixel RGB a 16 bit con 5 bit per il rosso, 6 bit per il verde e 5 bit per il blu.</span><span class="sxs-lookup"><span data-stu-id="02b4e-345">16-bit RGB pixel format with 5 bits for red, 6 bits for green, and 5 bits for blue.</span></span>                                                                                       |
| <span data-ttu-id="02b4e-346">**\_X1R5G5B5 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-346">**D3DFMT\_X1R5G5B5**</span></span>              | <span data-ttu-id="02b4e-347">24</span><span class="sxs-lookup"><span data-stu-id="02b4e-347">24</span></span>    | <span data-ttu-id="02b4e-348">formato pixel a 16 bit in cui 5 bit sono riservati per ogni colore.</span><span class="sxs-lookup"><span data-stu-id="02b4e-348">16-bit pixel format where 5 bits are reserved for each color.</span></span>                                                                                                             |
| <span data-ttu-id="02b4e-349">**\_A1R5G5B5 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-349">**D3DFMT\_A1R5G5B5**</span></span>              | <span data-ttu-id="02b4e-350">25</span><span class="sxs-lookup"><span data-stu-id="02b4e-350">25</span></span>    | <span data-ttu-id="02b4e-351">formato pixel a 16 bit in cui 5 bit sono riservati per ogni colore e 1 bit è riservato per Alpha.</span><span class="sxs-lookup"><span data-stu-id="02b4e-351">16-bit pixel format where 5 bits are reserved for each color and 1 bit is reserved for alpha.</span></span>                                                                             |
| <span data-ttu-id="02b4e-352">**\_A4R4G4B4 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-352">**D3DFMT\_A4R4G4B4**</span></span>              | <span data-ttu-id="02b4e-353">26</span><span class="sxs-lookup"><span data-stu-id="02b4e-353">26</span></span>    | <span data-ttu-id="02b4e-354">formato pixel ARGB a 16 bit con 4 bit per ogni canale.</span><span class="sxs-lookup"><span data-stu-id="02b4e-354">16-bit ARGB pixel format with 4 bits for each channel.</span></span>                                                                                                                    |
| <span data-ttu-id="02b4e-355">**\_R3G3B2 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-355">**D3DFMT\_R3G3B2**</span></span>                | <span data-ttu-id="02b4e-356">27</span><span class="sxs-lookup"><span data-stu-id="02b4e-356">27</span></span>    | <span data-ttu-id="02b4e-357">formato di trama RGB a 8 bit con 3 bit per il rosso, 3 bit per il verde e 2 bit per il blu.</span><span class="sxs-lookup"><span data-stu-id="02b4e-357">8-bit RGB texture format using 3 bits for red, 3 bits for green, and 2 bits for blue.</span></span>                                                                                     |
| <span data-ttu-id="02b4e-358">**D3DFMT \_ a8**</span><span class="sxs-lookup"><span data-stu-id="02b4e-358">**D3DFMT\_A8**</span></span>                    | <span data-ttu-id="02b4e-359">28</span><span class="sxs-lookup"><span data-stu-id="02b4e-359">28</span></span>    | <span data-ttu-id="02b4e-360">solo Alpha a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-360">8-bit alpha only.</span></span>                                                                                                                                                         |
| <span data-ttu-id="02b4e-361">**\_A8R3G3B2 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-361">**D3DFMT\_A8R3G3B2**</span></span>              | <span data-ttu-id="02b4e-362">29</span><span class="sxs-lookup"><span data-stu-id="02b4e-362">29</span></span>    | <span data-ttu-id="02b4e-363">formato di trama ARGB a 16 bit con 8 bit per alfa, 3 bit per colore rosso e verde e 2 bit per il blu.</span><span class="sxs-lookup"><span data-stu-id="02b4e-363">16-bit ARGB texture format using 8 bits for alpha, 3 bits each for red and green, and 2 bits for blue.</span></span>                                                                    |
| <span data-ttu-id="02b4e-364">**\_X4R4G4B4 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-364">**D3DFMT\_X4R4G4B4**</span></span>              | <span data-ttu-id="02b4e-365">30</span><span class="sxs-lookup"><span data-stu-id="02b4e-365">30</span></span>    | <span data-ttu-id="02b4e-366">formato pixel RGB a 16 bit con 4 bit per ogni colore.</span><span class="sxs-lookup"><span data-stu-id="02b4e-366">16-bit RGB pixel format using 4 bits for each color.</span></span>                                                                                                                      |
| <span data-ttu-id="02b4e-367">**\_A2B10G10R10 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-367">**D3DFMT\_A2B10G10R10**</span></span>           | <span data-ttu-id="02b4e-368">31</span><span class="sxs-lookup"><span data-stu-id="02b4e-368">31</span></span>    | <span data-ttu-id="02b4e-369">formato pixel a 32 bit che usa 10 bit per ogni colore e 2 bit per alfa.</span><span class="sxs-lookup"><span data-stu-id="02b4e-369">32-bit pixel format using 10 bits for each color and 2 bits for alpha.</span></span>                                                                                                    |
| <span data-ttu-id="02b4e-370">**\_A8B8G8R8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-370">**D3DFMT\_A8B8G8R8**</span></span>              | <span data-ttu-id="02b4e-371">32</span><span class="sxs-lookup"><span data-stu-id="02b4e-371">32</span></span>    | <span data-ttu-id="02b4e-372">formato pixel ARGB a 32 bit con Alpha, con 8 bit per canale.</span><span class="sxs-lookup"><span data-stu-id="02b4e-372">32-bit ARGB pixel format with alpha, using 8 bits per channel.</span></span>                                                                                                            |
| <span data-ttu-id="02b4e-373">**\_X8B8G8R8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-373">**D3DFMT\_X8B8G8R8**</span></span>              | <span data-ttu-id="02b4e-374">33</span><span class="sxs-lookup"><span data-stu-id="02b4e-374">33</span></span>    | <span data-ttu-id="02b4e-375">formato pixel RGB a 32 bit, dove 8 bit sono riservati per ogni colore.</span><span class="sxs-lookup"><span data-stu-id="02b4e-375">32-bit RGB pixel format, where 8 bits are reserved for each color.</span></span>                                                                                                        |
| <span data-ttu-id="02b4e-376">**\_G16R16 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-376">**D3DFMT\_G16R16**</span></span>                | <span data-ttu-id="02b4e-377">34</span><span class="sxs-lookup"><span data-stu-id="02b4e-377">34</span></span>    | <span data-ttu-id="02b4e-378">formato pixel a 32 bit con 16 bit ciascuno per verde e rosso.</span><span class="sxs-lookup"><span data-stu-id="02b4e-378">32-bit pixel format using 16 bits each for green and red.</span></span>                                                                                                                 |
| <span data-ttu-id="02b4e-379">**\_A2R10G10B10 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-379">**D3DFMT\_A2R10G10B10**</span></span>           | <span data-ttu-id="02b4e-380">35</span><span class="sxs-lookup"><span data-stu-id="02b4e-380">35</span></span>    | <span data-ttu-id="02b4e-381">formato pixel a 32 bit che usa 10 bit per ogni rosso, verde e blu e 2 bit per alfa.</span><span class="sxs-lookup"><span data-stu-id="02b4e-381">32-bit pixel format using 10 bits each for red, green, and blue, and 2 bits for alpha.</span></span>                                                                                    |
| <span data-ttu-id="02b4e-382">**\_A16B16G16R16 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-382">**D3DFMT\_A16B16G16R16**</span></span>          | <span data-ttu-id="02b4e-383">36</span><span class="sxs-lookup"><span data-stu-id="02b4e-383">36</span></span>    | <span data-ttu-id="02b4e-384">formato pixel a 64 bit con 16 bit per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="02b4e-384">64-bit pixel format using 16 bits for each component.</span></span>                                                                                                                     |
| <span data-ttu-id="02b4e-385">**\_A8P8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-385">**D3DFMT\_A8P8**</span></span>                  | <span data-ttu-id="02b4e-386">40</span><span class="sxs-lookup"><span data-stu-id="02b4e-386">40</span></span>    | <span data-ttu-id="02b4e-387">colore a 8 bit indicizzato con 8 bit di alfa.</span><span class="sxs-lookup"><span data-stu-id="02b4e-387">8-bit color indexed with 8 bits of alpha.</span></span>                                                                                                                                 |
| <span data-ttu-id="02b4e-388">**D3DFMT \_ P8**</span><span class="sxs-lookup"><span data-stu-id="02b4e-388">**D3DFMT\_P8**</span></span>                    | <span data-ttu-id="02b4e-389">41</span><span class="sxs-lookup"><span data-stu-id="02b4e-389">41</span></span>    | <span data-ttu-id="02b4e-390">colore a 8 bit indicizzato.</span><span class="sxs-lookup"><span data-stu-id="02b4e-390">8-bit color indexed.</span></span>                                                                                                                                                      |
| <span data-ttu-id="02b4e-391">**\_L8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-391">**D3DFMT\_L8**</span></span>                    | <span data-ttu-id="02b4e-392">50</span><span class="sxs-lookup"><span data-stu-id="02b4e-392">50</span></span>    | <span data-ttu-id="02b4e-393">solo luminanza a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-393">8-bit luminance only.</span></span>                                                                                                                                                     |
| <span data-ttu-id="02b4e-394">**\_L16 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-394">**D3DFMT\_L16**</span></span>                   | <span data-ttu-id="02b4e-395">81</span><span class="sxs-lookup"><span data-stu-id="02b4e-395">81</span></span>    | <span data-ttu-id="02b4e-396">solo luminanza a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-396">16-bit luminance only.</span></span>                                                                                                                                                    |
| <span data-ttu-id="02b4e-397">**\_A8L8 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-397">**D3DFMT\_A8L8**</span></span>                  | <span data-ttu-id="02b4e-398">51</span><span class="sxs-lookup"><span data-stu-id="02b4e-398">51</span></span>    | <span data-ttu-id="02b4e-399">a 16 bit con 8 bit per alfa e luminanza.</span><span class="sxs-lookup"><span data-stu-id="02b4e-399">16-bit using 8 bits each for alpha and luminance.</span></span>                                                                                                                         |
| <span data-ttu-id="02b4e-400">**\_A4L4 D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-400">**D3DFMT\_A4L4**</span></span>                  | <span data-ttu-id="02b4e-401">52</span><span class="sxs-lookup"><span data-stu-id="02b4e-401">52</span></span>    | <span data-ttu-id="02b4e-402">a 8 bit con 4 bit per alfa e luminanza.</span><span class="sxs-lookup"><span data-stu-id="02b4e-402">8-bit using 4 bits each for alpha and luminance.</span></span>                                                                                                                          |
| <span data-ttu-id="02b4e-403">**D3DFMT \_ a1**</span><span class="sxs-lookup"><span data-stu-id="02b4e-403">**D3DFMT\_A1**</span></span>                    | <span data-ttu-id="02b4e-404">118</span><span class="sxs-lookup"><span data-stu-id="02b4e-404">118</span></span>   | <span data-ttu-id="02b4e-405">monocromatico a 1 bit.</span><span class="sxs-lookup"><span data-stu-id="02b4e-405">1-bit monochrome.</span></span> <span data-ttu-id="02b4e-406">**Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="02b4e-406">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>                                            |
| <span data-ttu-id="02b4e-407">**D3DFMT \_ A2B10G10R10 \_ XR \_ Bias**</span><span class="sxs-lookup"><span data-stu-id="02b4e-407">**D3DFMT\_A2B10G10R10\_XR\_BIAS**</span></span> | <span data-ttu-id="02b4e-408">119</span><span class="sxs-lookup"><span data-stu-id="02b4e-408">119</span></span>   | <span data-ttu-id="02b4e-409">2,8-punto fisso distorta.</span><span class="sxs-lookup"><span data-stu-id="02b4e-409">2.8-biased fixed point.</span></span> <span data-ttu-id="02b4e-410">**Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="02b4e-410">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>                                      |
| <span data-ttu-id="02b4e-411">**\_BINARYBUFFER D3DFMT**</span><span class="sxs-lookup"><span data-stu-id="02b4e-411">**D3DFMT\_BINARYBUFFER**</span></span>          | <span data-ttu-id="02b4e-412">199</span><span class="sxs-lookup"><span data-stu-id="02b4e-412">199</span></span>   | <span data-ttu-id="02b4e-413">Formato binario che indica che i dati non hanno un tipo intrinseco.</span><span class="sxs-lookup"><span data-stu-id="02b4e-413">Binary format indicating that the data has no inherent type.</span></span> <span data-ttu-id="02b4e-414">**Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="02b4e-414">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

### <a name="other"></a><span data-ttu-id="02b4e-415">Altro</span><span class="sxs-lookup"><span data-stu-id="02b4e-415">Other</span></span>

<span data-ttu-id="02b4e-416">Questo flag viene utilizzato per i formati non definiti.</span><span class="sxs-lookup"><span data-stu-id="02b4e-416">This flag is used for undefined formats.</span></span>



| <span data-ttu-id="02b4e-417">Altri flag</span><span class="sxs-lookup"><span data-stu-id="02b4e-417">Other flags</span></span>         | <span data-ttu-id="02b4e-418">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-418">Value</span></span> | <span data-ttu-id="02b4e-419">Formato</span><span class="sxs-lookup"><span data-stu-id="02b4e-419">Format</span></span>                    |
|---------------------|-------|---------------------------|
| <span data-ttu-id="02b4e-420">**D3DFMT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="02b4e-420">**D3DFMT\_UNKNOWN**</span></span> | <span data-ttu-id="02b4e-421">0</span><span class="sxs-lookup"><span data-stu-id="02b4e-421">0</span></span>     | <span data-ttu-id="02b4e-422">Il formato della superficie è sconosciuto</span><span class="sxs-lookup"><span data-stu-id="02b4e-422">Surface format is unknown</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="02b4e-423">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02b4e-423">Requirements</span></span>



| <span data-ttu-id="02b4e-424">Requisito</span><span class="sxs-lookup"><span data-stu-id="02b4e-424">Requirement</span></span> | <span data-ttu-id="02b4e-425">Valore</span><span class="sxs-lookup"><span data-stu-id="02b4e-425">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02b4e-426">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02b4e-426">Header</span></span><br/> | <dl> <span data-ttu-id="02b4e-427"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="02b4e-427"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02b4e-428">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02b4e-428">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b4e-429">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="02b4e-429">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




