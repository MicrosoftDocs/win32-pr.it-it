---
title: Classe Win32_TSDeploymentSettings
description: Definisce le impostazioni predefinite utilizzate dal Gestione RemoteApp durante la creazione di file di Remote Desktop Protocol (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSDeploymentSettings Servizi Desktop remoto
- Classe Win32_TSDeploymentSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476391"
---
# <a name="win32_tsdeploymentsettings-class"></a><span data-ttu-id="e0ad8-105">Win32 \_ TSDeploymentSettings (classe)</span><span class="sxs-lookup"><span data-stu-id="e0ad8-105">Win32\_TSDeploymentSettings class</span></span>

<span data-ttu-id="e0ad8-106">Definisce le impostazioni predefinite utilizzate dal Gestione RemoteApp durante la creazione di file di Remote Desktop Protocol (RDP).</span><span class="sxs-lookup"><span data-stu-id="e0ad8-106">Defines the default settings that the RemoteApp Manager uses when creating Remote Desktop Protocol (RDP) files.</span></span> <span data-ttu-id="e0ad8-107">Queste impostazioni non influiscono su applicazioni o desktop pubblicati.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-107">These settings do not affect any published applications or desktops.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ad8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0ad8-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="e0ad8-109">Members</span><span class="sxs-lookup"><span data-stu-id="e0ad8-109">Members</span></span>

<span data-ttu-id="e0ad8-110">La classe **Win32 \_ TSDeploymentSettings** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e0ad8-110">The **Win32\_TSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="e0ad8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0ad8-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0ad8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0ad8-112">Properties</span></span>

<span data-ttu-id="e0ad8-113">La classe **Win32 \_ TSDeploymentSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-113">The **Win32\_TSDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0ad8-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-115">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-117">Indica se consentire la smussatura dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-117">Indicates whether to allow font smoothing.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e0ad8-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-122">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e0ad8-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0ad8-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-124">**CertificateExpiresOn**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-124">**CertificateExpiresOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-127">Data di scadenza del certificato.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-127">The date that the certificate expires on.</span></span> <span data-ttu-id="e0ad8-128">Questo valore viene archiviato come formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-128">This value is stored as a 64-bit [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-129">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-129">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-130">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-132">Identificazione personale del certificato utilizzato per firmare i file RDP.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-132">The thumbprint of the certificate that is used to sign RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-133">**CertificateIssuedBy**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-133">**CertificateIssuedBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-136">Specifica il certificato emesso da.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-136">Specifies who the certificate is issued by.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-137">**CertificateIssuedTo**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-137">**CertificateIssuedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-140">Specifica la persona a cui viene rilasciato il certificato.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-140">Specifies who the certificate is issued to.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-141">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-141">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-142">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-144">Profondità in bit del colore dello schermo.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-144">The color bit depth of the display.</span></span> <span data-ttu-id="e0ad8-145">I valori possibili sono 4, 8, 15, 16, 24 e 32.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-145">Possible values are 4, 8, 15, 16, 24, and 32.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-146">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-146">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-149">Contenuto del file RDP che corrisponde alle impostazioni RDP personalizzate in Gestione RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-149">The contents of the RDP file that correspond to the Custom RDP Settings in RemoteApp Manager.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-150">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-150">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-153">Contenuto del file RDP che corrisponde alle impostazioni di distribuzione in Gestione RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-153">The contents of the RDP file that correspond to the deployment settings in RemoteApp Manager.</span></span> <span data-ttu-id="e0ad8-154">Se questo valore è impostato, le impostazioni di distribuzione RDP sostituiscono le impostazioni predefinite in questa classe.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-154">If this value is set, the RDP deployment settings supersede the default settings in this class.</span></span> <span data-ttu-id="e0ad8-155">Se, ad esempio, si imposta la proprietà **GatewayAuthMode** in questa classe e si imposta la proprietà **DeploymentRDPSettings** , la proprietà **GatewayAuthMode** di questa classe verrà ignorata e verrà utilizzato il valore **GatewayAuthMode** del **DeploymentRDPSettings** .</span><span class="sxs-lookup"><span data-stu-id="e0ad8-155">For example, if you set the **GatewayAuthMode** property in this class, and set the **DeploymentRDPSettings** property, the **GatewayAuthMode** property from this class will be ignored and the **GatewayAuthMode** value from the **DeploymentRDPSettings** will be used.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-156">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-159">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-159">Description of the object.</span></span>

<span data-ttu-id="e0ad8-160">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0ad8-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-161">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-161">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-164">Il nome del server Host sessione Desktop remoto o il nome di dominio completo (FQDN) dell'host sessione Desktop remoto server farm.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-164">The name of the RD Session Host server, or the fully qualified domain name (FQDN) of the RD Session Host server farm.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-165">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-165">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-166">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-166">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-167">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-168">Metodo di autenticazione Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-168">The RD Gateway authentication method.</span></span> <span data-ttu-id="e0ad8-169">Sono possibili i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-169">The following values are possible.</span></span>

<dt>

<span data-ttu-id="e0ad8-170">0</span><span class="sxs-lookup"><span data-stu-id="e0ad8-170">0</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-171">Password</span><span class="sxs-lookup"><span data-stu-id="e0ad8-171">Password</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-172">1</span><span class="sxs-lookup"><span data-stu-id="e0ad8-172">1</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-173">Smart card</span><span class="sxs-lookup"><span data-stu-id="e0ad8-173">Smart card</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-174">4</span><span class="sxs-lookup"><span data-stu-id="e0ad8-174">4</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-175">Consenti all'utente di selezionare durante la connessione.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-175">Allow user to select during connection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e0ad8-176">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-176">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-179">Nome del server Gateway Desktop remoto da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-179">The name of the RD Gateway server to use.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-180">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-180">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-181">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-182">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-183">Indica se utilizzare un server Gateway Desktop remoto per connettersi al server Host sessione Desktop remoto di destinazione in un firewall.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-183">Indicates whether to use an RD Gateway server to connect to the target RD Session Host server across a firewall.</span></span> <span data-ttu-id="e0ad8-184">Sono possibili i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-184">The following values are possible.</span></span>

<dt>

<span data-ttu-id="e0ad8-185">0</span><span class="sxs-lookup"><span data-stu-id="e0ad8-185">0</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-186">Non usare un server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-186">Do not use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-187">1</span><span class="sxs-lookup"><span data-stu-id="e0ad8-187">1</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-188">Utilizzare un server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-188">Use an RD Gateway server.</span></span> <span data-ttu-id="e0ad8-189">Ignorare il server Gateway Desktop remoto per gli indirizzi locali.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-189">Bypass the RD Gateway server for local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-190">2</span><span class="sxs-lookup"><span data-stu-id="e0ad8-190">2</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-191">Utilizzare un server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-191">Use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-192">3</span><span class="sxs-lookup"><span data-stu-id="e0ad8-192">3</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-193">Rileva automaticamente le impostazioni del server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-193">Automatically detect RD Gateway server settings.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e0ad8-194">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-194">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-195">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-196">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-196">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-197">Quando possibile, utilizzare le stesse credenziali utente per il server Gateway Desktop remoto e il server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-197">When possible, use the same user credentials for the RD Gateway server and the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-198">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-198">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-199">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-200">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-201">Indica se utilizzare un certificato per firmare i file RDP.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-201">Indicates whether to use a certificate to sign the RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-203">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-205">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="e0ad8-205">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-206">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-206">The date the object was installed.</span></span> <span data-ttu-id="e0ad8-207">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-207">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e0ad8-208">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0ad8-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-209">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-209">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-212">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-212">The name of the object.</span></span>

<span data-ttu-id="e0ad8-213">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0ad8-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-214">**Porta**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-214">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-215">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-216">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-217">Porta RDP da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-217">The RDP port to use.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-218">**RedirectionOptions**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-218">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-219">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-221">Specifica le opzioni di reindirizzamento delle risorse e del dispositivo per le connessioni RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-221">Specifies the device and resource redirection options for RemoteApp connections.</span></span> <span data-ttu-id="e0ad8-222">I flag per **RedirectionOptions** possono essere combinati.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-222">Flags for **RedirectionOptions** can be combined.</span></span> <span data-ttu-id="e0ad8-223">Sono possibili i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-223">The following values are possible.</span></span>

<dt>

<span data-ttu-id="e0ad8-224">0</span><span class="sxs-lookup"><span data-stu-id="e0ad8-224">0</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-225">Nessun reindirizzamento di dispositivi o risorse.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-225">No device or resource redirection.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-226">1</span><span class="sxs-lookup"><span data-stu-id="e0ad8-226">1</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-227">Reindirizza unità disco.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-227">Redirect disk drives.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-228">2</span><span class="sxs-lookup"><span data-stu-id="e0ad8-228">2</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-229">Reindirizza le stampanti.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-229">Redirect printers.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-230">4</span><span class="sxs-lookup"><span data-stu-id="e0ad8-230">4</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-231">Reindirizzare gli Appunti.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-231">Redirect the Clipboard.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-232">8</span><span class="sxs-lookup"><span data-stu-id="e0ad8-232">8</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-233">Reindirizza i dispositivi Plug and Play supportati.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-233">Redirect supported Plug and Play devices.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-234">16</span><span class="sxs-lookup"><span data-stu-id="e0ad8-234">16</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-235">Reindirizza le smart card.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-235">Redirect smart cards.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-236">32</span><span class="sxs-lookup"><span data-stu-id="e0ad8-236">32</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-237">Reindirizza audio.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-237">Redirect audio.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-238">64</span><span class="sxs-lookup"><span data-stu-id="e0ad8-238">64</span></span>
</dt> <dd>

<span data-ttu-id="e0ad8-239">Reindirizza le porte seriali.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-239">Redirect serial ports.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e0ad8-240">**RequireServerAuth**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-240">**RequireServerAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-241">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-242">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-243">Indica se richiedere l'autenticazione server.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-243">Indicates whether to require server authentication.</span></span>

</dd> <dt>

<span data-ttu-id="e0ad8-244">**Status**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-244">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-245">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-247">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e0ad8-247">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-248">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-248">Current status of the object.</span></span> <span data-ttu-id="e0ad8-249">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-249">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e0ad8-250">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="e0ad8-250">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e0ad8-251">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="e0ad8-251">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e0ad8-252">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-252">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e0ad8-253">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-253">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e0ad8-254">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0ad8-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e0ad8-255">("OK")</span><span class="sxs-lookup"><span data-stu-id="e0ad8-255">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0ad8-256">("Errore")</span><span class="sxs-lookup"><span data-stu-id="e0ad8-256">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0ad8-257">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="e0ad8-257">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0ad8-258">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="e0ad8-258">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0ad8-259">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="e0ad8-259">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0ad8-260">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="e0ad8-260">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0ad8-261">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="e0ad8-261">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0ad8-262">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="e0ad8-262">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e0ad8-263">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-263">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ad8-264">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e0ad8-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0ad8-265">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e0ad8-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0ad8-266">Indica se sono abilitati più monitoraggi per il desktop.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-266">Indicates if multiple monitors are enabled for the desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0ad8-267">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0ad8-267">Remarks</span></span>

<span data-ttu-id="e0ad8-268">Per impostare le proprietà tramite questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-268">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="e0ad8-269">Se **RequireServerAuth** è impostato su **true**, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e0ad8-269">If **RequireServerAuth** is set to **TRUE**, consider the following:</span></span>

-   <span data-ttu-id="e0ad8-270">Se il programma RemoteApp è per l'utilizzo nella Intranet e tutti i computer client eseguono Windows Server 2008 o Windows Vista, non è necessario configurare il server Host sessione Desktop remoto per l'utilizzo di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-270">If the RemoteApp program is for intranet use, and all client computers are running either Windows Server 2008 or Windows Vista, you do not have to configure the RD Session Host server to use an SSL certificate.</span></span> <span data-ttu-id="e0ad8-271">In questo caso, viene utilizzato Autenticazione a livello di rete.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-271">In this case, Network Level Authentication is used.</span></span>
-   <span data-ttu-id="e0ad8-272">Per il valore della proprietà **farmname** , è necessario specificare il nome di dominio completo del server o della farm.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-272">You must specify the FQDN of the server or farm for the value of the **FarmName** property.</span></span>

<span data-ttu-id="e0ad8-273">Per connettersi allo \\ spazio dei nomi "CIMV2 TerminalServices", è necessario che il livello di autenticazione includa la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-273">To connect to the "CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="e0ad8-274">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_**, che può essere impostato tramite la funzione com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="e0ad8-274">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="e0ad8-275">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-275">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="e0ad8-276">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-276">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="e0ad8-277">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e0ad8-277">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e0ad8-278">Vengono installati nel computer quando si aggiunge il ruolo associato.</span><span class="sxs-lookup"><span data-stu-id="e0ad8-278">They are installed on the computer when you add the associated role.</span></span> <span data-ttu-id="e0ad8-279">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e0ad8-279">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ad8-280">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0ad8-280">Requirements</span></span>



| <span data-ttu-id="e0ad8-281">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0ad8-281">Requirement</span></span> | <span data-ttu-id="e0ad8-282">Valore</span><span class="sxs-lookup"><span data-stu-id="e0ad8-282">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ad8-283">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ad8-283">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ad8-284">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e0ad8-284">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e0ad8-285">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ad8-285">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ad8-286">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0ad8-286">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0ad8-287">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0ad8-287">Namespace</span></span><br/>                | <span data-ttu-id="e0ad8-288">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e0ad8-288">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e0ad8-289">MOF</span><span class="sxs-lookup"><span data-stu-id="e0ad8-289">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0ad8-290"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0ad8-290"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="e0ad8-291">DLL</span><span class="sxs-lookup"><span data-stu-id="e0ad8-291">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0ad8-292"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0ad8-292"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

