---
description: Specifica le informazioni sul provider del servizio di crittografia (CSP) e sulla chiave privata utilizzate per creare una firma digitale.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: Struttura SIGNER_PROVIDER_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316134"
---
# <a name="signer_provider_info-structure"></a><span data-ttu-id="0a0fb-103">Struttura di \_ informazioni sul provider del firmatario \_</span><span class="sxs-lookup"><span data-stu-id="0a0fb-103">SIGNER\_PROVIDER\_INFO structure</span></span>

<span data-ttu-id="0a0fb-104">La struttura delle **\_ \_ informazioni del provider del firmatario** specifica le informazioni sul [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e sulla chiave privata utilizzate per creare una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-104">The **SIGNER\_PROVIDER\_INFO** structure specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="0a0fb-105">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="0a0fb-106">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0a0fb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a0fb-107">Syntax</span></span>


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a><span data-ttu-id="0a0fb-108">Members</span><span class="sxs-lookup"><span data-stu-id="0a0fb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a0fb-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="0a0fb-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="0a0fb-110">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="0a0fb-111">**pwszProviderName**</span><span class="sxs-lookup"><span data-stu-id="0a0fb-111">**pwszProviderName**</span></span>
</dt> <dd>

<span data-ttu-id="0a0fb-112">Nome del CSP utilizzato per creare la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-112">The name of the CSP used to create the digital signature.</span></span> <span data-ttu-id="0a0fb-113">Se il valore di questo membro è **null**, viene utilizzato il provider predefinito.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-113">If the value of this member is **NULL**, the default provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="0a0fb-114">**dwProviderType**</span><span class="sxs-lookup"><span data-stu-id="0a0fb-114">**dwProviderType**</span></span>
</dt> <dd>

<span data-ttu-id="0a0fb-115">Tipo di CSP specificato dal membro **pwszProviderName** .</span><span class="sxs-lookup"><span data-stu-id="0a0fb-115">The type of the CSP specified by the **pwszProviderName** member.</span></span>

</dd> <dt>

<span data-ttu-id="0a0fb-116">**dwKeySpec**</span><span class="sxs-lookup"><span data-stu-id="0a0fb-116">**dwKeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="0a0fb-117">Specifica delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-117">The key specification.</span></span> <span data-ttu-id="0a0fb-118">Se questo membro è impostato su zero, viene utilizzata la specifica della chiave nel membro **pwszPvkFileName** o **pwszKeyContainer** .</span><span class="sxs-lookup"><span data-stu-id="0a0fb-118">If this member is set to zero, the key specification in the **pwszPvkFileName** or **pwszKeyContainer** member is used.</span></span> <span data-ttu-id="0a0fb-119">Se è presente più di una specifica chiave nel membro **pwszKeyContainer** , viene usata **la \_ firma** .</span><span class="sxs-lookup"><span data-stu-id="0a0fb-119">If there is more than one key specification in the **pwszKeyContainer** member, **AT\_SIGNATURE** is used.</span></span> <span data-ttu-id="0a0fb-120">In caso di esito negativo, viene utilizzato il **\_ cambio di** stato.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-120">If it fails, **AT\_KEYEXCHANGE** is used.</span></span>

</dd> <dt>

<span data-ttu-id="0a0fb-121">**dwPvkChoice**</span><span class="sxs-lookup"><span data-stu-id="0a0fb-121">**dwPvkChoice**</span></span>
</dt> <dd>

<span data-ttu-id="0a0fb-122">Specifica il tipo di informazioni sulla chiave privata.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-122">Specifies the type of private key information.</span></span> <span data-ttu-id="0a0fb-123">Il membro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-123">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="0a0fb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0a0fb-124">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="0a0fb-125">Significato</span><span class="sxs-lookup"><span data-stu-id="0a0fb-125">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <span data-ttu-id="0a0fb-126"><dt>**PVK \_ Digitare \_ il \_ nome file**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0a0fb-126"><dt>**PVK\_TYPE\_FILE\_NAME**</dt> <dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="0a0fb-127">Le informazioni sulla chiave privata sono un nome file.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-127">The private key information is a file name.</span></span><br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <span data-ttu-id="0a0fb-128"><dt>**PVK \_ TIPO di \_ contenitore di contenitori**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0a0fb-128"><dt>**PVK\_TYPE\_KEYCONTAINER**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0a0fb-129">Le informazioni sulla chiave privata sono un contenitore di chiavi.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-129">The private key information is a key container.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0a0fb-130">**pwszPvkFileName**</span><span class="sxs-lookup"><span data-stu-id="0a0fb-130">**pwszPvkFileName**</span></span>
</dt> <dd>

<span data-ttu-id="0a0fb-131">Nome del file che contiene le informazioni sulla chiave privata.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-131">The name of the file that contains the private key information.</span></span>

</dd> <dt>

<span data-ttu-id="0a0fb-132">**pwszKeyContainer**</span><span class="sxs-lookup"><span data-stu-id="0a0fb-132">**pwszKeyContainer**</span></span>
</dt> <dd>

<span data-ttu-id="0a0fb-133">Nome del contenitore di chiavi che contiene le informazioni sulla chiave privata.</span><span class="sxs-lookup"><span data-stu-id="0a0fb-133">The name of the key container that contains the private key information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a0fb-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a0fb-134">Requirements</span></span>



| <span data-ttu-id="0a0fb-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a0fb-135">Requirement</span></span> | <span data-ttu-id="0a0fb-136">Valore</span><span class="sxs-lookup"><span data-stu-id="0a0fb-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a0fb-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a0fb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0a0fb-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0a0fb-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0a0fb-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a0fb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0a0fb-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a0fb-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a0fb-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a0fb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a0fb-142">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="0a0fb-142">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="0a0fb-143">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="0a0fb-143">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
