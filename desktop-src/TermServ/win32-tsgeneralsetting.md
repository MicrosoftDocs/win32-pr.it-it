---
title: Classe Win32_TSGeneralSetting
description: Rappresenta le impostazioni generali del terminale, ad esempio il livello di crittografia e il protocollo di trasporto.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGeneralSetting Servizi Desktop remoto
- Classe Win32_TSGeneralSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741775"
---
# <a name="win32_tsgeneralsetting-class"></a><span data-ttu-id="2c060-105">Win32 \_ TSGeneralSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="2c060-105">Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="2c060-106">La classe WMI **\_ TSGeneralSetting Win32** rappresenta le impostazioni generali del terminale, ad esempio il livello di crittografia e il protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="2c060-106">The **Win32\_TSGeneralSetting** WMI class represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

<span data-ttu-id="2c060-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="2c060-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="2c060-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="2c060-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c060-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c060-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="2c060-110">Members</span><span class="sxs-lookup"><span data-stu-id="2c060-110">Members</span></span>

<span data-ttu-id="2c060-111">La classe **Win32 \_ TSGeneralSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2c060-111">The **Win32\_TSGeneralSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="2c060-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2c060-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2c060-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c060-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2c060-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="2c060-114">Methods</span></span>

<span data-ttu-id="2c060-115">La classe **Win32 \_ TSGeneralSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2c060-115">The **Win32\_TSGeneralSetting** class has these methods.</span></span>



| <span data-ttu-id="2c060-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="2c060-116">Method</span></span>                                                                                        | <span data-ttu-id="2c060-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c060-117">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c060-118">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="2c060-118">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)                       | <span data-ttu-id="2c060-119">Imposta il livello di crittografia.</span><span class="sxs-lookup"><span data-stu-id="2c060-119">Sets the encryption level.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="2c060-120">**SetSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="2c060-120">**SetSecurityLayer**</span></span>](win32-tsgeneralsetting-setsecuritylayer.md)                           | <span data-ttu-id="2c060-121">Imposta il livello di sicurezza su uno dei "livelli di sicurezza RDP" (0), "Negotiate" (1) o "SSL" (2).</span><span class="sxs-lookup"><span data-stu-id="2c060-121">Sets the security layer to one of "RDP Security Layer" (0), "Negotiate" (1), or "SSL" (2).</span></span><br/>                                                                   |
| [<span data-ttu-id="2c060-122">**SetUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="2c060-122">**SetUserAuthenticationRequired**</span></span>](setuserauthenticationrequired-win32-tsgeneralsetting.md) | <span data-ttu-id="2c060-123">Abilita o Disabilita il requisito per cui gli utenti devono essere autenticati al momento della connessione impostando il valore della proprietà **UserAuthenticationRequired** .</span><span class="sxs-lookup"><span data-stu-id="2c060-123">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2c060-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c060-124">Properties</span></span>

<span data-ttu-id="2c060-125">La classe **Win32 \_ TSGeneralSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2c060-125">The **Win32\_TSGeneralSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c060-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2c060-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c060-129">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2c060-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2c060-130">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c060-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="2c060-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c060-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c060-132">**CertificateName**</span><span class="sxs-lookup"><span data-stu-id="2c060-132">**CertificateName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-135">Nome visualizzato per il nome soggetto del certificato personale del computer locale.</span><span class="sxs-lookup"><span data-stu-id="2c060-135">Display name for the local computer personal certificate subject name.</span></span>

</dd> <dt>

<span data-ttu-id="2c060-136">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="2c060-136">**Certificates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-137">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2c060-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2c060-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-139">Contiene un archivio certificati serializzato contenente tutti i certificati dell'archivio **account utente** del computer che sono certificati server validi per l'utilizzo con SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="2c060-139">Contains a serialized certificate store that contains all of the certificates from the **My user account** store on the computer that are valid server certificates for use with secure sockets layer (SSL).</span></span>

</dd> <dt>

<span data-ttu-id="2c060-140">**Commento**</span><span class="sxs-lookup"><span data-stu-id="2c060-140">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2c060-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c060-143">Nome descrittivo della combinazione del protocollo di trasporto e del livello della sessione.</span><span class="sxs-lookup"><span data-stu-id="2c060-143">Descriptive name of the combination of session layer and transport protocol.</span></span>

</dd> <dt>

