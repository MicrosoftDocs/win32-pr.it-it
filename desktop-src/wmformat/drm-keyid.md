---
title: DRM_KeyID
description: L' \_ attributo keyId di DRM contiene l'identificatore di chiave.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID formato Windows Media
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046340"
---
# <a name="drm_keyid"></a><span data-ttu-id="dd497-104">\_KEYID DRM</span><span class="sxs-lookup"><span data-stu-id="dd497-104">DRM\_KeyID</span></span>

<span data-ttu-id="dd497-105">L' **attributo \_ keyId di DRM** contiene l'identificatore di chiave.</span><span class="sxs-lookup"><span data-stu-id="dd497-105">The **DRM\_KeyID** attribute contains the key identifier.</span></span>

## <a name="global-constant"></a><span data-ttu-id="dd497-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="dd497-106">Global Constant</span></span>

<span data-ttu-id="dd497-107">g \_ wszWMDRM \_ keyId</span><span class="sxs-lookup"><span data-stu-id="dd497-107">g\_wszWMDRM\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="dd497-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="dd497-108">Data Type</span></span>

<span data-ttu-id="dd497-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="dd497-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="dd497-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd497-110">Remarks</span></span>

<span data-ttu-id="dd497-111">Questo attributo è presente solo per il contenuto DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="dd497-111">This attribute is present for DRM Version 7 content only.</span></span> <span data-ttu-id="dd497-112">Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="dd497-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="dd497-113">Lo stesso attributo file può essere recuperato usando [**DRM \_ DRMHeader \_ keyId**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="dd497-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

<span data-ttu-id="dd497-114">L'ID chiave viene usato in combinazione con il valore di inizializzazione chiave per creare la chiave simmetrica usata per crittografare e decrittografare il file.</span><span class="sxs-lookup"><span data-stu-id="dd497-114">The key ID is used in conjunction with the key seed to create the content key which is used to encrypt and decrypt the file.</span></span> <span data-ttu-id="dd497-115">L'applicazione Writer usa l'ID chiave per crittografare il file e quindi archivia l'ID chiave nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="dd497-115">The writer application uses the key ID to encrypt the file and then it stores the key ID in the file header.</span></span> <span data-ttu-id="dd497-116">Quando un'applicazione lettore richiede una licenza per un file, il componente DRM invia l'ID chiave (insieme al resto dell'intestazione DRM) al server licenze.</span><span class="sxs-lookup"><span data-stu-id="dd497-116">When a player application requests a license for a file, the DRM component sends the key ID (along with the rest of the DRM header) to the license server.</span></span> <span data-ttu-id="dd497-117">Il server licenze, che ha il valore di inizializzazione chiave privata, lo usa e l'ID chiave per creare una chiave per il file, che viene quindi inserita in una licenza insieme ai vari diritti che verranno applicati al file.</span><span class="sxs-lookup"><span data-stu-id="dd497-117">The license server, which has the secret key seed, uses it and the key ID to create a key for the file, which it then inserts into a license along with the various rights that will be applied to the file.</span></span>

<span data-ttu-id="dd497-118">In genere, un valore di inizializzazione chiave viene utilizzato con molti ID chiave.</span><span class="sxs-lookup"><span data-stu-id="dd497-118">Typically, one key seed is used with many key IDs.</span></span> <span data-ttu-id="dd497-119">Il valore di inizializzazione chiave è un segreto condiviso solo dall'autore del contenuto e dal server di distribuzione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="dd497-119">The key seed is a secret shared only by the content creator and the license distributor.</span></span> <span data-ttu-id="dd497-120">L'ID chiave viene usato dalle applicazioni client DRM e viene archiviato nell'intestazione DRM in chiaro.</span><span class="sxs-lookup"><span data-stu-id="dd497-120">The key ID is used by DRM client applications and is stored in the DRM header in the clear.</span></span>

<span data-ttu-id="dd497-121">Questo attributo è identico a quello di [**DRM \_ DRMHeader \_ keyId**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="dd497-121">This attribute is the same as [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="dd497-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd497-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd497-123">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="dd497-123">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




