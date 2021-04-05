---
description: Specifica la dimensione del blocco di byte crittografato per la crittografia del modello basata su campione.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: Attributo MFSampleExtension_Encryption_CryptByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049802"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a><span data-ttu-id="73193-103">\_Attributo CryptByteBlock di crittografia MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="73193-103">MFSampleExtension\_Encryption\_CryptByteBlock attribute</span></span>

<span data-ttu-id="73193-104">Specifica la dimensione del blocco di byte crittografato per la crittografia del modello basata su campione.</span><span class="sxs-lookup"><span data-stu-id="73193-104">Specifies the encrypted byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="73193-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="73193-105">Data type</span></span>

<span data-ttu-id="73193-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="73193-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="73193-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="73193-107">Remarks</span></span>

<span data-ttu-id="73193-108">Il numero di byte cancellati (non crittografati) nel blocco di mapping di sottocampionamento viene specificato nell'attributo [ \_ \_ SkipByteBlock Encryption MFSampleExtension](mfsampleextension-encryption-skipbyteblock.md) .</span><span class="sxs-lookup"><span data-stu-id="73193-108">The number of clear (non-encrypted) bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) attribute.</span></span> <span data-ttu-id="73193-109">Se uno di questi attributi non è presente o ha un valore pari a 0, significa che i dati di esempio non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="73193-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="73193-110">Uno di questi valori deve essere diverso da zero, valori positivi oppure entrambi devono avere un valore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="73193-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="73193-111">Nei casi in cui l'origine è basata su MP4, il valore viene impostato in base ai valori del \_ blocco default Crypt \_ byte nella \_ casella Track Encryption (' Tenc ') nell'intestazione MP4.</span><span class="sxs-lookup"><span data-stu-id="73193-111">In cases where the Source is MP4-based, the value is set based off the values of default\_crypt\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="73193-112">Per altre informazioni, vedere [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span><span class="sxs-lookup"><span data-stu-id="73193-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73193-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73193-113">Requirements</span></span>



| <span data-ttu-id="73193-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="73193-114">Requirement</span></span> | <span data-ttu-id="73193-115">Valore</span><span class="sxs-lookup"><span data-stu-id="73193-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73193-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73193-116">Minimum supported client</span></span><br/> | <span data-ttu-id="73193-117">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="73193-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="73193-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73193-118">Minimum supported server</span></span><br/> | <span data-ttu-id="73193-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="73193-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="73193-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73193-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="73193-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73193-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




