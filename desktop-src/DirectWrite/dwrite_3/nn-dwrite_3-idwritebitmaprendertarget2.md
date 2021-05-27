---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Incapsula una bitmap indipendente dal dispositivo a 32 bit e un contesto di dispositivo, che può essere usato per il rendering dei glifi.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: 346b2e9c7510010abb50f421489b67f7d327512f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548946"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a><span data-ttu-id="92694-103">Interfaccia IDWriteBitmapRenderTarget2 (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="92694-103">IDWriteBitmapRenderTarget2 interface (dwrite_3.h)</span></span>

<span data-ttu-id="92694-104">Incapsula una bitmap indipendente dal dispositivo a 32 bit e un contesto di dispositivo, che può essere usato per il rendering dei glifi.</span><span class="sxs-lookup"><span data-stu-id="92694-104">Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92694-105">Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md)</span><span class="sxs-lookup"><span data-stu-id="92694-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="92694-106">DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme.</span><span class="sxs-lookup"><span data-stu-id="92694-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="92694-107">Per altre informazioni ed esempi di codice, vedi [Panoramica di DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="92694-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="inheritance"></a><span data-ttu-id="92694-108">Ereditarietà</span><span class="sxs-lookup"><span data-stu-id="92694-108">Inheritance</span></span>

<span data-ttu-id="92694-109">**L'interfaccia IDWriteBitmapRenderTarget2** eredita da [IDWriteBitmapRenderTarget1.](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)</span><span class="sxs-lookup"><span data-stu-id="92694-109">The **IDWriteBitmapRenderTarget2** interface inherits from [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span></span>

## <a name="methods"></a><span data-ttu-id="92694-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="92694-110">Methods</span></span>

<span data-ttu-id="92694-111">**L'interfaccia IDWriteBitmapRenderTarget2** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="92694-111">The **IDWriteBitmapRenderTarget2** interface has these methods.</span></span>

| <span data-ttu-id="92694-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="92694-112">Method</span></span> | <span data-ttu-id="92694-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92694-113">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="92694-114">IDWriteBitmapRenderTarget2::GetBitmapData</span><span class="sxs-lookup"><span data-stu-id="92694-114">IDWriteBitmapRenderTarget2::GetBitmapData</span></span>](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | <span data-ttu-id="92694-115">Recupera i dati pixel da una destinazione di rendering bitmap.</span><span class="sxs-lookup"><span data-stu-id="92694-115">Retrieves the pixel data from a bitmap render target.</span></span> |

## <a name="requirements"></a><span data-ttu-id="92694-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92694-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="92694-117">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="92694-117">**Minimum supported client**</span></span> | <span data-ttu-id="92694-118">Windows 10, Project Dispositivi [app Win32]</span><span class="sxs-lookup"><span data-stu-id="92694-118">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="92694-119">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="92694-119">**Header**</span></span> | <span data-ttu-id="92694-120">dwrite_3.h (includere dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="92694-120">dwrite_3.h (include dwrite_core.h)</span></span> |