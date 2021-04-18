---
description: Il campo lunghezza in una tripletta TLV identifica il numero di byte codificati nel campo valore.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Byte di lunghezza e valore codificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310756"
---
# <a name="encoded-length-and-value-bytes"></a><span data-ttu-id="1f6a4-103">Byte di lunghezza e valore codificati</span><span class="sxs-lookup"><span data-stu-id="1f6a4-103">Encoded Length and Value Bytes</span></span>

<span data-ttu-id="1f6a4-104">Il campo *lunghezza* in una tripletta TLV identifica il numero di byte codificati nel campo *valore* .</span><span class="sxs-lookup"><span data-stu-id="1f6a4-104">The *Length* field in a TLV triplet identifies the number of bytes encoded in the *Value* field.</span></span> <span data-ttu-id="1f6a4-105">Il campo *valore* contiene il contenuto inviato tra computer.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-105">The *Value* field contains the content being sent between computers.</span></span> <span data-ttu-id="1f6a4-106">Se il campo del *valore* contiene meno di 128 byte, il campo *lunghezza* richiede un solo byte.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-106">If the *Value* field contains fewer than 128 bytes, the *Length* field requires only one byte.</span></span> <span data-ttu-id="1f6a4-107">Il bit 7 del campo *length* è zero (0) e i bit rimanenti identificano il numero di byte del contenuto inviato.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-107">Bit 7 of the *Length* field is zero (0) and the remaining bits identify the number of bytes of content being sent.</span></span> <span data-ttu-id="1f6a4-108">Se il campo del *valore* contiene più di 127 byte, il bit 7 del campo *length* è uno (1) e i bit rimanenti identificano il numero di byte necessari per contenere la lunghezza.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-108">If the *Value* field contains more than 127 bytes, bit 7 of the *Length* field is one (1) and the remaining bits identify the number of bytes needed to contain the length.</span></span> <span data-ttu-id="1f6a4-109">Nella figura seguente sono illustrati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="1f6a4-109">Examples are shown in the following illustration.</span></span>

![byte Lunghezza der TLV](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a><span data-ttu-id="1f6a4-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f6a4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f6a4-112">Sintassi di trasferimento DER</span><span class="sxs-lookup"><span data-stu-id="1f6a4-112">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
</dt> <dt>

[<span data-ttu-id="1f6a4-113">Byte tag codificati</span><span class="sxs-lookup"><span data-stu-id="1f6a4-113">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



