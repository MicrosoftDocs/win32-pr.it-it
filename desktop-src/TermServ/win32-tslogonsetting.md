---
title: Classe Win32_TSLogonSetting
description: Definisce le impostazioni di configurazione per la \_ classe terminale Win32 correlate all'accesso client.
ms.assetid: a2ccb419-da1a-44d1-8a7a-4d0266fc1be8
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLogonSetting Servizi Desktop remoto
- Classe Win32_TSLogonSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting
- Win32_TSLogonSetting.Caption
- Win32_TSLogonSetting.Description
- Win32_TSLogonSetting.InstallDate
- Win32_TSLogonSetting.Name
- Win32_TSLogonSetting.Status
- Win32_TSLogonSetting.TerminalName
- Win32_TSLogonSetting.ClientLogonInfoPolicy
- Win32_TSLogonSetting.Domain
- Win32_TSLogonSetting.Password
- Win32_TSLogonSetting.PolicySourceDomain
- Win32_TSLogonSetting.PolicySourcePromptForPassword
- Win32_TSLogonSetting.PolicySourceUserName
- Win32_TSLogonSetting.PromptForPassword
- Win32_TSLogonSetting.UserName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e656f3913bb7320253dc9dbca6710f37e0cbdded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400773"
---
# <a name="win32_tslogonsetting-class"></a><span data-ttu-id="b58bc-105">Win32 \_ TSLogonSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="b58bc-105">Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="b58bc-106">La classe WMI **Win32 \_ TSLogonSetting** definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) correlate all'accesso client.</span><span class="sxs-lookup"><span data-stu-id="b58bc-106">The **Win32\_TSLogonSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

<span data-ttu-id="b58bc-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="b58bc-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="b58bc-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="b58bc-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="b58bc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b58bc-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSLOGONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSLogonSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientLogonInfoPolicy;
  string   Domain;
  string   Password;
  uint32   PolicySourceDomain;
  uint32   PolicySourcePromptForPassword;
  uint32   PolicySourceUserName;
  uint32   PromptForPassword;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="b58bc-110">Members</span><span class="sxs-lookup"><span data-stu-id="b58bc-110">Members</span></span>

<span data-ttu-id="b58bc-111">La classe **Win32 \_ TSLogonSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b58bc-111">The **Win32\_TSLogonSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="b58bc-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b58bc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b58bc-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b58bc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b58bc-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b58bc-114">Methods</span></span>

<span data-ttu-id="b58bc-115">La classe **Win32 \_ TSLogonSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b58bc-115">The **Win32\_TSLogonSetting** class has these methods.</span></span>



| <span data-ttu-id="b58bc-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="b58bc-116">Method</span></span>                                                                    | <span data-ttu-id="b58bc-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b58bc-117">Description</span></span>                                                                    |
|:--------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="b58bc-118">**ExplicitLogon**</span><span class="sxs-lookup"><span data-stu-id="b58bc-118">**ExplicitLogon**</span></span>](win32-tslogonsetting-explicitlogon.md)               | <span data-ttu-id="b58bc-119">Imposta il nome utente, la password e le credenziali di autenticazione del dominio.</span><span class="sxs-lookup"><span data-stu-id="b58bc-119">Sets the UserName, Password, and Domain authentication credentials.</span></span><br/> |
| [<span data-ttu-id="b58bc-120">**SetPromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="b58bc-120">**SetPromptForPassword**</span></span>](win32-tslogonsetting-setpromptforpassword.md) | <span data-ttu-id="b58bc-121">Imposta la proprietà **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="b58bc-121">Sets the **PromptForPassword** property.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="b58bc-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b58bc-122">Properties</span></span>

<span data-ttu-id="b58bc-123">La classe **Win32 \_ TSLogonSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b58bc-123">The **Win32\_TSLogonSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b58bc-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b58bc-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b58bc-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-127">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b58bc-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-128">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b58bc-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="b58bc-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b58bc-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-130">**ClientLogonInfoPolicy**</span><span class="sxs-lookup"><span data-stu-id="b58bc-130">**ClientLogonInfoPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b58bc-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b58bc-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-133">Criterio utilizzato dal server per determinare le impostazioni di connessione.</span><span class="sxs-lookup"><span data-stu-id="b58bc-133">The policy the server uses to determine connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="b58bc-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (0)</span><span class="sxs-lookup"><span data-stu-id="b58bc-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b58bc-135">Sono attive le singole impostazioni di connessione utente.</span><span class="sxs-lookup"><span data-stu-id="b58bc-135">Individual user connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="b58bc-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)</span><span class="sxs-lookup"><span data-stu-id="b58bc-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b58bc-137">Le impostazioni di connessione utente individuali vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="b58bc-137">Individual user connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b58bc-138">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b58bc-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b58bc-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-141">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b58bc-141">Description of the object.</span></span>

