---
title: Classe Win32_RDMSJoinedNode
description: Rappresenta un nodo del server gestito da Desktop remoto Management Services (RDBMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSJoinedNode Servizi Desktop remoto
- Classe Win32_RDMSJoinedNode Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400276"
---
# <a name="win32_rdmsjoinednode-class"></a><span data-ttu-id="937bc-105">Win32 \_ RDMSJoinedNode (classe)</span><span class="sxs-lookup"><span data-stu-id="937bc-105">Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="937bc-106">Rappresenta un nodo del server gestito da Desktop remoto Management Services (RDBMS).</span><span class="sxs-lookup"><span data-stu-id="937bc-106">Represents a server node that is managed by Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="937bc-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="937bc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="937bc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="937bc-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a><span data-ttu-id="937bc-109">Members</span><span class="sxs-lookup"><span data-stu-id="937bc-109">Members</span></span>

<span data-ttu-id="937bc-110">La classe **Win32 \_ RDMSJoinedNode** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="937bc-110">The **Win32\_RDMSJoinedNode** class has these types of members:</span></span>

-   [<span data-ttu-id="937bc-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="937bc-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="937bc-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="937bc-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="937bc-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="937bc-113">Methods</span></span>

<span data-ttu-id="937bc-114">La classe **Win32 \_ RDMSJoinedNode** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="937bc-114">The **Win32\_RDMSJoinedNode** class has these methods.</span></span>



| <span data-ttu-id="937bc-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="937bc-115">Method</span></span>                                                                | <span data-ttu-id="937bc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="937bc-116">Description</span></span>                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="937bc-117">**GetJoinedNodeCount**</span><span class="sxs-lookup"><span data-stu-id="937bc-117">**GetJoinedNodeCount**</span></span>](win32-rdmsjoinednode-getjoinednodecount.md) | <span data-ttu-id="937bc-118">**Windows server 2012 R2 e Windows server 2012:** Questo metodo non è disponibile prima di Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="937bc-118">**Windows Server 2012 R2 and Windows Server 2012:** This method is unavailable prior to Windows Server 2016.</span></span><br/> <span data-ttu-id="937bc-119">Ottiene il numero di server in cui è installato il ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="937bc-119">Gets the number of servers that have the specified role installed.</span></span><br/> |
| [<span data-ttu-id="937bc-120">**Partecipa**</span><span class="sxs-lookup"><span data-stu-id="937bc-120">**Join**</span></span>](join-win32-rdmsjoinednode.md)                             | <span data-ttu-id="937bc-121">Aggiunge un nodo a RDBMS.</span><span class="sxs-lookup"><span data-stu-id="937bc-121">Adds a node to RDMS.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="937bc-122">**Separazione**</span><span class="sxs-lookup"><span data-stu-id="937bc-122">**Unjoin**</span></span>](unjoin-win32-rdmsjoinednode.md)                         | <span data-ttu-id="937bc-123">Rimuove un nodo da RDBMS.</span><span class="sxs-lookup"><span data-stu-id="937bc-123">Removes a node from RDMS.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="937bc-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="937bc-124">Properties</span></span>

