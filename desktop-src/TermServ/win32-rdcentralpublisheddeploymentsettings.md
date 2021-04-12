---
title: Classe Win32_RDCentralPublishedDeploymentSettings
description: Contiene le impostazioni di distribuzione utilizzate per generare file RDP per le risorse pubblicate da una farm.
ms.assetid: 6d1be0b2-e070-4c60-8068-b59ba121bf9f
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDCentralPublishedDeploymentSettings Servizi Desktop remoto
- Classe Win32_RDCentralPublishedDeploymentSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedDeploymentSettings
- Win32_RDCentralPublishedDeploymentSettings.Caption
- Win32_RDCentralPublishedDeploymentSettings.Description
- Win32_RDCentralPublishedDeploymentSettings.InstallDate
- Win32_RDCentralPublishedDeploymentSettings.Name
- Win32_RDCentralPublishedDeploymentSettings.Status
- Win32_RDCentralPublishedDeploymentSettings.PublishingFarm
- Win32_RDCentralPublishedDeploymentSettings.Port
- Win32_RDCentralPublishedDeploymentSettings.FarmName
- Win32_RDCentralPublishedDeploymentSettings.GatewayUsage
- Win32_RDCentralPublishedDeploymentSettings.GatewayName
- Win32_RDCentralPublishedDeploymentSettings.GatewayAuthMode
- Win32_RDCentralPublishedDeploymentSettings.GatewayUseCachedCreds
- Win32_RDCentralPublishedDeploymentSettings.ColorBitDepth
- Win32_RDCentralPublishedDeploymentSettings.AllowFontSmoothing
- Win32_RDCentralPublishedDeploymentSettings.UseMultimon
- Win32_RDCentralPublishedDeploymentSettings.RedirectionOptions
- Win32_RDCentralPublishedDeploymentSettings.HasCertificate
- Win32_RDCentralPublishedDeploymentSettings.CertificateHash
- Win32_RDCentralPublishedDeploymentSettings.CustomRDPSettings
- Win32_RDCentralPublishedDeploymentSettings.DeploymentRDPSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b118f2fabf22f10e47c0b8467b0ddf6388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400876"
---
# <a name="win32_rdcentralpublisheddeploymentsettings-class"></a><span data-ttu-id="adc6c-105">Win32 \_ RDCentralPublishedDeploymentSettings (classe)</span><span class="sxs-lookup"><span data-stu-id="adc6c-105">Win32\_RDCentralPublishedDeploymentSettings class</span></span>

<span data-ttu-id="adc6c-106">Contiene le impostazioni di distribuzione utilizzate per generare file RDP per le risorse pubblicate da una farm.</span><span class="sxs-lookup"><span data-stu-id="adc6c-106">Contains the deployment settings used to generate RDP files for resources published from a farm.</span></span>

<span data-ttu-id="adc6c-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="adc6c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc6c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="adc6c-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="adc6c-109">Members</span><span class="sxs-lookup"><span data-stu-id="adc6c-109">Members</span></span>

<span data-ttu-id="adc6c-110">La classe **Win32 \_ RDCentralPublishedDeploymentSettings** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="adc6c-110">The **Win32\_RDCentralPublishedDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="adc6c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="adc6c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="adc6c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="adc6c-112">Properties</span></span>

<span data-ttu-id="adc6c-113">La classe **Win32 \_ RDCentralPublishedDeploymentSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="adc6c-113">The **Win32\_RDCentralPublishedDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="adc6c-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="adc6c-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-115">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="adc6c-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-117">**true** per consentire la smussatura dei caratteri; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="adc6c-117">**true** to allow font smoothing; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="adc6c-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="adc6c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="adc6c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="adc6c-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-122">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="adc6c-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="adc6c-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="adc6c-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-124">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="adc6c-124">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-125">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="adc6c-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-127">Certificato utilizzato per firmare i file RDP; necessariamente solo se *HasCertificate* è true.</span><span class="sxs-lookup"><span data-stu-id="adc6c-127">The certificate used to sign the RDP files; necessarily only if *HasCertificate* is true.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-128">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="adc6c-128">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adc6c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-131">Contiene la profondità del bit di colore:</span><span class="sxs-lookup"><span data-stu-id="adc6c-131">Contains the color bit depth:</span></span>

<dt>

<span id="4"></span>

<span data-ttu-id="adc6c-132">**4** ()</span><span class="sxs-lookup"><span data-stu-id="adc6c-132">**4** ()</span></span>


</dt> <dd></dd> <dt>

<span id="8"></span>

<span data-ttu-id="adc6c-133">**8** ()</span><span class="sxs-lookup"><span data-stu-id="adc6c-133">**8** ()</span></span>


</dt> <dd></dd> <dt>

<span id="15"></span>

