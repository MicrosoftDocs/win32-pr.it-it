---
title: DRM_KeySeed
description: La \_ proprietà chiave di inizializzazione DRM contiene il valore di inizializzazione chiave che verrà usato insieme a keyId per creare la chiave.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed formato Windows Media
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299445"
---
# <a name="drm_keyseed"></a><span data-ttu-id="ad344-104">Valore di inizializzazione del valore DRM \_</span><span class="sxs-lookup"><span data-stu-id="ad344-104">DRM\_KeySeed</span></span>

<span data-ttu-id="ad344-105">La proprietà chiave di **\_ inizializzazione DRM** contiene il valore di inizializzazione chiave che verrà usato insieme a keyId per creare la chiave.</span><span class="sxs-lookup"><span data-stu-id="ad344-105">The **DRM\_KeySeed** property contains the key seed that will be used in conjunction with the KeyID to create the key.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ad344-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="ad344-106">Global Constant</span></span>

<span data-ttu-id="ad344-107">valore \_ di \_ inizializzazione g wszWMDRM</span><span class="sxs-lookup"><span data-stu-id="ad344-107">g\_wszWMDRM\_KeySeed</span></span>

## <a name="data-type"></a><span data-ttu-id="ad344-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ad344-108">Data Type</span></span>

<span data-ttu-id="ad344-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ad344-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="ad344-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad344-110">Remarks</span></span>

<span data-ttu-id="ad344-111">Questa proprietà può essere impostata utilizzando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="ad344-111">This property can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span> <span data-ttu-id="ad344-112">Non è accessibile dall'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="ad344-112">It is not accessible by the reader object.</span></span>

<span data-ttu-id="ad344-113">Un valore di inizializzazione chiave viene in genere usato per proteggere più file o set di file, ad esempio tutti i file emessi da un server licenze o forse tutti i file di un particolare artista.</span><span class="sxs-lookup"><span data-stu-id="ad344-113">A key seed is typically used to protect multiple files or sets of files, for example all the files issued by a license server, or perhaps all the files by a particular artist.</span></span> <span data-ttu-id="ad344-114">KeyID, tuttavia, è univoco per ogni file.</span><span class="sxs-lookup"><span data-stu-id="ad344-114">The KeyID, however, is unique for each file.</span></span>

<span data-ttu-id="ad344-115">Il valore di inizializzazione chiave deve rimanere un segreto condiviso solo tra l'autore del contenuto e il server di distribuzione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="ad344-115">The key seed must remain a secret that is shared only between the content creator and the license distributor.</span></span> <span data-ttu-id="ad344-116">Questo valore non è archiviato nell'intestazione DRM e non è né necessario né accessibile per le applicazioni DRM Player.</span><span class="sxs-lookup"><span data-stu-id="ad344-116">This value is not stored in the DRM header and it is neither needed by nor accessible to DRM player applications.</span></span>

<span data-ttu-id="ad344-117">Un nuovo valore di inizializzazione chiave può essere generato usando il metodo [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) o qualsiasi altro mezzo appropriato.</span><span class="sxs-lookup"><span data-stu-id="ad344-117">A new key seed can be generated using the [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) method or by any other suitable means.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad344-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad344-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad344-119">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="ad344-119">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