<span data-ttu-id="937bc-125">La classe **Win32 \_ RDMSJoinedNode** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="937bc-125">The **Win32\_RDMSJoinedNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="937bc-126">**Nome di dominio completo**</span><span class="sxs-lookup"><span data-stu-id="937bc-126">**FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="937bc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="937bc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="937bc-129">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="937bc-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="937bc-130">Ottiene il nome di dominio completo del nodo.</span><span class="sxs-lookup"><span data-stu-id="937bc-130">Gets the fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-131">**IsGatewayCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="937bc-131">**IsGatewayCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-132">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-134">Ottiene e imposta un valore che indica se il server dispone di un certificato per eseguire l'autenticazione per le connessioni del Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="937bc-134">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop gateway connections.</span></span> <span data-ttu-id="937bc-135">**True** se il certificato è installato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-135">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-136">**IsPublishingCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="937bc-136">**IsPublishingCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-137">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-139">Ottiene e imposta un valore che indica se il server dispone di un certificato per firmare i file di pubblicazione Remote Desktop Protocol.</span><span class="sxs-lookup"><span data-stu-id="937bc-139">Gets and sets a value that indicates whether the server has a certificate to sign Remote Desktop Protocol publishing files.</span></span> <span data-ttu-id="937bc-140">**True** se il certificato è installato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-140">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-141">**IsRdcb**</span><span class="sxs-lookup"><span data-stu-id="937bc-141">**IsRdcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-144">Ottiene e imposta un valore che indica se il server è Connessione Desktop remoto broker.</span><span class="sxs-lookup"><span data-stu-id="937bc-144">Gets and sets a value that indicates whether the server is Remote Desktop Connection Broker.</span></span> <span data-ttu-id="937bc-145">**True** se il server è un Broker di connessione Desktop remoto; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-145">**TRUE** if the server is a Remote Desktop Connection Broker; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-146">**IsRdg**</span><span class="sxs-lookup"><span data-stu-id="937bc-146">**IsRdg**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-147">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-149">Ottiene e imposta un valore che indica se il server è Desktop remoto server gateway.</span><span class="sxs-lookup"><span data-stu-id="937bc-149">Gets and sets a value that indicates whether the server is Remote Desktop gateway server.</span></span> <span data-ttu-id="937bc-150">**True** se il server è un server Gateway Desktop remoto; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-150">**TRUE** if the server is a Remote Desktop gateway server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-151">**IsRdls**</span><span class="sxs-lookup"><span data-stu-id="937bc-151">**IsRdls**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-152">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-154">Ottiene e imposta un valore che indica se il server è Desktop remoto server licenze.</span><span class="sxs-lookup"><span data-stu-id="937bc-154">Gets and sets a value that indicates whether the server is Remote Desktop license server.</span></span> <span data-ttu-id="937bc-155">**True** se il server è un server licenze Desktop remoto; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-155">**TRUE** if the server is a Remote Desktop license server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-156">**IsRdsh**</span><span class="sxs-lookup"><span data-stu-id="937bc-156">**IsRdsh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-157">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-159">Ottiene e imposta un valore che indica se il server è Desktop remoto server Host sessione.</span><span class="sxs-lookup"><span data-stu-id="937bc-159">Gets and sets a value that indicates whether the server is Remote Desktop session host server.</span></span> <span data-ttu-id="937bc-160">**True** se il server è un server Host sessione di desktop remoto; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-160">**TRUE** if the server is a Remote Desktop session host server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-161">**IsRdvh**</span><span class="sxs-lookup"><span data-stu-id="937bc-161">**IsRdvh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-162">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-164">Ottiene e imposta un valore che indica se il server è Desktop remoto host di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="937bc-164">Gets and sets a value that indicates whether the server is Remote Desktop virtualization host.</span></span> <span data-ttu-id="937bc-165">**True** se il server è un host di virtualizzazione Desktop remoto; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-165">**TRUE** if the server is a Remote Desktop virtualization host; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-166">**IsRdwa**</span><span class="sxs-lookup"><span data-stu-id="937bc-166">**IsRdwa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-167">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-167">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-168">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-168">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-169">Ottiene e imposta un valore che indica se il server è Desktop remoto server Accesso Web.</span><span class="sxs-lookup"><span data-stu-id="937bc-169">Gets and sets a value that indicates whether the server is Remote Desktop web access server.</span></span> <span data-ttu-id="937bc-170">**True** se il server è un desktop remoto accesso Web Server; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-170">**TRUE** if the server is a Remote Desktop Web Access server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-171">**IsRedirectorCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="937bc-171">**IsRedirectorCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-172">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-174">Ottiene e imposta un valore che indica se il server dispone di un certificato per eseguire l'autenticazione per la distribuzione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="937bc-174">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Services deployment.</span></span> <span data-ttu-id="937bc-175">**True** se il certificato è installato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-175">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-176">**IsWebAccessCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="937bc-176">**IsWebAccessCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-177">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="937bc-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="937bc-179">Ottiene e imposta un valore che indica se il server dispone di un certificato per eseguire l'autenticazione per Desktop remoto Accesso Web.</span><span class="sxs-lookup"><span data-stu-id="937bc-179">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Web Access.</span></span> <span data-ttu-id="937bc-180">**True** se il certificato è installato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="937bc-180">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-181">**OSVersion**</span><span class="sxs-lookup"><span data-stu-id="937bc-181">**OSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="937bc-182">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-183">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="937bc-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="937bc-184">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="937bc-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="937bc-185">Ottiene e imposta la versione dei sistemi operativi nel nodo.</span><span class="sxs-lookup"><span data-stu-id="937bc-185">Gets and sets the version of the operating systems on the node.</span></span>

</dd> <dt>

<span data-ttu-id="937bc-186">**SID**</span><span class="sxs-lookup"><span data-stu-id="937bc-186">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="937bc-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="937bc-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="937bc-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="937bc-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="937bc-189">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="937bc-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="937bc-190">Ottiene l'ID di sicurezza (SID) del nodo.</span><span class="sxs-lookup"><span data-stu-id="937bc-190">Gets the security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="937bc-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="937bc-191">Requirements</span></span>



| <span data-ttu-id="937bc-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="937bc-192">Requirement</span></span> | <span data-ttu-id="937bc-193">Valore</span><span class="sxs-lookup"><span data-stu-id="937bc-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="937bc-194">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="937bc-194">Minimum supported client</span></span><br/> | <span data-ttu-id="937bc-195">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="937bc-195">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="937bc-196">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="937bc-196">Minimum supported server</span></span><br/> | <span data-ttu-id="937bc-197">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="937bc-197">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="937bc-198">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="937bc-198">Namespace</span></span><br/>                | <span data-ttu-id="937bc-199">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="937bc-199">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="937bc-200">MOF</span><span class="sxs-lookup"><span data-stu-id="937bc-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="937bc-201"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="937bc-201"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="937bc-202">DLL</span><span class="sxs-lookup"><span data-stu-id="937bc-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="937bc-203"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="937bc-203"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="937bc-204">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="937bc-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="937bc-205">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="937bc-205">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

