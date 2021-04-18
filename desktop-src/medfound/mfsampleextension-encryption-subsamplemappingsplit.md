---
description: Imposta il mapping dei sottocampionamenti per l'esempio che indica i byte cancellati e crittografati nei dati di esempio.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: Attributo MFSampleExtension_Encryption_SubSampleMappingSplit (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309095"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a><span data-ttu-id="8bcfa-103">\_Attributo SubSampleMappingSplit di crittografia MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="8bcfa-103">MFSampleExtension\_Encryption\_SubSampleMappingSplit attribute</span></span>

<span data-ttu-id="8bcfa-104">Imposta il mapping dei sottocampionamenti per l'esempio che indica i byte cancellati e crittografati nei dati di esempio.</span><span class="sxs-lookup"><span data-stu-id="8bcfa-104">Sets the sub-sample mapping for the sample indicating the clear and encrypted bytes in the sample data.</span></span>

## <a name="data-type"></a><span data-ttu-id="8bcfa-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8bcfa-105">Data type</span></span>

<span data-ttu-id="8bcfa-106">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="8bcfa-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="8bcfa-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="8bcfa-107">Remarks</span></span>

<span data-ttu-id="8bcfa-108">Il **BLOB** deve contenere una matrice di intervalli di byte come DWORD, dove ogni due DWORD crea un set.</span><span class="sxs-lookup"><span data-stu-id="8bcfa-108">The **BLOB** should contain an array of byte ranges as DWORDs where every two DWORDs makes a set.</span></span> <span data-ttu-id="8bcfa-109">Il primo valore DWORD in ogni set è il numero di byte cancellati e il secondo valore DWORD del set è il numero di byte crittografati.</span><span class="sxs-lookup"><span data-stu-id="8bcfa-109">The first DWORD in each set is the number of clear bytes and the second DWORD of the set is the number of encrypted bytes.</span></span> <span data-ttu-id="8bcfa-110">Si noti che una coppia di zeri non è un set valido (il valore può essere 0, ma non entrambi).</span><span class="sxs-lookup"><span data-stu-id="8bcfa-110">Note that a pair of 0s is not a valid set (either value can be 0, but not both).</span></span> <span data-ttu-id="8bcfa-111">La matrice di intervalli di byte indica gli intervalli da decrittografare, inclusa la possibilità che l'intero campione non venga decrittografato.</span><span class="sxs-lookup"><span data-stu-id="8bcfa-111">The array of byte ranges indicate which ranges to decrypt, including the possibility that the entire sample should not be decrypted.</span></span> <span data-ttu-id="8bcfa-112">Si consiglia di non impostare questa opzione su Clear Samples, anche se è possibile ottenere lo stesso risultato impostando i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="8bcfa-112">It is recommended that this should not be set on clear samples, though it is possible to achieve the same result by setting it with the appropriate values.</span></span>

## <a name="examples"></a><span data-ttu-id="8bcfa-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="8bcfa-113">Examples</span></span>

<span data-ttu-id="8bcfa-114">Nell'esempio seguente viene illustrato come impostare \_ SubSampleMappingSplit Encryption MFSampleExtension \_ .</span><span class="sxs-lookup"><span data-stu-id="8bcfa-114">The following example shows how to set MFSampleExtension\_Encryption\_SubSampleMappingSplit.</span></span>


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a><span data-ttu-id="8bcfa-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bcfa-115">Requirements</span></span>



| <span data-ttu-id="8bcfa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bcfa-116">Requirement</span></span> | <span data-ttu-id="8bcfa-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8bcfa-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8bcfa-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bcfa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8bcfa-119">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8bcfa-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="8bcfa-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bcfa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8bcfa-121">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8bcfa-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8bcfa-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bcfa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bcfa-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bcfa-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bcfa-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bcfa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bcfa-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8bcfa-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8bcfa-126">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="8bcfa-126">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="8bcfa-127">\_KeyId contenuto \_ MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="8bcfa-127">MFSampleExtension\_Content\_KeyID</span></span>](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