<span data-ttu-id="2c060-144">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2c060-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-147">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c060-147">Description of the object.</span></span>

<span data-ttu-id="2c060-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c060-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c060-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2c060-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-150">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c060-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c060-152">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="2c060-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2c060-153">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c060-153">The date the object was installed.</span></span> <span data-ttu-id="2c060-154">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="2c060-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2c060-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c060-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c060-156">**MinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="2c060-156">**MinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c060-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c060-159">Qualificatori: **low** ("solo i dati inviati dal client al server sono protetti dalla crittografia in base al livello di attendibilità della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="2c060-159">Qualifiers: **Low** ("Only data sent from client to server is protected by encryption based on server's standard key strength.</span></span> <span data-ttu-id="2c060-160">I dati inviati da server a client non sono protetti. "), **medium** (" tutti i dati inviati tra server e client sono protetti dalla crittografia in base al livello di attendibilità della chiave standard del server "), **alto** (" tutti i dati inviati tra server e client sono protetti con la massima attendibilità della chiave del server in base alla crittografia ").</span><span class="sxs-lookup"><span data-stu-id="2c060-160">Data sent from Server to client is not protected."), **Medium** ("All data sent between Server and client is protected by encryption based on server's standard key strength."), **High** ("All data sent between Server and client is protected by encryption based onserver's maximum key strength.")</span></span>
</dt> </dl>

<span data-ttu-id="2c060-161">Livello di crittografia minimo.</span><span class="sxs-lookup"><span data-stu-id="2c060-161">The minimum encryption level.</span></span>

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="2c060-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bassa** (1)</span><span class="sxs-lookup"><span data-stu-id="2c060-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-163">Basso livello di crittografia.</span><span class="sxs-lookup"><span data-stu-id="2c060-163">Low level of encryption.</span></span> <span data-ttu-id="2c060-164">Solo i dati inviati dal client al server vengono crittografati con la crittografia a 56 bit.</span><span class="sxs-lookup"><span data-stu-id="2c060-164">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="2c060-165">Tenere presente che i dati inviati dal server al client non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="2c060-165">Be aware that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span data-ttu-id="2c060-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Compatibilità media/client** (2)</span><span class="sxs-lookup"><span data-stu-id="2c060-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Medium / Client Compatible** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-167">Livello di crittografia compatibile con il client.</span><span class="sxs-lookup"><span data-stu-id="2c060-167">Client compatible level of encryption.</span></span> <span data-ttu-id="2c060-168">Tutti i dati inviati da client a server e da server a client vengono crittografati al livello di attendibilità massima supportato dal client.</span><span class="sxs-lookup"><span data-stu-id="2c060-168">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="2c060-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (3)</span><span class="sxs-lookup"><span data-stu-id="2c060-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-170">Livello elevato di crittografia.</span><span class="sxs-lookup"><span data-stu-id="2c060-170">High level of encryption.</span></span> <span data-ttu-id="2c060-171">Tutti i dati inviati da client a server e da server a client vengono crittografati con la crittografia a 128 bit avanzata.</span><span class="sxs-lookup"><span data-stu-id="2c060-171">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="2c060-172">I client che non supportano questo livello di crittografia non possono connettersi.</span><span class="sxs-lookup"><span data-stu-id="2c060-172">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span data-ttu-id="2c060-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Conforme allo standard FIPS** (4)</span><span class="sxs-lookup"><span data-stu-id="2c060-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**FIPS Compliant** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-174">Crittografia conforme a FIPS.</span><span class="sxs-lookup"><span data-stu-id="2c060-174">FIPS compliant encryption.</span></span> <span data-ttu-id="2c060-175">Tutti i dati inviati da client a server e da server a client vengono crittografati e decrittografati con gli algoritmi di crittografia Federal Information Processing Standard (FIPS) usando i moduli di crittografia Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2c060-175">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="2c060-176">FIPS è uno standard denominato "requisiti di sicurezza per i moduli di crittografia".</span><span class="sxs-lookup"><span data-stu-id="2c060-176">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="2c060-177">FIPS 140-1 (1994) e FIPS 140-2 (2001) descrivono i requisiti governativi per i moduli di crittografia hardware e software utilizzati all'interno del governo degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="2c060-177">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c060-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2c060-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-181">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c060-181">The name of the object.</span></span>

