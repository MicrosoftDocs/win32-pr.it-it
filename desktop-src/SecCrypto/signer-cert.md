---
description: Specifica un certificato utilizzato per firmare un documento. Il certificato può essere archiviato in un file di certificato dell'editore del software (SPC) o in un archivio certificati.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: Struttura SIGNER_CERT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233123"
---
# <a name="signer_cert-structure"></a><span data-ttu-id="0184f-104">Struttura del certificato del FIRMATARIo \_</span><span class="sxs-lookup"><span data-stu-id="0184f-104">SIGNER\_CERT structure</span></span>

<span data-ttu-id="0184f-105">La struttura del certificato del **firmatario \_** specifica un [*certificato*](../secgloss/c-gly.md) utilizzato per firmare un documento.</span><span class="sxs-lookup"><span data-stu-id="0184f-105">The **SIGNER\_CERT** structure specifies a [*certificate*](../secgloss/c-gly.md) used to sign a document.</span></span> <span data-ttu-id="0184f-106">Il certificato può essere archiviato in un file di [*certificato dell'editore del software*](../secgloss/s-gly.md) (SPC) o in un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0184f-106">The certificate can be stored in a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) file or in a [*certificate store*](../secgloss/c-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="0184f-107">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="0184f-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="0184f-108">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="0184f-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0184f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0184f-109">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a><span data-ttu-id="0184f-110">Members</span><span class="sxs-lookup"><span data-stu-id="0184f-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="0184f-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="0184f-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="0184f-112">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="0184f-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="0184f-113">**dwCertChoice**</span><span class="sxs-lookup"><span data-stu-id="0184f-113">**dwCertChoice**</span></span>
</dt> <dd>

<span data-ttu-id="0184f-114">Specifica la modalità di archiviazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="0184f-114">Specifies how the certificate is stored.</span></span> <span data-ttu-id="0184f-115">Il membro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0184f-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="0184f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0184f-116">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="0184f-117">Significato</span><span class="sxs-lookup"><span data-stu-id="0184f-117">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <span data-ttu-id="0184f-118"><dt>**\_ Firmatario \_ \_ File di certificato SPC**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0184f-118"><dt>**SIGNER\_CERT\_SPC\_FILE**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="0184f-119">Il certificato viene archiviato in un file SPC.</span><span class="sxs-lookup"><span data-stu-id="0184f-119">The certificate is stored in an SPC file.</span></span> <span data-ttu-id="0184f-120">Il membro **pwszSpcFile** contiene il percorso e il nome file del file SPC.</span><span class="sxs-lookup"><span data-stu-id="0184f-120">The **pwszSpcFile** member contains the path and file name of the SPC file.</span></span><br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <span data-ttu-id="0184f-121"><dt>**\_ Firmatario \_Archivio certificati**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0184f-121"><dt>**SIGNER\_CERT\_STORE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="0184f-122">Il certificato viene archiviato in un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="0184f-122">The certificate is stored in a certificate store.</span></span> <span data-ttu-id="0184f-123">Il membro **pCertStoreInfo** contiene un puntatore a una struttura di informazioni dell'archivio certificati del firmatario che specifica l'archivio certificati in cui è archiviato il certificato. [**\_ \_ \_**](signer-cert-store-info.md)</span><span class="sxs-lookup"><span data-stu-id="0184f-123">The **pCertStoreInfo** member contains a pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span><br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <span data-ttu-id="0184f-124"><dt>**\_ Firmatario \_ \_ Catena di certificati SPC**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0184f-124"><dt>**SIGNER\_CERT\_SPC\_CHAIN**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="0184f-125">Il certificato viene archiviato in un file SPC ed è associato a una catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="0184f-125">The certificate is stored in an SPC file and is associated with a certificate chain.</span></span> <span data-ttu-id="0184f-126">Il membro **pSpcChainInfo** contiene un puntatore a una struttura di informazioni della [**catena di SPC del firmatario \_ \_ \_**](signer-spc-chain-info.md) che contiene le informazioni sulla catena per il certificato.</span><span class="sxs-lookup"><span data-stu-id="0184f-126">The **pSpcChainInfo** member contains a pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0184f-127">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="0184f-127">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="0184f-128">Puntatore a una stringa Unicode con terminazione null che contiene il percorso e il nome file del file SPC in cui è archiviato il certificato.</span><span class="sxs-lookup"><span data-stu-id="0184f-128">A pointer to a null-terminated Unicode string that contains the path and file name of the SPC file in which the certificate is stored.</span></span> <span data-ttu-id="0184f-129">Questo membro viene utilizzato solo se il membro **dwCertChoice** contiene il **\_ \_ \_ file SPC del certificato del firmatario**.</span><span class="sxs-lookup"><span data-stu-id="0184f-129">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_FILE**.</span></span>

</dd> <dt>

<span data-ttu-id="0184f-130">**pCertStoreInfo**</span><span class="sxs-lookup"><span data-stu-id="0184f-130">**pCertStoreInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0184f-131">Puntatore a una struttura di [**\_ \_ \_ informazioni dell'archivio certificati del firmatario**](signer-cert-store-info.md) che specifica l'archivio certificati in cui è archiviato il certificato.</span><span class="sxs-lookup"><span data-stu-id="0184f-131">A pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span> <span data-ttu-id="0184f-132">Questo membro viene usato solo se il membro **dwCertChoice** contiene l' **\_ \_ Archivio del certificato del firmatario**.</span><span class="sxs-lookup"><span data-stu-id="0184f-132">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_STORE**.</span></span>

</dd> <dt>

<span data-ttu-id="0184f-133">**pSpcChainInfo**</span><span class="sxs-lookup"><span data-stu-id="0184f-133">**pSpcChainInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0184f-134">Puntatore a una struttura di [**\_ \_ \_ informazioni della catena SPC del firmatario**](signer-spc-chain-info.md) che contiene le informazioni sulla catena per il certificato.</span><span class="sxs-lookup"><span data-stu-id="0184f-134">A pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span> <span data-ttu-id="0184f-135">Questo membro viene usato solo se il membro **dwCertChoice** contiene una **\_ \_ \_ catena di certificati SPC del firmatario**.</span><span class="sxs-lookup"><span data-stu-id="0184f-135">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_CHAIN**.</span></span>

</dd> <dt>

<span data-ttu-id="0184f-136">**HWND**</span><span class="sxs-lookup"><span data-stu-id="0184f-136">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="0184f-137">Handle della finestra da utilizzare come proprietario di tutte le finestre di dialogo visualizzate.</span><span class="sxs-lookup"><span data-stu-id="0184f-137">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="0184f-138">Questo membro non è attualmente in uso e viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0184f-138">This member is not currently used and is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0184f-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0184f-139">Requirements</span></span>



| <span data-ttu-id="0184f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0184f-140">Requirement</span></span> | <span data-ttu-id="0184f-141">Valore</span><span class="sxs-lookup"><span data-stu-id="0184f-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0184f-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0184f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0184f-143">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0184f-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0184f-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0184f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0184f-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0184f-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0184f-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0184f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0184f-147">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="0184f-147">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="0184f-148">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="0184f-148">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
