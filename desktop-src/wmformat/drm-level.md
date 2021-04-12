---
title: DRM_Level
description: '\_Il livello DRM è un attributo di licenza impostato da Windows Media Format SDK quando crea una licenza locale per i file protetti con la versione 1 di DRM.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336426"
---
# <a name="drm_level"></a><span data-ttu-id="1c5b4-104">\_Livello DRM</span><span class="sxs-lookup"><span data-stu-id="1c5b4-104">DRM\_Level</span></span>

<span data-ttu-id="1c5b4-105">**DRM \_ Level** è un attributo di licenza impostato da Windows Media Format SDK quando crea una licenza locale per i file protetti con la versione 1 di DRM.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-105">**DRM\_Level** is a license attribute that the Windows Media Format SDK sets when it creates a local license for files protected with DRM version 1.</span></span> <span data-ttu-id="1c5b4-106">Contiene il livello di sicurezza che l'applicazione chiamante deve avere per accedere al contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-106">It contains the security level that the calling application must have to access the content in the file.</span></span> <span data-ttu-id="1c5b4-107">Il valore predefinito è 150.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-107">The default value is 150.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1c5b4-108">Costante globale</span><span class="sxs-lookup"><span data-stu-id="1c5b4-108">Global Constant</span></span>

<span data-ttu-id="1c5b4-109">\_livello g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="1c5b4-109">g\_wszWMDRM\_Level</span></span>

## <a name="data-type"></a><span data-ttu-id="1c5b4-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1c5b4-110">Data Type</span></span>

<span data-ttu-id="1c5b4-111">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1c5b4-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="1c5b4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c5b4-112">Remarks</span></span>

<span data-ttu-id="1c5b4-113">Il livello di sicurezza DRM di un'applicazione è determinato dalla particolare libreria WMStubDRM a cui si collega in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-113">An application's DRM security level is determined by the particular wmstubdrm library that it links to at compile time.</span></span> <span data-ttu-id="1c5b4-114">Per ulteriori informazioni su questi livelli di sicurezza, vedere [ottenere la libreria DRM necessaria](obtaining-the-required-drm-library.md).</span><span class="sxs-lookup"><span data-stu-id="1c5b4-114">For more information on these security levels, see [Obtaining the Required DRM Library](obtaining-the-required-drm-library.md).</span></span> <span data-ttu-id="1c5b4-115">Usare [**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) per impostare questa proprietà quando si proteggono i file ASF con DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when protecting ASF files with DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c5b4-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c5b4-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5b4-117">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="1c5b4-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




