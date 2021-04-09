---
title: DRM_Flags
description: La \_ Proprietà flag DRM viene utilizzata con contenuto DRM versione 1 solo per specificare i diritti che saranno contenuti nella licenza locale.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956185"
---
# <a name="drm_flags"></a><span data-ttu-id="84572-104">\_Flag DRM</span><span class="sxs-lookup"><span data-stu-id="84572-104">DRM\_Flags</span></span>

<span data-ttu-id="84572-105">La **proprietà \_ flag DRM** viene utilizzata con contenuto DRM versione 1 solo per specificare i diritti che saranno contenuti nella licenza locale.</span><span class="sxs-lookup"><span data-stu-id="84572-105">The **DRM\_Flags** property is used with DRM version 1 content only to specify the rights that will be contained in the local license.</span></span> <span data-ttu-id="84572-106">I diritti vengono specificati con i valori definiti dal tipo di enumerazione **\_ dei diritti WMT** .</span><span class="sxs-lookup"><span data-stu-id="84572-106">Rights are specified with values defined by the **WMT\_RIGHTS** enumeration type.</span></span> <span data-ttu-id="84572-107">È possibile selezionare più di un valore unendoli con **l'operatore OR** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="84572-107">More than one value can be selected by combining them with the bitwise **OR** operator.</span></span>

## <a name="global-constant"></a><span data-ttu-id="84572-108">Costante globale</span><span class="sxs-lookup"><span data-stu-id="84572-108">Global Constant</span></span>

<span data-ttu-id="84572-109">\_flag g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="84572-109">g\_wszWMDRM\_Flags</span></span>

## <a name="data-type"></a><span data-ttu-id="84572-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="84572-110">Data Type</span></span>

<span data-ttu-id="84572-111">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="84572-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="84572-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="84572-112">Remarks</span></span>

<span data-ttu-id="84572-113">Quando si accede all'interfaccia **IWMHeaderInfo3** dell'oggetto writer, è possibile aggiungere o modificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="84572-113">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="84572-114">In altri oggetti (editor di metadati, lettore e lettore sincrono), questo valore è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="84572-114">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span> <span data-ttu-id="84572-115">Usare [**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) per impostare questa proprietà quando si crea contenuto DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="84572-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when creating DRM version 1 content.</span></span>

## <a name="see-also"></a><span data-ttu-id="84572-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84572-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84572-117">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="84572-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




