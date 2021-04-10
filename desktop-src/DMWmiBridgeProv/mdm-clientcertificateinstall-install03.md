---
title: Classe MDM_ClientCertificateInstall_Install03
description: La \_ classe MDM ClientCertificateInstall \_ Install03 consente all'organizzazione di impostare l'installazione dei certificati client.
ms.assetid: 0083e54c-e621-47da-a20d-17c8bbf7dd3a
keywords:
- Classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, descritta
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03.InstanceID
- MDM_ClientCertificateInstall_Install03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ac690808551e05d6ceba4f3c84bcaa521d4d01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120663"
---
# <a name="mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="151ec-105">\_Classe MDM ClientCertificateInstall \_ Install03</span><span class="sxs-lookup"><span data-stu-id="151ec-105">MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="151ec-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="151ec-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="151ec-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="151ec-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="151ec-108">La classe **MDM \_ ClientCertificateInstall \_ Install03** consente all'organizzazione di impostare l'installazione dei certificati client. Obbligatorio per la registrazione del certificato SCEP.</span><span class="sxs-lookup"><span data-stu-id="151ec-108">The **MDM\_ClientCertificateInstall\_Install03** class enables the enterprise to set the installation of client certificates.Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="151ec-109">Nodo padre per raggruppare la richiesta relativa all'installazione del certificato SCEP.</span><span class="sxs-lookup"><span data-stu-id="151ec-109">Parent node to group SCEP cert install related request.</span></span>

> [!Note]  
> <span data-ttu-id="151ec-110">Anche se i nodi figlio in installazione supportano i comandi Replace, dopo l'invio del comando exec al dispositivo, il dispositivo utilizzerà i valori impostati quando il comando exec viene accettato.</span><span class="sxs-lookup"><span data-stu-id="151ec-110">Even though the child nodes under Install support Replace commands, after the Exec command is sent to the device, the device will take the values which are set when the Exec command is accepted.</span></span> <span data-ttu-id="151ec-111">Il server non deve aspettarsi che la modifica del valore del nodo dopo l'accettazione del comando exec influirà sulla registrazione in corso.</span><span class="sxs-lookup"><span data-stu-id="151ec-111">The server should not expect the node value change after Exec command is accepted will impact the current undergoing enrollment.</span></span> <span data-ttu-id="151ec-112">Il server deve verificare il valore del nodo stato e assicurarsi che il dispositivo non sia in fase sconosciuta prima di modificare i valori del nodo figlio.</span><span class="sxs-lookup"><span data-stu-id="151ec-112">The server should check the Status node value and make sure the device is not at unknown stage before changing child node values.</span></span>

 

