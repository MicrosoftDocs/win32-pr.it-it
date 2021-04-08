---
description: Specifica la dimensione del blocco di byte cancellata (non crittografata) per la crittografia dei modelli basata sul campione.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: Attributo MFSampleExtension_Encryption_SkipByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18003c03df7e65314846d34cb1d1093f5b2507a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880614"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a><span data-ttu-id="b8131-103">\_Attributo SkipByteBlock di crittografia MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="b8131-103">MFSampleExtension\_Encryption\_SkipByteBlock attribute</span></span>

<span data-ttu-id="b8131-104">Specifica la dimensione del blocco di byte cancellata (non crittografata) per la crittografia dei modelli basata sul campione.</span><span class="sxs-lookup"><span data-stu-id="b8131-104">Specifies the clear (non-encrypted) byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="b8131-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b8131-105">Data type</span></span>

<span data-ttu-id="b8131-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b8131-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b8131-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8131-107">Remarks</span></span>

<span data-ttu-id="b8131-108">Il numero di byte crittografati nel blocco di mapping di sottocampionamento viene specificato nell'attributo [ \_ \_ CryptByteBlock Encryption MFSampleExtension](mfsampleextension-encryption-cryptbyteblock.md) .</span><span class="sxs-lookup"><span data-stu-id="b8131-108">The number of encrypted bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) attribute.</span></span> <span data-ttu-id="b8131-109">Se uno di questi attributi non è presente o ha un valore pari a 0, significa che i dati di esempio non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="b8131-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="b8131-110">Uno di questi valori deve essere diverso da zero, valori positivi oppure entrambi devono avere un valore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="b8131-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="b8131-111">Nei casi in cui l'origine è basata su MP4, il valore viene impostato in base ai valori del \_ blocco default Skip \_ byte nella \_ casella Track Encryption ("Tenc") nell'intestazione MP4.</span><span class="sxs-lookup"><span data-stu-id="b8131-111">In cases where the Source is MP4-based, the value is set based off the values of default\_skip\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="b8131-112">Per altre informazioni, vedere [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span><span class="sxs-lookup"><span data-stu-id="b8131-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8131-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8131-113">Requirements</span></span>



| <span data-ttu-id="b8131-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8131-114">Requirement</span></span> | <span data-ttu-id="b8131-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b8131-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8131-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8131-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8131-117">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8131-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b8131-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8131-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8131-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b8131-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b8131-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8131-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8131-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8131-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




