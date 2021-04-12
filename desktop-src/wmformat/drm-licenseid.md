---
title: DRM_LicenseID
description: La \_ Proprietà DRM LicenseID contiene una stringa recuperata dalla licenza associata al file attualmente aperto che identifica in modo univoco la licenza.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336425"
---
# <a name="drm_licenseid"></a><span data-ttu-id="e6455-104">\_LICENSEID DRM</span><span class="sxs-lookup"><span data-stu-id="e6455-104">DRM\_LicenseID</span></span>

<span data-ttu-id="e6455-105">La proprietà **DRM \_ LicenseID** contiene una stringa recuperata dalla licenza associata al file attualmente aperto che identifica in modo univoco la licenza.</span><span class="sxs-lookup"><span data-stu-id="e6455-105">The **DRM\_LicenseID** property contains a string retrieved from the license associated with the currently open file that uniquely identifies that license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="e6455-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="e6455-106">Global Constant</span></span>

<span data-ttu-id="e6455-107">g \_ wszWMDRM \_ LicenseID</span><span class="sxs-lookup"><span data-stu-id="e6455-107">g\_wszWMDRM\_LicenseID</span></span>

## <a name="data-type"></a><span data-ttu-id="e6455-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e6455-108">Data Type</span></span>

<span data-ttu-id="e6455-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e6455-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="e6455-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6455-110">Remarks</span></span>

<span data-ttu-id="e6455-111">Questo attributo è presente solo con contenuto DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="e6455-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="e6455-112">Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="e6455-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

<span data-ttu-id="e6455-113">L'ID licenza viene archiviato in una licenza, non in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="e6455-113">The license ID is stored in a license, not in an ASF file.</span></span> <span data-ttu-id="e6455-114">Ogni singola licenza dispone di un ID univoco assegnato dal generatore di licenze al momento della creazione della licenza.</span><span class="sxs-lookup"><span data-stu-id="e6455-114">Each individual license has a unique ID which is assigned by the license generator at the time the license is created.</span></span> <span data-ttu-id="e6455-115">Se ad esempio si ottengono due licenze per lo stesso contenuto, ciascuna di esse avrà un attributo LicenseID diverso.</span><span class="sxs-lookup"><span data-stu-id="e6455-115">For example, if you obtain two licenses for the same content, each one will have a different LicenseID attribute.</span></span> <span data-ttu-id="e6455-116">In genere, le applicazioni non devono recuperare questo valore.</span><span class="sxs-lookup"><span data-stu-id="e6455-116">Typically, applications have no need to retrieve this value.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6455-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6455-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6455-118">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="e6455-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