<span data-ttu-id="adc6c-134">**15** ()</span><span class="sxs-lookup"><span data-stu-id="adc6c-134">**15** ()</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="adc6c-135">**16** ()</span><span class="sxs-lookup"><span data-stu-id="adc6c-135">**16** ()</span></span>


</dt> <dd></dd> <dt>

<span id="24"></span>

<span data-ttu-id="adc6c-136">**24** ()</span><span class="sxs-lookup"><span data-stu-id="adc6c-136">**24** ()</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="adc6c-137">**32** ()</span><span class="sxs-lookup"><span data-stu-id="adc6c-137">**32** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="adc6c-138">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="adc6c-138">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="adc6c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-141">Contiene il contenuto del file RDP corrispondente alle impostazioni RDP personalizzate.</span><span class="sxs-lookup"><span data-stu-id="adc6c-141">Contains the contents of the RDP file corresponding to the custom RDP settings.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-142">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="adc6c-142">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="adc6c-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-145">Contiene il contenuto del file RDP corrispondente alle impostazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="adc6c-145">Contains the contents of the RDP file corresponding to the deployment settings.</span></span> <span data-ttu-id="adc6c-146">Se questo parametro è impostato, il sistema utilizzerà questo file RDP e ignorerà le altre impostazioni RDP in questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="adc6c-146">If this parameter is set, the system will use this RDP file, and ignore the other RDP settings in this call.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-147">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="adc6c-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="adc6c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="adc6c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-150">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="adc6c-150">Description of the object.</span></span>

<span data-ttu-id="adc6c-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="adc6c-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-152">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="adc6c-152">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="adc6c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-155">Nome della farm.</span><span class="sxs-lookup"><span data-stu-id="adc6c-155">The name of the farm.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-156">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="adc6c-156">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-157">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adc6c-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-159">Contiene la modalità di autenticazione del gateway:</span><span class="sxs-lookup"><span data-stu-id="adc6c-159">Contains the gateway authentication mode:</span></span>

<dt>

<span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>

<span data-ttu-id="adc6c-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Password (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="adc6c-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Password(0)** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>

<span data-ttu-id="adc6c-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Smart Card (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="adc6c-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Smartcard(1)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>

<span data-ttu-id="adc6c-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Consenti all'utente di scegliere (4** ) (4)</span><span class="sxs-lookup"><span data-stu-id="adc6c-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Allow User to Choose(4)** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="adc6c-163">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="adc6c-163">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="adc6c-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-166">Nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="adc6c-166">The name of the gateway.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-167">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="adc6c-167">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-168">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adc6c-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-170">Descrive il modo in cui viene usato il gateway:</span><span class="sxs-lookup"><span data-stu-id="adc6c-170">Describes how the gateway is used:</span></span>

<dt>

<span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>

<span data-ttu-id="adc6c-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**Nogateway** (0)</span><span class="sxs-lookup"><span data-stu-id="adc6c-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**NoGateway** (0)</span></span>


</dt> <dd>

<span data-ttu-id="adc6c-172">Nessun gateway.</span><span class="sxs-lookup"><span data-stu-id="adc6c-172">No gateway.</span></span>

</dd> <dt>

<span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>

<span data-ttu-id="adc6c-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span><span class="sxs-lookup"><span data-stu-id="adc6c-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="adc6c-174">Usare il gateway pass by local.</span><span class="sxs-lookup"><span data-stu-id="adc6c-174">Use gateway pass by local.</span></span>

</dd> <dt>

<span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>

<span data-ttu-id="adc6c-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span><span class="sxs-lookup"><span data-stu-id="adc6c-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span></span>


</dt> <dd>

<span data-ttu-id="adc6c-176">Usare il gateway.</span><span class="sxs-lookup"><span data-stu-id="adc6c-176">Use gateway.</span></span>

</dd> <dt>

<span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>

<span data-ttu-id="adc6c-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span><span class="sxs-lookup"><span data-stu-id="adc6c-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span></span>


</dt> <dd>

<span data-ttu-id="adc6c-178">Rilevare il gateway.</span><span class="sxs-lookup"><span data-stu-id="adc6c-178">Detect gateway.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="adc6c-179">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="adc6c-179">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-180">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="adc6c-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-182">**true** per utilizzare le stesse credenziali utente per gateway di Servizi terminal e server Servizi terminal, quando possibile; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="adc6c-182">**true** to use the same user credentials for TS gateway and TS server when possible; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-183">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="adc6c-183">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="adc6c-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-185">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-186">**true** per utilizzare un certificato per firmare i file RDP; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="adc6c-186">**true** to use a certificate to sign the RDP files; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-187">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="adc6c-187">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-188">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="adc6c-188">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="adc6c-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-190">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="adc6c-190">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-191">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="adc6c-191">The date the object was installed.</span></span> <span data-ttu-id="adc6c-192">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="adc6c-192">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="adc6c-193">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="adc6c-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-194">**Nome**</span><span class="sxs-lookup"><span data-stu-id="adc6c-194">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="adc6c-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="adc6c-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-197">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="adc6c-197">The name of the object.</span></span>

