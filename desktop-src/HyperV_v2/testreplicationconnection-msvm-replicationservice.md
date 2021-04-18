---
description: Verifica se la replica può essere abilitata dal sistema host corrente al sistema di ripristino specificato.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Metodo TestReplicationConnection della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305969"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="5e176-103">Metodo TestReplicationConnection della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="5e176-103">TestReplicationConnection method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="5e176-104">Verifica se la replica può essere abilitata dal sistema host corrente al sistema di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="5e176-104">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e176-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e176-105">Syntax</span></span>


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5e176-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e176-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e176-107">*RecoveryConnectionPoint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e176-107">*RecoveryConnectionPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e176-108">Nome del punto di connessione.</span><span class="sxs-lookup"><span data-stu-id="5e176-108">The name of the connection point.</span></span> <span data-ttu-id="5e176-109">Per un cluster di ripristino, questo è il nome del CAP del broker.</span><span class="sxs-lookup"><span data-stu-id="5e176-109">For a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="5e176-110">Per un server di ripristino autonomo, questo è il nome del sistema host.</span><span class="sxs-lookup"><span data-stu-id="5e176-110">For a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="5e176-111">*RecoveryServerPortNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e176-111">*RecoveryServerPortNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e176-112">Numero di porta del punto di connessione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5e176-112">The recovery connection point port number.</span></span>

</dd> <dt>

<span data-ttu-id="5e176-113">*AuthenticationType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e176-113">*AuthenticationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e176-114">Schema di autenticazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5e176-114">The recovery authentication scheme.</span></span> <span data-ttu-id="5e176-115">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e176-115">This must be one of the following values.</span></span>

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span data-ttu-id="5e176-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Autenticazione integrata** (1)</span><span class="sxs-lookup"><span data-stu-id="5e176-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrated authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5e176-117">Autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="5e176-117">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="5e176-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticazione basata su certificati** (2)</span><span class="sxs-lookup"><span data-stu-id="5e176-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5e176-119">Autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="5e176-119">Certificate based authentication.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5e176-120">*CertificateThumbPrint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e176-120">*CertificateThumbPrint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e176-121">Identificazione personale del certificato da usare quando il parametro *AuthenticationType* è l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="5e176-121">Certificate thumbprint to use when the *AuthenticationType* parameter is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5e176-122">*BypassProxyServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e176-122">*BypassProxyServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e176-123">Ignora il server proxy per la connessione al server di replica.</span><span class="sxs-lookup"><span data-stu-id="5e176-123">Bypass the proxy server when connecting to the replica server.</span></span>

</dd> <dt>

<span data-ttu-id="5e176-124">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="5e176-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e176-125">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e176-125">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e176-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e176-126">Return value</span></span>

<span data-ttu-id="5e176-127">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e176-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5e176-128">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="5e176-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-129">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="5e176-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-130">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="5e176-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-131">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="5e176-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-132">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="5e176-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-133">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="5e176-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-134">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="5e176-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-135">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="5e176-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-136">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5e176-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-137">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="5e176-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-138">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5e176-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-139">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="5e176-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-140">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="5e176-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="5e176-141">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="5e176-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5e176-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e176-142">Requirements</span></span>



| <span data-ttu-id="5e176-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e176-143">Requirement</span></span> | <span data-ttu-id="5e176-144">Valore</span><span class="sxs-lookup"><span data-stu-id="5e176-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e176-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e176-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5e176-146">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5e176-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5e176-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e176-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5e176-148">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5e176-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e176-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5e176-149">Namespace</span></span><br/>                | <span data-ttu-id="5e176-150">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5e176-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5e176-151">MOF</span><span class="sxs-lookup"><span data-stu-id="5e176-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e176-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e176-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e176-153">DLL</span><span class="sxs-lookup"><span data-stu-id="5e176-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e176-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e176-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e176-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e176-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e176-156">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="5e176-156">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

