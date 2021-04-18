---
description: Specifica l'archivio certificati utilizzato per firmare un documento.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: Struttura SIGNER_CERT_STORE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308109"
---
# <a name="signer_cert_store_info-structure"></a><span data-ttu-id="f3626-103">Struttura delle \_ \_ informazioni dell'archivio certificati del firmatario \_</span><span class="sxs-lookup"><span data-stu-id="f3626-103">SIGNER\_CERT\_STORE\_INFO structure</span></span>

<span data-ttu-id="f3626-104">La struttura delle **\_ \_ \_ informazioni dell'archivio certificati del firmatario** specifica l'archivio certificati utilizzato per firmare un documento.</span><span class="sxs-lookup"><span data-stu-id="f3626-104">The **SIGNER\_CERT\_STORE\_INFO** structure specifies the certificate store used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="f3626-105">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="f3626-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="f3626-106">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f3626-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f3626-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3626-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a><span data-ttu-id="f3626-108">Members</span><span class="sxs-lookup"><span data-stu-id="f3626-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3626-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="f3626-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="f3626-110">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="f3626-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="f3626-111">**pSigningCert**</span><span class="sxs-lookup"><span data-stu-id="f3626-111">**pSigningCert**</span></span>
</dt> <dd>

<span data-ttu-id="f3626-112">Puntatore a una struttura [**del \_ contesto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato per il certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="f3626-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f3626-113">**dwCertPolicy**</span><span class="sxs-lookup"><span data-stu-id="f3626-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="f3626-114">Specifica la modalità di aggiunta dei certificati alla firma.</span><span class="sxs-lookup"><span data-stu-id="f3626-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="f3626-115">Per trovare la catena di certificati, vengono controllati gli archivi MY, CA, ROOT e SPC, oltre all'archivio specificato dal membro **hCertStore** .</span><span class="sxs-lookup"><span data-stu-id="f3626-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="f3626-116">Il membro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3626-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="f3626-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f3626-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="f3626-118">Significato</span><span class="sxs-lookup"><span data-stu-id="f3626-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="f3626-119"><dt>**\_ Firmatario \_ \_ Catena di criteri CERT**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="f3626-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="f3626-120">Aggiungere solo i certificati nella catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="f3626-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="f3626-121"><dt>**\_ Firmatario \_Catena di criteri CERT \_ \_ senza \_ radice**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="f3626-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="f3626-122">Aggiungere solo i certificati nella catena di certificati, escluso il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="f3626-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="f3626-123"><dt>**\_ Firmatario \_ \_ Archivio criteri CERT**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f3626-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="f3626-124">Aggiungere tutti i certificati nell'archivio specificato dal membro **hCertStore** .</span><span class="sxs-lookup"><span data-stu-id="f3626-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="f3626-125">Questo flag può essere **una combinazione OR bit per** bit con uno degli altri valori possibili per questo membro.</span><span class="sxs-lookup"><span data-stu-id="f3626-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3626-126">**hCertStore**</span><span class="sxs-lookup"><span data-stu-id="f3626-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="f3626-127">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f3626-127">Optional.</span></span> <span data-ttu-id="f3626-128">Handle per un archivio certificati aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="f3626-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3626-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3626-129">Requirements</span></span>



| <span data-ttu-id="f3626-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3626-130">Requirement</span></span> | <span data-ttu-id="f3626-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f3626-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3626-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3626-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f3626-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f3626-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f3626-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3626-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f3626-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f3626-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3626-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3626-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3626-137">**certificato FIRMATARIo \_**</span><span class="sxs-lookup"><span data-stu-id="f3626-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 