<span data-ttu-id="b58bc-142">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b58bc-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-143">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="b58bc-143">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b58bc-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-146">Credenziali di autenticazione per l'accesso al dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b58bc-146">The user's domain logon authentication credential.</span></span> <span data-ttu-id="b58bc-147">Si tratta del dominio in cui risiede il computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b58bc-147">This is the domain in which the user's computer resides.</span></span> <span data-ttu-id="b58bc-148">Questa proprietà non può contenere più di 17 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b58bc-148">This property cannot be longer than 17 characters.</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b58bc-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-150">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b58bc-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-152">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="b58bc-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-153">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b58bc-153">The date the object was installed.</span></span> <span data-ttu-id="b58bc-154">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="b58bc-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b58bc-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b58bc-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-156">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b58bc-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b58bc-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-159">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b58bc-159">The name of the object.</span></span>

<span data-ttu-id="b58bc-160">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b58bc-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-161">**Password**</span><span class="sxs-lookup"><span data-stu-id="b58bc-161">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b58bc-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-164">Credenziali di autenticazione per l'accesso alla password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b58bc-164">The user's password logon authentication credential.</span></span> <span data-ttu-id="b58bc-165">Questa proprietà non può contenere più di 14 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b58bc-165">This property cannot be longer than 14 characters.</span></span> <span data-ttu-id="b58bc-166">Se si esegue una query su questa proprietà, è consigliabile impostare il livello di sicurezza sulla privacy dei pacchetti (wbemAuthenticationLevelPktPrivacy = 6).</span><span class="sxs-lookup"><span data-stu-id="b58bc-166">It is recommended that you set the security level to packet privacy (wbemAuthenticationLevelPktPrivacy = 6) if you query this property.</span></span> <span data-ttu-id="b58bc-167">Questo perché la password non è crittografata in rete senza questo livello di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b58bc-167">This is because the password is not encrypted on the wire without this level of security.</span></span> <span data-ttu-id="b58bc-168">Per ulteriori informazioni sull'impostazione dei livelli di sicurezza, vedere [impostazione della sicurezza del processo dell'applicazione client](/windows/desktop/WmiSdk/setting-client-application-process-security) nella documentazione di WMI SDK.</span><span class="sxs-lookup"><span data-stu-id="b58bc-168">For more information about setting security levels, see [Setting Client Application Process Security](/windows/desktop/WmiSdk/setting-client-application-process-security) in the WMI SDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-169">**PolicySourceDomain**</span><span class="sxs-lookup"><span data-stu-id="b58bc-169">**PolicySourceDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b58bc-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-172">Indica se la proprietà di **dominio** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b58bc-172">Indicates whether the **Domain** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="b58bc-173">0</span><span class="sxs-lookup"><span data-stu-id="b58bc-173">0</span></span>
</dt> <dd>

<span data-ttu-id="b58bc-174">Server</span><span class="sxs-lookup"><span data-stu-id="b58bc-174">Server</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-175">1</span><span class="sxs-lookup"><span data-stu-id="b58bc-175">1</span></span>
</dt> <dd>

<span data-ttu-id="b58bc-176">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="b58bc-176">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-177">2</span><span class="sxs-lookup"><span data-stu-id="b58bc-177">2</span></span>
</dt> <dd>

<span data-ttu-id="b58bc-178">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b58bc-178">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b58bc-179">**PolicySourcePromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="b58bc-179">**PolicySourcePromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-180">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b58bc-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-182">Indica se la proprietà **PromptForPassword** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b58bc-182">Indicates whether the **PromptForPassword** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="b58bc-183">0</span><span class="sxs-lookup"><span data-stu-id="b58bc-183">0</span></span>
</dt> <dd>

<span data-ttu-id="b58bc-184">Server</span><span class="sxs-lookup"><span data-stu-id="b58bc-184">Server</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-185">1</span><span class="sxs-lookup"><span data-stu-id="b58bc-185">1</span></span>
</dt> <dd>

<span data-ttu-id="b58bc-186">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="b58bc-186">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-187">2</span><span class="sxs-lookup"><span data-stu-id="b58bc-187">2</span></span>
</dt> <dd>

<span data-ttu-id="b58bc-188">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b58bc-188">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b58bc-189">**PolicySourceUserName**</span><span class="sxs-lookup"><span data-stu-id="b58bc-189">**PolicySourceUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-190">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b58bc-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-192">Indica se la proprietà **username** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b58bc-192">Indicates whether the **UserName** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="b58bc-193">0</span><span class="sxs-lookup"><span data-stu-id="b58bc-193">0</span></span>
</dt> <dd>

<span data-ttu-id="b58bc-194">Server</span><span class="sxs-lookup"><span data-stu-id="b58bc-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-195">1</span><span class="sxs-lookup"><span data-stu-id="b58bc-195">1</span></span>
</dt> <dd>

