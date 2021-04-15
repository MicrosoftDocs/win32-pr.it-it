---
description: Molte delle funzioni richiedono tipi di codifica dei messaggi o certificati.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Tipi di codifica di messaggi e certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484693"
---
# <a name="certificate-and-message-encoding-types"></a><span data-ttu-id="0d4eb-103">Tipi di codifica di messaggi e certificati</span><span class="sxs-lookup"><span data-stu-id="0d4eb-103">Certificate and Message Encoding Types</span></span>

<span data-ttu-id="0d4eb-104">Molte delle funzioni richiedono [*tipi di codifica dei messaggi*](../secgloss/m-gly.md)o certificati.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-104">Many of the functions require certificate or [*message encoding types*](../secgloss/m-gly.md).</span></span> <span data-ttu-id="0d4eb-105">Questo tipo di codifica è un **valore DWORD**, che può contenere sia il certificato che i tipi di codifica dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-105">This encoding type is a **DWORD**, possibly containing both the certificate and message encoding types.</span></span> <span data-ttu-id="0d4eb-106">Il tipo di codifica del certificato viene archiviato nella parola di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-106">The certificate encoding type is stored in the low-order word.</span></span> <span data-ttu-id="0d4eb-107">Il tipo di codifica dei messaggi viene archiviato nella parola più avanzata.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-107">The message encoding type is stored in the high-order word.</span></span> <span data-ttu-id="0d4eb-108">Alcune funzioni o campi della struttura richiedono solo uno dei tipi di codifica, ma è sempre accettabile specificare entrambi i tipi di codifica.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-108">Some functions or structure fields require only one of the encoding types, but it is always acceptable to specify both encoding types.</span></span> <span data-ttu-id="0d4eb-109">Per un esempio di specifica di entrambi i tipi di codifica, vedere [ \# include e \# definisce](-includes-and--defines.md).</span><span class="sxs-lookup"><span data-stu-id="0d4eb-109">For an example specifying both encoding types, see [\#includes and \#defines](-includes-and--defines.md).</span></span>

<span data-ttu-id="0d4eb-110">La convenzione di denominazione dei parametri riportata di seguito viene usata per indicare i tipi di codifica richiesti.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-110">The following parameter naming convention is used to indicate the encoding types required.</span></span>



| <span data-ttu-id="0d4eb-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0d4eb-111">Name</span></span>                       | <span data-ttu-id="0d4eb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d4eb-112">Comments</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4eb-113">*dwMsgAndCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="0d4eb-113">*dwMsgAndCertEncodingType*</span></span> | <span data-ttu-id="0d4eb-114">Sono necessari entrambi i tipi di codifica.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-114">Both encoding types are required.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0d4eb-115">*dwMsgEncodingType*</span><span class="sxs-lookup"><span data-stu-id="0d4eb-115">*dwMsgEncodingType*</span></span>        | <span data-ttu-id="0d4eb-116">È necessario solo il tipo di codifica dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-116">Only the message encoding type is required.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0d4eb-117">*dwCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="0d4eb-117">*dwCertEncodingType*</span></span>       | <span data-ttu-id="0d4eb-118">È necessario solo il tipo di codifica del certificato.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-118">Only the certificate encoding type is required.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="0d4eb-119">*dwEncodingType*</span><span class="sxs-lookup"><span data-stu-id="0d4eb-119">*dwEncodingType*</span></span>           | <span data-ttu-id="0d4eb-120">È necessario specificare un tipo di codifica del messaggio o del certificato.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-120">Either a message or certificate encoding type is required.</span></span> <span data-ttu-id="0d4eb-121">Se la parola più bassa che contiene il tipo di codifica del certificato è diversa da zero, viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-121">If the low-order word containing the certificate encoding type is nonzero, then it is used.</span></span> <span data-ttu-id="0d4eb-122">In caso contrario, viene utilizzata la parola più ordinata contenente il tipo di codifica dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-122">Otherwise, the high-order word containing the message encoding type is used.</span></span> <span data-ttu-id="0d4eb-123">Se vengono specificati entrambi, viene utilizzato il tipo di codifica del certificato nella parola di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-123">If both are specified, the certificate encoding type in the low-order word is used.</span></span> |



 

<span data-ttu-id="0d4eb-124">I tipi di codifica attualmente definiti sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0d4eb-124">Currently defined encoding types are shown in the following table.</span></span>



| <span data-ttu-id="0d4eb-125">Tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="0d4eb-125">Encoding type</span></span>          | <span data-ttu-id="0d4eb-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0d4eb-126">Value</span></span>      |
|------------------------|------------|
| <span data-ttu-id="0d4eb-127">\_codifica ASN di Crypt \_</span><span class="sxs-lookup"><span data-stu-id="0d4eb-127">CRYPT\_ASN\_ENCODING</span></span>   | <span data-ttu-id="0d4eb-128">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0d4eb-128">0x00000001</span></span> |
| <span data-ttu-id="0d4eb-129">\_Codifica ASN \_ X509</span><span class="sxs-lookup"><span data-stu-id="0d4eb-129">X509\_ASN\_ENCODING</span></span>    | <span data-ttu-id="0d4eb-130">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0d4eb-130">0x00000001</span></span> |
| <span data-ttu-id="0d4eb-131">\_ \_ Codifica ASN 7 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="0d4eb-131">PKCS\_7\_ASN\_ENCODING</span></span> | <span data-ttu-id="0d4eb-132">0x00010000</span><span class="sxs-lookup"><span data-stu-id="0d4eb-132">0x00010000</span></span> |



 

 

 