<span data-ttu-id="2c060-182">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c060-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c060-183">**PolicySourceMinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="2c060-183">**PolicySourceMinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-184">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c060-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-186">Indica se la proprietà **MinEncryptionLevel** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2c060-186">Indicates whether the **MinEncryptionLevel** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="2c060-187">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="2c060-187">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-188">Server</span><span class="sxs-lookup"><span data-stu-id="2c060-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="2c060-189">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="2c060-189">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-190">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2c060-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="2c060-191">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="2c060-191">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-192">Predefinito</span><span class="sxs-lookup"><span data-stu-id="2c060-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c060-193">**PolicySourceSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="2c060-193">**PolicySourceSecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-194">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c060-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-196">Indica se la proprietà **SecurityLayer** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2c060-196">Indicates whether the **SecurityLayer** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="2c060-197">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="2c060-197">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-198">Server</span><span class="sxs-lookup"><span data-stu-id="2c060-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="2c060-199">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="2c060-199">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-200">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2c060-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="2c060-201">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="2c060-201">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-202">Predefinito</span><span class="sxs-lookup"><span data-stu-id="2c060-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c060-203">**PolicySourceUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="2c060-203">**PolicySourceUserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-204">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c060-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-206">Indica se la proprietà **UserAuthenticationRequired** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2c060-206">Indicates whether the **UserAuthenticationRequired** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="2c060-207">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="2c060-207">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-208">Server</span><span class="sxs-lookup"><span data-stu-id="2c060-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="2c060-209">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="2c060-209">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-210">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2c060-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="2c060-211">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="2c060-211">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-212">Predefinito</span><span class="sxs-lookup"><span data-stu-id="2c060-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c060-213">**SecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="2c060-213">**SecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-214">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c060-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c060-216">Qualificatori: **RDPSecurityLayer** ("livello di sicurezza RDP: comunicazione tra serverand il client utilizzerà la crittografia RDP nativa"), **Negotiate** ("il livello più sicuro supportato dal client verrà usato. Se supportato, verrà usato TLS 1,0. "), **SSL** (" SSL (TLS 1,0) verrà usato per l'autenticazione server, oltre a forencrypting tutti i dati trasferiti tra il server e il client. Per questa impostazione è necessario che il server disponga di un certificato compatibile con SSL. "), **NEWTBD** (" nuovo livello di sicurezza in Longhorn ").</span><span class="sxs-lookup"><span data-stu-id="2c060-216">Qualifiers: **RDPSecurityLayer** ("RDP Security Layer: Communication between the serverand the client will use native RDP encryption."), **Negotiate** ("The most secure layer that is supported by the client will be used.If supported, TLS 1.0 will be used."), **SSL** ("SSL (TLS 1.0) will be used for server authentication as well as forencrypting all data transferred between the server and the client.This setting requires the server to have an SSL compatible certificate."), **NEWTBD** ("A NEW SECURITY LAYER in LONGHORN.")</span></span>
</dt> </dl>

<span data-ttu-id="2c060-217">Specifica il livello di sicurezza usato tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="2c060-217">Specifies the security layer used between the client and server.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="2c060-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Livello di protezione RDP** (1)</span><span class="sxs-lookup"><span data-stu-id="2c060-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-219">La comunicazione tra il server e il client utilizza la crittografia RDP nativa.</span><span class="sxs-lookup"><span data-stu-id="2c060-219">Communication between the server and the client uses native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="2c060-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negoziazione** (2)</span><span class="sxs-lookup"><span data-stu-id="2c060-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-221">Viene utilizzato il livello più sicuro supportato dal client.</span><span class="sxs-lookup"><span data-stu-id="2c060-221">The most secure layer that is supported by the client is used.</span></span> <span data-ttu-id="2c060-222">Se supportato, viene usato SSL (TLS 1,0).</span><span class="sxs-lookup"><span data-stu-id="2c060-222">If supported, SSL (TLS 1.0) is used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="2c060-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span><span class="sxs-lookup"><span data-stu-id="2c060-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-224">SSL (TLS 1,0) viene utilizzato per l'autenticazione server e per la crittografia di tutti i dati trasferiti tra il server e il client.</span><span class="sxs-lookup"><span data-stu-id="2c060-224">SSL (TLS 1.0) is used for server authentication and for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="2c060-225">Questa impostazione richiede che il server disponga di un certificato compatibile con SSL.</span><span class="sxs-lookup"><span data-stu-id="2c060-225">This setting requires the server to have an SSL-compatible certificate.</span></span> <span data-ttu-id="2c060-226">Questa impostazione non è compatibile con un valore **MinEncryptionLevel** pari a 1.</span><span class="sxs-lookup"><span data-stu-id="2c060-226">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span data-ttu-id="2c060-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span><span class="sxs-lookup"><span data-stu-id="2c060-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-228">Un nuovo livello di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2c060-228">A new security layer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c060-229">**SSLCertificateSHA1Hash**</span><span class="sxs-lookup"><span data-stu-id="2c060-229">**SSLCertificateSHA1Hash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-231">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2c060-231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c060-232">Specifica l'hash SHA1 in formato esadecimale del certificato SSL per il server di destinazione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="2c060-232">Specifies the SHA1 hash in hexadecimal format of the SSL certificate for the target server to use.</span></span>

