---
description: Recupera i certificati di sistema in un sistema host.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Metodo GetSystemCertificates della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5464d420b7fc019a0829d7255dafb1716e5e9f5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525242"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="a774d-103">Metodo GetSystemCertificates della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="a774d-103">GetSystemCertificates method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="a774d-104">Recupera i certificati di sistema in un sistema host.</span><span class="sxs-lookup"><span data-stu-id="a774d-104">Retrieves the system certificates on a host system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a774d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a774d-105">Syntax</span></span>


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a><span data-ttu-id="a774d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a774d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a774d-107">*EncodedCertificates* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a774d-107">*EncodedCertificates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a774d-108">Se l'esito è positivo, riceve i certificati disponibili nell'archivio personale del computer locale.</span><span class="sxs-lookup"><span data-stu-id="a774d-108">If successful, receives the certificates available from the Personal store for the local machine.</span></span> <span data-ttu-id="a774d-109">Ogni voce è una stringa di certificato con codifica base 64.</span><span class="sxs-lookup"><span data-stu-id="a774d-109">Each entry is a base 64 encoded certificate string.</span></span> <span data-ttu-id="a774d-110">Questa stringa può essere convertita in una matrice di byte costruendo un oggetto X509Certificate2.</span><span class="sxs-lookup"><span data-stu-id="a774d-110">This string can be converted to a byte array by constructing an X509Certificate2 object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a774d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a774d-111">Return value</span></span>

<span data-ttu-id="a774d-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a774d-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a774d-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="a774d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="a774d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="a774d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="a774d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="a774d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="a774d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="a774d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a774d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a774d-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="a774d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a774d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="a774d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a774d-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a774d-126">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="a774d-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a774d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a774d-127">Requirements</span></span>



| <span data-ttu-id="a774d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a774d-128">Requirement</span></span> | <span data-ttu-id="a774d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a774d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a774d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a774d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a774d-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a774d-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a774d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a774d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a774d-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a774d-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a774d-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a774d-134">Namespace</span></span><br/>                | <span data-ttu-id="a774d-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a774d-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a774d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a774d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a774d-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a774d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a774d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a774d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a774d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a774d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a774d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a774d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a774d-141">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="a774d-141">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

 




