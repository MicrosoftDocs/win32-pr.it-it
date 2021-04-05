---
title: DRM_HeaderSignPrivKey
description: La \_ Proprietà DRM HeaderSignPrivKey contiene la chiave privata usata per firmare l'intestazione ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey formato Windows Media
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723487"
---
# <a name="drm_headersignprivkey"></a><span data-ttu-id="720a1-104">\_HEADERSIGNPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="720a1-104">DRM\_HeaderSignPrivKey</span></span>

<span data-ttu-id="720a1-105">La proprietà **DRM \_ HeaderSignPrivKey** contiene la chiave privata usata per firmare l'intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="720a1-105">The **DRM\_HeaderSignPrivKey** property contains the private key used to sign the ASF header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="720a1-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="720a1-106">Global Constant</span></span>

<span data-ttu-id="720a1-107">g \_ wszWMDRM \_ HeaderSignPrivKey</span><span class="sxs-lookup"><span data-stu-id="720a1-107">g\_wszWMDRM\_HeaderSignPrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="720a1-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="720a1-108">Data Type</span></span>

<span data-ttu-id="720a1-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="720a1-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="720a1-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="720a1-110">Remarks</span></span>

<span data-ttu-id="720a1-111">Questa proprietà viene generata utilizzando [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span><span class="sxs-lookup"><span data-stu-id="720a1-111">This property is generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span></span> <span data-ttu-id="720a1-112">Mantieni questo segreto chiave e Condividi la chiave pubblica solo con il servizio licenze.</span><span class="sxs-lookup"><span data-stu-id="720a1-112">Keep this key secret and share the public key only with the license service.</span></span> <span data-ttu-id="720a1-113">Dopo aver impostato questa chiave, il componente DRM lo utilizzerà per firmare l'intestazione del file ASF (non l'intestazione DRM firmata con i valori dell'oggetto firma digitale, ad esempio DRM \_ LASignaturePrivKey).</span><span class="sxs-lookup"><span data-stu-id="720a1-113">After you set this key, the DRM component will use it to sign the ASF file header (not the DRM header which is signed with the digital signature object values such as DRM\_LASignaturePrivKey).</span></span> <span data-ttu-id="720a1-114">Ovviamente, **DRM \_ HeaderSignPrivKey** non è incluso nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="720a1-114">Obviously, **DRM\_HeaderSignPrivKey** is not included in the file headert.</span></span>

<span data-ttu-id="720a1-115">Questa proprietà non è accessibile dall'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="720a1-115">This property is not accessible from the reader object.</span></span> <span data-ttu-id="720a1-116">Può essere impostata dall'oggetto writer usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="720a1-116">It can be set from the writer object using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

## <a name="see-also"></a><span data-ttu-id="720a1-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="720a1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="720a1-118">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="720a1-118">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