<span data-ttu-id="2c060-233">È possibile trovare l'identificazione personale di un certificato tramite lo snap-in MMC certificati della scheda Dettagli della pagina Proprietà certificato.</span><span class="sxs-lookup"><span data-stu-id="2c060-233">The thumbprint of a certificate may be found using the Certificates MMC snap-in on the Details tab of the certificate properties page.</span></span>

</dd> <dt>

<span data-ttu-id="2c060-234">**SSLCertificateSHA1HashType**</span><span class="sxs-lookup"><span data-stu-id="2c060-234">**SSLCertificateSHA1HashType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-235">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c060-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-237">Indica lo stato della proprietà **SSLCertificateSHA1Hash** .</span><span class="sxs-lookup"><span data-stu-id="2c060-237">Indicates the state of the **SSLCertificateSHA1Hash** property.</span></span>

<dt>

<span data-ttu-id="2c060-238">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="2c060-238">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-239">Non valido</span><span class="sxs-lookup"><span data-stu-id="2c060-239">Not valid</span></span>

</dd> <dt>

<span data-ttu-id="2c060-240">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="2c060-240">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-241">Autofirmato predefinito</span><span class="sxs-lookup"><span data-stu-id="2c060-241">Default self-signed</span></span>

</dd> <dt>

<span data-ttu-id="2c060-242">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="2c060-242">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-243">Criteri di gruppo predefiniti applicati</span><span class="sxs-lookup"><span data-stu-id="2c060-243">Default group policy enforced</span></span>

</dd> <dt>

<span data-ttu-id="2c060-244">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="2c060-244">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="2c060-245">Personalizzato</span><span class="sxs-lookup"><span data-stu-id="2c060-245">Custom</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c060-246">**Status**</span><span class="sxs-lookup"><span data-stu-id="2c060-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c060-249">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="2c060-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="2c060-250">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c060-250">Current status of the object.</span></span> <span data-ttu-id="2c060-251">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="2c060-251">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2c060-252">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="2c060-252">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2c060-253">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="2c060-253">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2c060-254">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="2c060-254">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2c060-255">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="2c060-255">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2c060-256">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c060-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="2c060-257">("OK")</span><span class="sxs-lookup"><span data-stu-id="2c060-257">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c060-258">("Errore")</span><span class="sxs-lookup"><span data-stu-id="2c060-258">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c060-259">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="2c060-259">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c060-260">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="2c060-260">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c060-261">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="2c060-261">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c060-262">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="2c060-262">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c060-263">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="2c060-263">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c060-264">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="2c060-264">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c060-265">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="2c060-265">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-266">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-268">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="2c060-268">The name of the terminal.</span></span>

<span data-ttu-id="2c060-269">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="2c060-269">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c060-270">**TerminalProtocol**</span><span class="sxs-lookup"><span data-stu-id="2c060-270">**TerminalProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-271">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-273">Nome del protocollo di livello sessione. ad esempio, Microsoft RDP 5,0.</span><span class="sxs-lookup"><span data-stu-id="2c060-273">The name of the session layer protocol; for example, Microsoft RDP 5.0.</span></span>

</dd> <dt>

<span data-ttu-id="2c060-274">**Trasporto**</span><span class="sxs-lookup"><span data-stu-id="2c060-274">**Transport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-275">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2c060-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-277">Tipo di trasporto utilizzato nella connessione. ad esempio TCP, NetBIOS o IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="2c060-277">The type of transport used in the connection; for example, TCP, NetBIOS, or IPX/SPX.</span></span>