<span data-ttu-id="151ec-113">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="151ec-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="151ec-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="151ec-114">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_Install03
{
  string InstanceID;
  string ParentID;
  string ServerURL;
  string Challenge;
  string EKUMapping;
  sint32 KeyUsage;
  string SubjectName;
  sint32 KeyProtection;
  sint32 RetryDelay;
  sint32 RetryCount;
  string TemplateName;
  sint32 KeyLength;
  string HashAlgorithm;
  string CAThumbprint;
  string SubjectAlternativeNames;
  string ValidPeriod;
  sint32 ValidPeriodUnits;
  string ContainerName;
  string CustomTextToShowInPrompt;
  string AADKeyIdentifierList;
};
```

## <a name="members"></a><span data-ttu-id="151ec-115">Members</span><span class="sxs-lookup"><span data-stu-id="151ec-115">Members</span></span>

<span data-ttu-id="151ec-116">La classe **MDM \_ ClientCertificateInstall \_ Install03** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="151ec-116">The **MDM\_ClientCertificateInstall\_Install03** class has these types of members:</span></span>

-   [<span data-ttu-id="151ec-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="151ec-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="151ec-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="151ec-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="151ec-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="151ec-119">Methods</span></span>

<span data-ttu-id="151ec-120">La classe **MDM \_ ClientCertificateInstall \_ Install03** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="151ec-120">The **MDM\_ClientCertificateInstall\_Install03** class has these methods.</span></span>



| <span data-ttu-id="151ec-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="151ec-121">Method</span></span>                                                                      | <span data-ttu-id="151ec-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="151ec-122">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="151ec-123">**EnrollMethod**</span><span class="sxs-lookup"><span data-stu-id="151ec-123">**EnrollMethod**</span></span>](mdm-clientcertificateinstall-install03-enrollmethod.md) | <span data-ttu-id="151ec-124">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="151ec-124">Required.</span></span> <span data-ttu-id="151ec-125">Attiva il dispositivo per avviare la registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="151ec-125">Triggers the device to start the certificate enrollment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="151ec-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="151ec-126">Properties</span></span>

<span data-ttu-id="151ec-127">La classe **MDM \_ ClientCertificateInstall \_ Install03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="151ec-127">The **MDM\_ClientCertificateInstall\_Install03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="151ec-128">AADKeyIdentifierList</span><span class="sxs-lookup"><span data-stu-id="151ec-128">AADKeyIdentifierList</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-aadkeyidentifierlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-131">Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="151ec-131">CAThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-cathumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-134">Sfida</span><span class="sxs-lookup"><span data-stu-id="151ec-134">Challenge</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-challenge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-137">ContainerName</span><span class="sxs-lookup"><span data-stu-id="151ec-137">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-140">CustomTextToShowInPrompt</span><span class="sxs-lookup"><span data-stu-id="151ec-140">CustomTextToShowInPrompt</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-customtexttoshowinprompt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-143">EKUMapping</span><span class="sxs-lookup"><span data-stu-id="151ec-143">EKUMapping</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-ekumapping)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-146">HashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="151ec-146">HashAlgorithm</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-hashalgorithm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="151ec-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="151ec-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="151ec-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="151ec-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="151ec-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="151ec-153">Obbligatorio per la registrazione del certificato SCEP.</span><span class="sxs-lookup"><span data-stu-id="151ec-153">Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="151ec-154">Nodo padre per raggruppare la richiesta relativa all'installazione del certificato SCEP.</span><span class="sxs-lookup"><span data-stu-id="151ec-154">Parent node to group SCEP cert install related request.</span></span>

<span data-ttu-id="151ec-155">Il formato è node.</span><span class="sxs-lookup"><span data-stu-id="151ec-155">The Format is node.</span></span>

</dd> <dt>

[<span data-ttu-id="151ec-156">KeyLength</span><span class="sxs-lookup"><span data-stu-id="151ec-156">KeyLength</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keylength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-157">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="151ec-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-159">Protezione di dati</span><span class="sxs-lookup"><span data-stu-id="151ec-159">KeyProtection</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keyprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-160">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="151ec-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-161">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-162">KeyUsage</span><span class="sxs-lookup"><span data-stu-id="151ec-162">KeyUsage</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-163">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="151ec-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-164">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="151ec-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="151ec-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="151ec-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="151ec-168">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="151ec-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="151ec-169">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="151ec-169">Describes the full path to the parent node.</span></span>

<span data-ttu-id="151ec-170">La stringa è "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueId*"</span><span class="sxs-lookup"><span data-stu-id="151ec-170">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*"</span></span>

</dd> <dt>

[<span data-ttu-id="151ec-171">RetryCount</span><span class="sxs-lookup"><span data-stu-id="151ec-171">RetryCount</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrycount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-172">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="151ec-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-174">RetryDelay</span><span class="sxs-lookup"><span data-stu-id="151ec-174">RetryDelay</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrydelay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-175">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="151ec-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-176">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-177">ServerURL</span><span class="sxs-lookup"><span data-stu-id="151ec-177">ServerURL</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-serverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-179">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-180">SubjectAlternativeNames</span><span class="sxs-lookup"><span data-stu-id="151ec-180">SubjectAlternativeNames</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectalternativenames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-182">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-183">SubjectName</span><span class="sxs-lookup"><span data-stu-id="151ec-183">SubjectName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-185">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-185">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-186">TemplateName</span><span class="sxs-lookup"><span data-stu-id="151ec-186">TemplateName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-templatename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-188">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-189">ValidPeriod</span><span class="sxs-lookup"><span data-stu-id="151ec-189">ValidPeriod</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="151ec-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-191">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-191">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="151ec-192">ValidPeriodUnits</span><span class="sxs-lookup"><span data-stu-id="151ec-192">ValidPeriodUnits</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiodunits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="151ec-193">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="151ec-193">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="151ec-194">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="151ec-194">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="151ec-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="151ec-195">Requirements</span></span>



| <span data-ttu-id="151ec-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="151ec-196">Requirement</span></span> | <span data-ttu-id="151ec-197">Valore</span><span class="sxs-lookup"><span data-stu-id="151ec-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="151ec-198">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="151ec-198">Minimum supported client</span></span><br/> | <span data-ttu-id="151ec-199">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="151ec-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="151ec-200">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="151ec-200">Minimum supported server</span></span><br/> | <span data-ttu-id="151ec-201">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="151ec-201">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="151ec-202">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="151ec-202">Namespace</span></span><br/>                | <span data-ttu-id="151ec-203">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="151ec-203">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="151ec-204">MOF</span><span class="sxs-lookup"><span data-stu-id="151ec-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="151ec-205"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="151ec-205"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="151ec-206">DLL</span><span class="sxs-lookup"><span data-stu-id="151ec-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="151ec-207"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="151ec-207"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="151ec-208">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="151ec-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151ec-209">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="151ec-209">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

