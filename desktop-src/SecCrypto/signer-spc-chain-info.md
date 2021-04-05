---
description: Specifica un certificato del server di pubblicazione software (SPC) e una catena di certificati utilizzati per firmare un documento.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: Struttura SIGNER_SPC_CHAIN_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131650"
---
# <a name="signer_spc_chain_info-structure"></a><span data-ttu-id="51d3f-103">Struttura delle \_ \_ informazioni sulla catena \_ di firma SPC</span><span class="sxs-lookup"><span data-stu-id="51d3f-103">SIGNER\_SPC\_CHAIN\_INFO structure</span></span>

<span data-ttu-id="51d3f-104">La struttura **\_ \_ \_ info Chain SPC del firmatario** specifica un [*certificato dell'editore del software*](../secgloss/s-gly.md) (SPC) e una catena di certificati usati per firmare un documento.</span><span class="sxs-lookup"><span data-stu-id="51d3f-104">The **SIGNER\_SPC\_CHAIN\_INFO** structure specifies a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) and certificate chain used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="51d3f-105">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="51d3f-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="51d3f-106">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="51d3f-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="51d3f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51d3f-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a><span data-ttu-id="51d3f-108">Members</span><span class="sxs-lookup"><span data-stu-id="51d3f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="51d3f-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="51d3f-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="51d3f-110">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="51d3f-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="51d3f-111">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="51d3f-111">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="51d3f-112">Nome del file SPC da usare per firmare un documento.</span><span class="sxs-lookup"><span data-stu-id="51d3f-112">The name of the SPC file to use to sign a document.</span></span>

</dd> <dt>

<span data-ttu-id="51d3f-113">**dwCertPolicy**</span><span class="sxs-lookup"><span data-stu-id="51d3f-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="51d3f-114">Specifica la modalità di aggiunta dei certificati alla firma.</span><span class="sxs-lookup"><span data-stu-id="51d3f-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="51d3f-115">Per trovare la catena di certificati, vengono controllati gli archivi MY, CA, ROOT e SPC, oltre all'archivio specificato dal membro **hCertStore** .</span><span class="sxs-lookup"><span data-stu-id="51d3f-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="51d3f-116">Il membro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="51d3f-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="51d3f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="51d3f-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="51d3f-118">Significato</span><span class="sxs-lookup"><span data-stu-id="51d3f-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="51d3f-119"><dt>**\_ Firmatario \_ \_ Catena di criteri CERT**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="51d3f-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="51d3f-120">Aggiungere solo i certificati nella catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="51d3f-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="51d3f-121"><dt>**\_ Firmatario \_Catena di criteri CERT \_ \_ senza \_ radice**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="51d3f-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="51d3f-122">Aggiungere solo i certificati nella catena di certificati, escluso il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="51d3f-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="51d3f-123"><dt>**\_ Firmatario \_ \_ Archivio criteri CERT**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="51d3f-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="51d3f-124">Aggiungere tutti i certificati nell'archivio specificato dal membro **hCertStore** .</span><span class="sxs-lookup"><span data-stu-id="51d3f-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="51d3f-125">Questo flag può essere **una combinazione OR bit per** bit con uno degli altri valori possibili per questo membro.</span><span class="sxs-lookup"><span data-stu-id="51d3f-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="51d3f-126">**hCertStore**</span><span class="sxs-lookup"><span data-stu-id="51d3f-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="51d3f-127">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="51d3f-127">Optional.</span></span> <span data-ttu-id="51d3f-128">Handle per un archivio certificati aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="51d3f-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51d3f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51d3f-129">Requirements</span></span>



| <span data-ttu-id="51d3f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="51d3f-130">Requirement</span></span> | <span data-ttu-id="51d3f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="51d3f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51d3f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51d3f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="51d3f-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="51d3f-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="51d3f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51d3f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="51d3f-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51d3f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51d3f-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51d3f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d3f-137">**certificato FIRMATARIo \_**</span><span class="sxs-lookup"><span data-stu-id="51d3f-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 