<span data-ttu-id="b58bc-196">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="b58bc-196">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-197">2</span><span class="sxs-lookup"><span data-stu-id="b58bc-197">2</span></span>
</dt> <dd>

<span data-ttu-id="b58bc-198">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b58bc-198">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b58bc-199">**PromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="b58bc-199">**PromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-200">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b58bc-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-202">Specifica se all'utente viene sempre richiesta una password durante l'accesso al server.</span><span class="sxs-lookup"><span data-stu-id="b58bc-202">Specifies whether the user is always prompted for a password while logging into the server.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="b58bc-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="b58bc-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b58bc-204">All'utente non viene richiesta una password.</span><span class="sxs-lookup"><span data-stu-id="b58bc-204">The user is not prompted for a password.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="b58bc-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="b58bc-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b58bc-206">All'utente viene richiesta una password.</span><span class="sxs-lookup"><span data-stu-id="b58bc-206">The user is prompted for a password.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b58bc-207">**Status**</span><span class="sxs-lookup"><span data-stu-id="b58bc-207">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b58bc-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-210">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="b58bc-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-211">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b58bc-211">Current status of the object.</span></span> <span data-ttu-id="b58bc-212">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="b58bc-212">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b58bc-213">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="b58bc-213">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b58bc-214">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="b58bc-214">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b58bc-215">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="b58bc-215">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b58bc-216">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="b58bc-216">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b58bc-217">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b58bc-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="b58bc-218">("OK")</span><span class="sxs-lookup"><span data-stu-id="b58bc-218">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b58bc-219">("Errore")</span><span class="sxs-lookup"><span data-stu-id="b58bc-219">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b58bc-220">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="b58bc-220">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b58bc-221">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b58bc-221">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b58bc-222">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="b58bc-222">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b58bc-223">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="b58bc-223">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b58bc-224">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="b58bc-224">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b58bc-225">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="b58bc-225">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b58bc-226">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="b58bc-226">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b58bc-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-229">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="b58bc-229">The name of the terminal.</span></span>

<span data-ttu-id="b58bc-230">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="b58bc-230">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b58bc-231">**UserName**</span><span class="sxs-lookup"><span data-stu-id="b58bc-231">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58bc-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b58bc-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b58bc-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b58bc-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b58bc-234">Credenziali di autenticazione per l'accesso al nome utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b58bc-234">The user's user name logon authentication credential.</span></span> <span data-ttu-id="b58bc-235">Questa proprietà non può contenere più di 20 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b58bc-235">This property cannot be longer than 20 characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b58bc-236">Commenti</span><span class="sxs-lookup"><span data-stu-id="b58bc-236">Remarks</span></span>

<span data-ttu-id="b58bc-237">Tenere presente che WinStations associato alla sessione della console non può accedere ai metodi e alle proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b58bc-237">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="b58bc-238">Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà TerminalName, i metodi di questo oggetto restituiscono **WBEM \_ E \_ non \_ supportati**.</span><span class="sxs-lookup"><span data-stu-id="b58bc-238">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="b58bc-239">Questo codice di errore viene restituito se una stazione della finestra tenta di chiamare i metodi di questo oggetto per aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="b58bc-239">This error code is returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="b58bc-240">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="b58bc-240">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="b58bc-241">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="b58bc-241">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="b58bc-242">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="b58bc-242">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="b58bc-243">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="b58bc-243">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="b58bc-244">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b58bc-244">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b58bc-245">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b58bc-245">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b58bc-246">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b58bc-246">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b58bc-247">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b58bc-247">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b58bc-248">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b58bc-248">Requirements</span></span>



| <span data-ttu-id="b58bc-249">Requisito</span><span class="sxs-lookup"><span data-stu-id="b58bc-249">Requirement</span></span> | <span data-ttu-id="b58bc-250">Valore</span><span class="sxs-lookup"><span data-stu-id="b58bc-250">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b58bc-251">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b58bc-251">Minimum supported client</span></span><br/> | <span data-ttu-id="b58bc-252">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b58bc-252">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b58bc-253">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b58bc-253">Minimum supported server</span></span><br/> | <span data-ttu-id="b58bc-254">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b58bc-254">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b58bc-255">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b58bc-255">Namespace</span></span><br/>                | <span data-ttu-id="b58bc-256">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b58bc-256">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b58bc-257">MOF</span><span class="sxs-lookup"><span data-stu-id="b58bc-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b58bc-258"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b58bc-258"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b58bc-259">DLL</span><span class="sxs-lookup"><span data-stu-id="b58bc-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b58bc-260"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b58bc-260"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b58bc-261">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b58bc-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58bc-262">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="b58bc-262">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="b58bc-263">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="b58bc-263">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

