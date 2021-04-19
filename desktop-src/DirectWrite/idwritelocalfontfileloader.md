---
title: Interfaccia IDWriteLocalFontFileLoader
description: Implementazione incorporata dell'interfaccia IDWriteFontFileLoader, che opera sui file del tipo di carattere locale ed espone le informazioni sul file di tipo di carattere locale dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Scrittura diretta dell'interfaccia IDWriteLocalFontFileLoader
- Scrittura diretta dell'interfaccia IDWriteLocalFontFileLoader, descritta
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329139"
---
# <a name="idwritelocalfontfileloader-interface"></a><span data-ttu-id="3462e-105">Interfaccia IDWriteLocalFontFileLoader</span><span class="sxs-lookup"><span data-stu-id="3462e-105">IDWriteLocalFontFileLoader interface</span></span>

<span data-ttu-id="3462e-106">Implementazione incorporata dell'interfaccia [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , che opera sui file del tipo di carattere locale ed espone le informazioni sul file di tipo di carattere locale dalla chiave di riferimento del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="3462e-106">A built-in implementation of the [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) interface, that operates on local font files and exposes local font file information from the font file reference key.</span></span> <span data-ttu-id="3462e-107">I riferimenti ai file del tipo di carattere creati con [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usano questo caricatore di file di tipo</span><span class="sxs-lookup"><span data-stu-id="3462e-107">Font file references created using [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) use this font file loader.</span></span>

## <a name="members"></a><span data-ttu-id="3462e-108">Membri</span><span class="sxs-lookup"><span data-stu-id="3462e-108">Members</span></span>

<span data-ttu-id="3462e-109">L'interfaccia **IDWriteLocalFontFileLoader** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3462e-109">The **IDWriteLocalFontFileLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3462e-110">**IDWriteLocalFontFileLoader** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3462e-110">**IDWriteLocalFontFileLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="3462e-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="3462e-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3462e-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="3462e-112">Methods</span></span>

<span data-ttu-id="3462e-113">L'interfaccia **IDWriteLocalFontFileLoader** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3462e-113">The **IDWriteLocalFontFileLoader** interface has these methods.</span></span>



| <span data-ttu-id="3462e-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="3462e-114">Method</span></span>                                                                                  | <span data-ttu-id="3462e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3462e-115">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3462e-116">**GetFilePathFromKey**</span><span class="sxs-lookup"><span data-stu-id="3462e-116">**GetFilePathFromKey**</span></span>](idwritelocalfontfileloader-getfilepathfromkey.md)             | <span data-ttu-id="3462e-117">Ottiene il percorso del file del tipo di carattere assoluto dalla chiave di riferimento del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="3462e-117">Obtains the absolute font file path from the font file reference key.</span></span><br/>          |
| [<span data-ttu-id="3462e-118">**GetFilePathLengthFromKey**</span><span class="sxs-lookup"><span data-stu-id="3462e-118">**GetFilePathLengthFromKey**</span></span>](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | <span data-ttu-id="3462e-119">Ottiene la lunghezza del percorso del file assoluto dalla chiave di riferimento del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="3462e-119">Obtains the length of the absolute file path from the font file reference key.</span></span><br/> |
| [<span data-ttu-id="3462e-120">**GetLastWriteTimeFromKey**</span><span class="sxs-lookup"><span data-stu-id="3462e-120">**GetLastWriteTimeFromKey**</span></span>](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | <span data-ttu-id="3462e-121">Ottiene l'ora dell'ultima scrittura del file dalla chiave di riferimento del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="3462e-121">Obtains the last write time of the file from the font file reference key.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="3462e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3462e-122">Requirements</span></span>



| <span data-ttu-id="3462e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3462e-123">Requirement</span></span> | <span data-ttu-id="3462e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3462e-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3462e-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="3462e-125">Library</span></span><br/> | <dl> <span data-ttu-id="3462e-126"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3462e-126"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="3462e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3462e-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="3462e-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3462e-128"><dt>Dwrite.dll</dt></span></span> </dl> |



 

