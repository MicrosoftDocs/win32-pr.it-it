---
title: Struttura LSLicense
description: Contiene informazioni su una licenza di Servizi Desktop remoto specifica.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della struttura LSLicense
- Servizi Desktop remoto puntatore alla struttura LPLSLicense
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476439"
---
# <a name="lslicense-structure"></a><span data-ttu-id="fa164-105">Struttura LSLicense</span><span class="sxs-lookup"><span data-stu-id="fa164-105">LSLicense structure</span></span>

<span data-ttu-id="fa164-106">Contiene informazioni su una licenza di Servizi Desktop remoto specifica.</span><span class="sxs-lookup"><span data-stu-id="fa164-106">Contains information about a specific Remote Desktop Services license.</span></span>

> [!Note]  
> <span data-ttu-id="fa164-107">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="fa164-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="fa164-108">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="fa164-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fa164-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa164-109">Syntax</span></span>


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a><span data-ttu-id="fa164-110">Members</span><span class="sxs-lookup"><span data-stu-id="fa164-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa164-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="fa164-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-112">Versione della licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-112">Version of the license.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-113">**dwLicenseId**</span><span class="sxs-lookup"><span data-stu-id="fa164-113">**dwLicenseId**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-114">ID della licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-114">ID of the license.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-115">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="fa164-115">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-116">ID del [**LSKeyPack**](lskeypack.md) che contiene la licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-116">ID of the [**LSKeyPack**](lskeypack.md) that contains the license.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-117">**szHWID**</span><span class="sxs-lookup"><span data-stu-id="fa164-117">**szHWID**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-118">ID hardware del client di Connessione Desktop remoto (RDC) che ha emesso la licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-118">Hardware ID of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-119">**szMachineName**</span><span class="sxs-lookup"><span data-stu-id="fa164-119">**szMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-120">Nome del client di Connessione Desktop remoto (RDC) che ha emesso la licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-120">Name of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-121">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="fa164-121">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-122">Nome dell'utente che ha emesso la licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-122">Name of the user who was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-123">**dwCertSerialLicense**</span><span class="sxs-lookup"><span data-stu-id="fa164-123">**dwCertSerialLicense**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-124">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="fa164-124">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-125">**dwLicenseSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="fa164-125">**dwLicenseSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-126">Numero di serie della licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-126">Serial number of the license.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-127">**ftIssueDate**</span><span class="sxs-lookup"><span data-stu-id="fa164-127">**ftIssueDate**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-128">Data di rilascio della licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-128">Date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-129">**ftExpireDate**</span><span class="sxs-lookup"><span data-stu-id="fa164-129">**ftExpireDate**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-130">Data di scadenza della licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-130">Date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="fa164-131">**ucLicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="fa164-131">**ucLicenseStatus**</span></span>
</dt> <dd>

<span data-ttu-id="fa164-132">Stato corrente della licenza.</span><span class="sxs-lookup"><span data-stu-id="fa164-132">Current status of the license.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa164-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa164-133">Requirements</span></span>



| <span data-ttu-id="fa164-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa164-134">Requirement</span></span> | <span data-ttu-id="fa164-135">Valore</span><span class="sxs-lookup"><span data-stu-id="fa164-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fa164-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa164-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fa164-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa164-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fa164-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa164-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fa164-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa164-139">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa164-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa164-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa164-141">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="fa164-141">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="fa164-142">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="fa164-142">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="fa164-143">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="fa164-143">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="fa164-144">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="fa164-144">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

 