<span data-ttu-id="adc6c-198">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="adc6c-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-199">**Porta**</span><span class="sxs-lookup"><span data-stu-id="adc6c-199">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-200">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adc6c-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-201">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-202">Porta RDP.</span><span class="sxs-lookup"><span data-stu-id="adc6c-202">The RDP port.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-203">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="adc6c-203">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="adc6c-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-205">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-206">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="adc6c-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-207">Alias della farm che ha pubblicato l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="adc6c-207">The alias of the farm that published the application.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-208">**RedirectionOptions**</span><span class="sxs-lookup"><span data-stu-id="adc6c-208">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-209">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="adc6c-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-210">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-211">Opzioni di reindirizzamento:</span><span class="sxs-lookup"><span data-stu-id="adc6c-211">Redirection Options:</span></span>

<dt>

<span data-ttu-id="adc6c-212">0</span><span class="sxs-lookup"><span data-stu-id="adc6c-212">0</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-213">nessuno</span><span class="sxs-lookup"><span data-stu-id="adc6c-213">None</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-214">1</span><span class="sxs-lookup"><span data-stu-id="adc6c-214">1</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-215">Unità</span><span class="sxs-lookup"><span data-stu-id="adc6c-215">Drives</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-216">2</span><span class="sxs-lookup"><span data-stu-id="adc6c-216">2</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-217">Stampanti</span><span class="sxs-lookup"><span data-stu-id="adc6c-217">Printers</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-218">4</span><span class="sxs-lookup"><span data-stu-id="adc6c-218">4</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-219">Appunti</span><span class="sxs-lookup"><span data-stu-id="adc6c-219">Clipboard</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-220">8</span><span class="sxs-lookup"><span data-stu-id="adc6c-220">8</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-221">Plug and Play</span><span class="sxs-lookup"><span data-stu-id="adc6c-221">Plug and Play</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-222">16</span><span class="sxs-lookup"><span data-stu-id="adc6c-222">16</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-223">Smart card</span><span class="sxs-lookup"><span data-stu-id="adc6c-223">Smart Card</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="adc6c-224">**Status**</span><span class="sxs-lookup"><span data-stu-id="adc6c-224">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="adc6c-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="adc6c-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-227">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="adc6c-227">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-228">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="adc6c-228">Current status of the object.</span></span> <span data-ttu-id="adc6c-229">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="adc6c-229">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="adc6c-230">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="adc6c-230">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="adc6c-231">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="adc6c-231">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="adc6c-232">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="adc6c-232">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="adc6c-233">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="adc6c-233">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="adc6c-234">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="adc6c-234">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="adc6c-235">("OK")</span><span class="sxs-lookup"><span data-stu-id="adc6c-235">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="adc6c-236">("Errore")</span><span class="sxs-lookup"><span data-stu-id="adc6c-236">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="adc6c-237">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="adc6c-237">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="adc6c-238">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="adc6c-238">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="adc6c-239">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="adc6c-239">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="adc6c-240">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="adc6c-240">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="adc6c-241">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="adc6c-241">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="adc6c-242">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="adc6c-242">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="adc6c-243">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="adc6c-243">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="adc6c-244">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="adc6c-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="adc6c-245">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="adc6c-245">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="adc6c-246">**true** per abilitare la funzionalità multimonitor per desktop (non binario); in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="adc6c-246">**true** to enable multi-monitor for desktop (not RAIL); otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adc6c-247">Requisiti</span><span class="sxs-lookup"><span data-stu-id="adc6c-247">Requirements</span></span>



| <span data-ttu-id="adc6c-248">Requisito</span><span class="sxs-lookup"><span data-stu-id="adc6c-248">Requirement</span></span> | <span data-ttu-id="adc6c-249">Valore</span><span class="sxs-lookup"><span data-stu-id="adc6c-249">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="adc6c-250">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adc6c-250">Minimum supported client</span></span><br/> | <span data-ttu-id="adc6c-251">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="adc6c-251">None supported</span></span><br/>                                                                |
| <span data-ttu-id="adc6c-252">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adc6c-252">Minimum supported server</span></span><br/> | <span data-ttu-id="adc6c-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="adc6c-253">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="adc6c-254">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="adc6c-254">Namespace</span></span><br/>                | <span data-ttu-id="adc6c-255">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="adc6c-255">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="adc6c-256">MOF</span><span class="sxs-lookup"><span data-stu-id="adc6c-256">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adc6c-257"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="adc6c-257"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="adc6c-258">DLL</span><span class="sxs-lookup"><span data-stu-id="adc6c-258">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adc6c-259"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adc6c-259"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

