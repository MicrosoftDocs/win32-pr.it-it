---
title: DRM_LASignaturePrivKey
description: La \_ Proprietà DRM LASignaturePrivKey contiene la chiave privata usata per crittografare l'intestazione DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398620"
---
# <a name="drm_lasignatureprivkey"></a><span data-ttu-id="e9802-104">\_LASIGNATUREPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="e9802-104">DRM\_LASignaturePrivKey</span></span>

<span data-ttu-id="e9802-105">La proprietà **DRM \_ LASignaturePrivKey** contiene la chiave privata usata per crittografare l'intestazione DRM.</span><span class="sxs-lookup"><span data-stu-id="e9802-105">The **DRM\_LASignaturePrivKey** property contains the private key that is used to encrypt the DRM header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="e9802-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="e9802-106">Global Constant</span></span>

<span data-ttu-id="e9802-107">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="e9802-107">g\_wszWMDRM\_LASignaturePrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="e9802-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e9802-108">Data Type</span></span>

<span data-ttu-id="e9802-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e9802-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="e9802-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9802-110">Remarks</span></span>

<span data-ttu-id="e9802-111">Questa proprietà può essere generata usando il metodo [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) .</span><span class="sxs-lookup"><span data-stu-id="e9802-111">This property can be generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) method.</span></span> <span data-ttu-id="e9802-112">Questa proprietà deve rimanere un segreto noto solo dall'autore del contenuto.</span><span class="sxs-lookup"><span data-stu-id="e9802-112">This property should remain a secret known only by the content creator.</span></span> <span data-ttu-id="e9802-113">Questa proprietà può essere impostata con il metodo [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) .</span><span class="sxs-lookup"><span data-stu-id="e9802-113">This property can be set with the [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) method.</span></span> <span data-ttu-id="e9802-114">Non è accessibile all'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="e9802-114">It is not accessible to the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9802-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9802-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9802-116">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="e9802-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