</dd> <dt>

<span data-ttu-id="2c060-278">**UserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="2c060-278">**UserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-279">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c060-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c060-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c060-281">Specifica il tipo di autenticazione utente utilizzato per le connessioni remote.</span><span class="sxs-lookup"><span data-stu-id="2c060-281">Specifies the type of user authentication used for remote connections.</span></span> <span data-ttu-id="2c060-282">Se impostato su 1, ovvero abilitato, **UserAuthenticationRequired** richiede l'autenticazione dell'utente in fase di connessione per aumentare la protezione del server contro gli attacchi alla rete.</span><span class="sxs-lookup"><span data-stu-id="2c060-282">If set to 1, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="2c060-283">Solo i client [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) che supportano la versione 6,0 o successiva di RDP sono in grado di connettersi.</span><span class="sxs-lookup"><span data-stu-id="2c060-283">Only [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="2c060-284">Per evitare le rotture per gli utenti remoti, è consigliabile distribuire i client RDP che supportano la versione del protocollo appropriata prima di abilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="2c060-284">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

<span data-ttu-id="2c060-285">Usare il metodo [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) per abilitare o disabilitare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2c060-285">Use the [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) method to enable or disable this property.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="2c060-286"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="2c060-286"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-287">L'autenticazione utente alla connessione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="2c060-287">User authentication at connection is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="2c060-288"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="2c060-288"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-289">L'autenticazione utente alla connessione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2c060-289">User authentication at connection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c060-290">**WindowsAuthentication**</span><span class="sxs-lookup"><span data-stu-id="2c060-290">**WindowsAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c060-291">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c060-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c060-292">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2c060-292">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2c060-293">Specifica se per la connessione viene utilizzato per impostazione predefinita il processo di autenticazione standard di Windows o un altro pacchetto di autenticazione installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2c060-293">Specifies whether the connection defaults to the standard Windows authentication process or to another authentication package that has been installed on the system.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="2c060-294"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="2c060-294"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-295">Per impostazione predefinita, non è il processo di autenticazione standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="2c060-295">Does not default to the standard Windows authentication process.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="2c060-296"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="2c060-296"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2c060-297">Il valore predefinito è il processo di autenticazione standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="2c060-297">Defaults to the standard Windows authentication process.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c060-298">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c060-298">Remarks</span></span>

<span data-ttu-id="2c060-299">Tenere presente che le stazioni della finestra non associate alla sessione della console non possono accedere ai metodi e alle proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="2c060-299">Be aware that window stations not associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="2c060-300">Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà TerminalName, i metodi di questo oggetto restituiranno **WBEM \_ E \_ non \_ supportati**.</span><span class="sxs-lookup"><span data-stu-id="2c060-300">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="2c060-301">Questo codice di errore viene restituito anche se una stazione della finestra tenta di chiamare i metodi di questo oggetto allo scopo di aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="2c060-301">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="2c060-302">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="2c060-302">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="2c060-303">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="2c060-303">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="2c060-304">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="2c060-304">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="2c060-305">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="2c060-305">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="2c060-306">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2c060-306">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2c060-307">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="2c060-307">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2c060-308">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="2c060-308">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2c060-309">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2c060-309">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c060-310">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c060-310">Requirements</span></span>



| <span data-ttu-id="2c060-311">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c060-311">Requirement</span></span> | <span data-ttu-id="2c060-312">Valore</span><span class="sxs-lookup"><span data-stu-id="2c060-312">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c060-313">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c060-313">Minimum supported client</span></span><br/> | <span data-ttu-id="2c060-314">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c060-314">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c060-315">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c060-315">Minimum supported server</span></span><br/> | <span data-ttu-id="2c060-316">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c060-316">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c060-317">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2c060-317">Namespace</span></span><br/>                | <span data-ttu-id="2c060-318">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2c060-318">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2c060-319">MOF</span><span class="sxs-lookup"><span data-stu-id="2c060-319">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c060-320"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c060-320"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c060-321">DLL</span><span class="sxs-lookup"><span data-stu-id="2c060-321">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c060-322"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c060-322"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c060-323">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c060-323">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c060-324">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="2c060-324">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

