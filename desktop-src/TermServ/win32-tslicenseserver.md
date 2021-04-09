---
title: Classe Win32_TSLicenseServer
description: Fornisce metodi e proprietà per visualizzare e Desktop remoto configurare licenze Desktop remoto in un server licenze Desktop remoto.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseServer Servizi Desktop remoto
- Classe Win32_TSLicenseServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964498"
---
# <a name="win32_tslicenseserver-class"></a><span data-ttu-id="9429b-105">Win32 \_ TSLicenseServer (classe)</span><span class="sxs-lookup"><span data-stu-id="9429b-105">Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="9429b-106">Fornisce metodi e proprietà per visualizzare e Desktop remoto configurare licenze Desktop remoto in un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-106">Provides methods and properties to view and configure Remote Desktop Licensing (RD Licensing) on a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9429b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9429b-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a><span data-ttu-id="9429b-108">Members</span><span class="sxs-lookup"><span data-stu-id="9429b-108">Members</span></span>

<span data-ttu-id="9429b-109">La classe **Win32 \_ TSLicenseServer** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9429b-109">The **Win32\_TSLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="9429b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="9429b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9429b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9429b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9429b-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="9429b-112">Methods</span></span>

<span data-ttu-id="9429b-113">La classe **Win32 \_ TSLicenseServer** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9429b-113">The **Win32\_TSLicenseServer** class has these methods.</span></span>



| <span data-ttu-id="9429b-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="9429b-114">Method</span></span>                                                                                   | <span data-ttu-id="9429b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9429b-115">Description</span></span>                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9429b-116">**ActivateServer**</span><span class="sxs-lookup"><span data-stu-id="9429b-116">**ActivateServer**</span></span>](activateserver-win32-tslicenseserver.md)                           | <span data-ttu-id="9429b-117">Attiva il server licenze Desktop remoto usando un ID del server licenze Desktop remoto ottenuto sul telefono o su Internet.</span><span class="sxs-lookup"><span data-stu-id="9429b-117">Activates the Remote Desktop license server by using a Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                           |
| [<span data-ttu-id="9429b-118">**ActivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="9429b-118">**ActivateServerAutomatic**</span></span>](activateserverautomatic-win32-tslicenseserver.md)         | <span data-ttu-id="9429b-119">Attiva automaticamente il server licenze Desktop remoto tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="9429b-119">Activates the Remote Desktop license server automatically over the Internet.</span></span> <span data-ttu-id="9429b-120">Le proprietà **FirstName**, **LastName**, **Company** e **CountryRegion** non devono essere vuote quando viene chiamato questo metodo oppure il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9429b-120">The **FirstName**, **LastName**, **Company**, and **CountryRegion** properties must not be empty when this method is called, or the method will fail.</span></span><br/> |
| [<span data-ttu-id="9429b-121">**AddLStoTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="9429b-121">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)                       | <span data-ttu-id="9429b-122">Aggiunge il server licenze Desktop remoto al gruppo server licenze Desktop remoto in un controller di dominio nello stesso dominio del server licenze.</span><span class="sxs-lookup"><span data-stu-id="9429b-122">Adds the Remote Desktop license server to the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                                |
| [<span data-ttu-id="9429b-123">**ChangeRole**</span><span class="sxs-lookup"><span data-stu-id="9429b-123">**ChangeRole**</span></span>](changerole-win32-tslicenseserver.md)                                   | <span data-ttu-id="9429b-124">Modifica l'ambito di individuazione del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-124">Changes the discovery scope of the Remote Desktop license server.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="9429b-125">**CreateTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="9429b-125">**CreateTSCGroup**</span></span>](createtscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="9429b-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="9429b-126">This method is not supported.</span></span><br/> <span data-ttu-id="9429b-127">**Windows server 2008 R2 e Windows server 2008:** Consente di creare il gruppo locale computer Terminal Server nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-127">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                               |
| [<span data-ttu-id="9429b-128">**DeactivateServer**</span><span class="sxs-lookup"><span data-stu-id="9429b-128">**DeactivateServer**</span></span>](deactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="9429b-129">Disattiva il server licenze Desktop remoto utilizzando un codice di conferma ricevuto tramite telefono.</span><span class="sxs-lookup"><span data-stu-id="9429b-129">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="9429b-130">**DeactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="9429b-130">**DeactivateServerAutomatic**</span></span>](deactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="9429b-131">Disattiva il server licenze Desktop remoto tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="9429b-131">Deactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="9429b-132">Le proprietà **FirstName** e **LastName** non devono essere vuote quando viene chiamato questo metodo, altrimenti il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9429b-132">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="9429b-133">**GetActivationStatus**</span><span class="sxs-lookup"><span data-stu-id="9429b-133">**GetActivationStatus**</span></span>](getactivationstatus-win32-tslicenseserver.md)                 | <span data-ttu-id="9429b-134">Recupera lo stato di attivazione corrente.</span><span class="sxs-lookup"><span data-stu-id="9429b-134">Retrieves the current activation status.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="9429b-135">**GetLicenseServerId**</span><span class="sxs-lookup"><span data-stu-id="9429b-135">**GetLicenseServerId**</span></span>](getlicenseserverid-win32-tslicenseserver.md)                   | <span data-ttu-id="9429b-136">Recupera un ID del server licenze Desktop remoto se il server è attualmente attivato.</span><span class="sxs-lookup"><span data-stu-id="9429b-136">Retrieves a Remote Desktop license server ID if the server is currently activated.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="9429b-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="9429b-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)                         | <span data-ttu-id="9429b-138">Recupera un valore che indica se il server licenze Desktop remoto è un membro del gruppo server licenze Desktop remoto in un controller di dominio in un determinato dominio.</span><span class="sxs-lookup"><span data-stu-id="9429b-138">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop License Servers group on a domain controller in a given domain.</span></span><br/>                                                                              |
| [<span data-ttu-id="9429b-139">**IsLSonDC**</span><span class="sxs-lookup"><span data-stu-id="9429b-139">**IsLSonDC**</span></span>](islsondc-win32-tslicenseserver.md)                                       | <span data-ttu-id="9429b-140">Recupera un valore che indica se le licenze Desktop remoto sono installate in un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="9429b-140">Retrieves whether RD Licensing is installed on a domain controller.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="9429b-141">**IsLSPreventUpgradeGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="9429b-141">**IsLSPreventUpgradeGPEnabled**</span></span>](islspreventupgradegpenabled-win32-tslicenseserver.md) | <span data-ttu-id="9429b-142">Recupera un valore che indica se l'impostazione di criteri di gruppo "Impedisci aggiornamento licenza" è abilitata nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-142">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="9429b-143">**IsLSPublished**</span><span class="sxs-lookup"><span data-stu-id="9429b-143">**IsLSPublished**</span></span>](islspublished-win32-tslicenseserver.md)                             | <span data-ttu-id="9429b-144">Recupera un valore che indica se il server licenze Desktop remoto è pubblicato in Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="9429b-144">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="9429b-145">**IsLSRegisteredToSCP**</span><span class="sxs-lookup"><span data-stu-id="9429b-145">**IsLSRegisteredToSCP**</span></span>](win32-tslicenseserver-islsregisteredtoscp.md)                 | <span data-ttu-id="9429b-146">Recupera un valore che indica se il server licenze Desktop remoto viene registrato come punto di connessione del servizio nel Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9429b-146">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                               |
| [<span data-ttu-id="9429b-147">**IsLSSecGrpGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="9429b-147">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)                 | <span data-ttu-id="9429b-148">Recupera un valore che indica se l'impostazione di criteri di gruppo "gruppo di sicurezza del server licenze" è abilitata nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-148">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="9429b-149">**IsSecureAccessAllowed**</span><span class="sxs-lookup"><span data-stu-id="9429b-149">**IsSecureAccessAllowed**</span></span>](issecureaccessallowed-win32-tslicenseserver.md)             | <span data-ttu-id="9429b-150">Recupera un valore che indica se un server Host sessione Desktop remoto è autorizzato a richiedere Servizi Desktop remoto licenze CAL (Client Access License) del server licenze di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-150">Retrieves whether an RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span><br/>                                                                |
| [<span data-ttu-id="9429b-151">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="9429b-151">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)                     | <span data-ttu-id="9429b-152">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="9429b-152">This method is not supported.</span></span><br/> <span data-ttu-id="9429b-153">**Windows server 2008 R2 e Windows server 2008:** Recupera un valore che indica se il gruppo locale computer Terminal Server esiste nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-153">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span><br/>                              |
| [<span data-ttu-id="9429b-154">**IsTSinTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="9429b-154">**IsTSinTSCGroup**</span></span>](istsintscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="9429b-155">Recupera un valore che indica se un server Host sessione Desktop remoto è un membro del gruppo locale computer Terminal Server nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-155">Retrieves whether an RD Session Host server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="9429b-156">**PublishLS**</span><span class="sxs-lookup"><span data-stu-id="9429b-156">**PublishLS**</span></span>](publishls-win32-tslicenseserver.md)                                     | <span data-ttu-id="9429b-157">Pubblica il server licenze Desktop remoto in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9429b-157">Publishes the Remote Desktop license server in AD DS.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="9429b-158">**ReactivateServer**</span><span class="sxs-lookup"><span data-stu-id="9429b-158">**ReactivateServer**</span></span>](reactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="9429b-159">Riattiva il server licenze Desktop remoto utilizzando un nuovo ID server licenze Desktop remoto ottenuto tramite telefono o Internet.</span><span class="sxs-lookup"><span data-stu-id="9429b-159">Reactivates the Remote Desktop license server by using a new Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                     |
| [<span data-ttu-id="9429b-160">**ReactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="9429b-160">**ReactivateServerAutomatic**</span></span>](reactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="9429b-161">Riattiva il server licenze Desktop remoto tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="9429b-161">Reactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="9429b-162">Le proprietà **FirstName** e **LastName** non devono essere vuote quando viene chiamato questo metodo, altrimenti il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9429b-162">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="9429b-163">**RegisterLSToSCP**</span><span class="sxs-lookup"><span data-stu-id="9429b-163">**RegisterLSToSCP**</span></span>](win32-tslicenseserver-registerlstoscp.md)                         | <span data-ttu-id="9429b-164">Registra il server licenze Desktop remoto come punto di connessione del servizio in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9429b-164">Registers the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="9429b-165">**RemoveLSfromTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="9429b-165">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)             | <span data-ttu-id="9429b-166">Rimuove il server licenze Desktop remoto dal gruppo server licenze Desktop remoto in un controller di dominio nello stesso dominio del server licenze.</span><span class="sxs-lookup"><span data-stu-id="9429b-166">Removes the Remote Desktop license server from the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                           |
| [<span data-ttu-id="9429b-167">**RemoveTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="9429b-167">**RemoveTSCGroup**</span></span>](removetscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="9429b-168">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="9429b-168">This method is not supported.</span></span><br/> <span data-ttu-id="9429b-169">**Windows server 2008 R2 e Windows server 2008:** Rimuove il gruppo locale computer Terminal Server dal server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-169">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span><br/>                                             |
| [<span data-ttu-id="9429b-170">**UnpublishLS**</span><span class="sxs-lookup"><span data-stu-id="9429b-170">**UnpublishLS**</span></span>](unpublishls-win32-tslicenseserver.md)                                 | <span data-ttu-id="9429b-171">Annulla la pubblicazione di un server licenze Desktop remoto da servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9429b-171">Unpublishes a Remote Desktop license server from AD DS.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="9429b-172">**UnRegisterLSFromSCP**</span><span class="sxs-lookup"><span data-stu-id="9429b-172">**UnRegisterLSFromSCP**</span></span>](win32-tslicenseserver-unregisterlsfromscp.md)                 | <span data-ttu-id="9429b-173">Rimuove il server licenze Desktop remoto come punto di connessione del servizio in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9429b-173">Removes the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="9429b-174">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9429b-174">Properties</span></span>

<span data-ttu-id="9429b-175">La classe **Win32 \_ TSLicenseServer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9429b-175">The **Win32\_TSLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9429b-176">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="9429b-176">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-179">Via indirizzo del contatto per licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-179">Street address of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-180">Questa proprietà viene utilizzata quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-180">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="9429b-181">Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .</span><span class="sxs-lookup"><span data-stu-id="9429b-181">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="9429b-182">**Città**</span><span class="sxs-lookup"><span data-stu-id="9429b-182">**City**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-185">Città del contatto per licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-185">City of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-186">Questa proprietà viene utilizzata quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-186">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="9429b-187">Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .</span><span class="sxs-lookup"><span data-stu-id="9429b-187">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="9429b-188">**Company**</span><span class="sxs-lookup"><span data-stu-id="9429b-188">**Company**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-191">Società del contatto per licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-191">Company of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-192">Questa proprietà viene utilizzata (e obbligatoria) quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-192">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="9429b-193">**CountryRegion**</span><span class="sxs-lookup"><span data-stu-id="9429b-193">**CountryRegion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-195">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-195">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-196">Paese/area geografica del contatto per licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-196">Country/region of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-197">Questa proprietà viene utilizzata (e obbligatoria) quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-197">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="9429b-198">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="9429b-198">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9429b-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9429b-201">Percorso del database di gestione licenze Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-201">Path of the RDS Licensing database.</span></span>

</dd> <dt>

<span data-ttu-id="9429b-202">**Posta elettronica**</span><span class="sxs-lookup"><span data-stu-id="9429b-202">**eMail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-204">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-204">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-205">Indirizzo di posta elettronica del contatto per licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-205">Email address of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-206">Questa proprietà viene utilizzata quando vengono chiamati i metodi [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-206">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span> <span data-ttu-id="9429b-207">Questa proprietà è facoltativa per le chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="9429b-207">(This property is optional for these method calls.)</span></span>

</dd> <dt>

<span data-ttu-id="9429b-208">**FirstName**</span><span class="sxs-lookup"><span data-stu-id="9429b-208">**FirstName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-210">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-211">Nome del contatto per licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-211">First name of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-212">Questa proprietà viene utilizzata (e obbligatoria) quando vengono chiamati i metodi [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-212">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="9429b-213">**LastName**</span><span class="sxs-lookup"><span data-stu-id="9429b-213">**LastName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-215">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-215">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-216">Cognome del contatto per le licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-216">Last name of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-217">Questa proprietà viene utilizzata (e obbligatoria) quando vengono chiamati i metodi [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-217">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="9429b-218">**OrgUnit**</span><span class="sxs-lookup"><span data-stu-id="9429b-218">**OrgUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-221">Unità organizzativa del contatto per licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-221">Organizational unit of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-222">Questa proprietà viene utilizzata quando viene chiamato [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-222">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) is called.</span></span> <span data-ttu-id="9429b-223">Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .</span><span class="sxs-lookup"><span data-stu-id="9429b-223">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="9429b-224">**PostalCode**</span><span class="sxs-lookup"><span data-stu-id="9429b-224">**PostalCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-227">Cap del contatto per licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-227">Postal code of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-228">Questa proprietà viene utilizzata quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-228">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="9429b-229">Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .</span><span class="sxs-lookup"><span data-stu-id="9429b-229">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="9429b-230">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="9429b-230">**ProductId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9429b-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9429b-233">ID prodotto del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-233">Product ID of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="9429b-234">**ServerRole**</span><span class="sxs-lookup"><span data-stu-id="9429b-234">**ServerRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-235">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9429b-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9429b-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9429b-237">Descrive l'ambito di gestione licenze per il server licenze Desktop remoto all'interno dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="9429b-237">Describes the licensing scope for the Remote Desktop license server within the organization.</span></span>

<dt>

<span data-ttu-id="9429b-238">0</span><span class="sxs-lookup"><span data-stu-id="9429b-238">0</span></span>
</dt> <dd>

<span data-ttu-id="9429b-239">I server Host sessione Desktop remoto nello stesso gruppo di lavoro possono individuare il server licenze.</span><span class="sxs-lookup"><span data-stu-id="9429b-239">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="9429b-240">1</span><span class="sxs-lookup"><span data-stu-id="9429b-240">1</span></span>
</dt> <dd>

<span data-ttu-id="9429b-241">I server Host sessione Desktop remoto nello stesso dominio possono individuare il server licenze.</span><span class="sxs-lookup"><span data-stu-id="9429b-241">RD Session Host servers in the same domain can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="9429b-242">2</span><span class="sxs-lookup"><span data-stu-id="9429b-242">2</span></span>
</dt> <dd>

<span data-ttu-id="9429b-243">I server Host sessione Desktop remoto da più domini nella stessa foresta possono individuare il server licenze.</span><span class="sxs-lookup"><span data-stu-id="9429b-243">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9429b-244">**State**</span><span class="sxs-lookup"><span data-stu-id="9429b-244">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-245">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-246">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9429b-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9429b-247">Stato del contatto per licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-247">State of the contact for RD Licensing.</span></span> <span data-ttu-id="9429b-248">Questa proprietà viene utilizzata quando viene chiamato il metodo [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="9429b-248">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="9429b-249">Questa proprietà è facoltativa quando si usa il metodo **ActivateServerAutomatic** .</span><span class="sxs-lookup"><span data-stu-id="9429b-249">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="9429b-250">**Versione**</span><span class="sxs-lookup"><span data-stu-id="9429b-250">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9429b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9429b-253">Versione del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-253">Version of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="9429b-254">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="9429b-254">**VersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9429b-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9429b-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9429b-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9429b-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9429b-257">Numero di versione del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9429b-257">Version number of the Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9429b-258">Commenti</span><span class="sxs-lookup"><span data-stu-id="9429b-258">Remarks</span></span>

<span data-ttu-id="9429b-259">Questa classe è una classe [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) e può avere una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="9429b-259">This class is a [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) class and can have only one instance.</span></span> <span data-ttu-id="9429b-260">Tutti i metodi contenuti in questa classe sono statici.</span><span class="sxs-lookup"><span data-stu-id="9429b-260">All of the methods contained within this class are static.</span></span>

<span data-ttu-id="9429b-261">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="9429b-261">You must be a member of the Administrators group to use this class.</span></span> <span data-ttu-id="9429b-262">Se il chiamante non è un membro del gruppo Administrators, le proprietà restituite saranno vuote.</span><span class="sxs-lookup"><span data-stu-id="9429b-262">If the caller is not a member of the Administrators group, the properties returned will be empty.</span></span>

<span data-ttu-id="9429b-263">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9429b-263">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9429b-264">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9429b-264">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9429b-265">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="9429b-265">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9429b-266">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9429b-266">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9429b-267">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9429b-267">Requirements</span></span>



| <span data-ttu-id="9429b-268">Requisito</span><span class="sxs-lookup"><span data-stu-id="9429b-268">Requirement</span></span> | <span data-ttu-id="9429b-269">Valore</span><span class="sxs-lookup"><span data-stu-id="9429b-269">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9429b-270">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9429b-270">Minimum supported client</span></span><br/> | <span data-ttu-id="9429b-271">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9429b-271">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9429b-272">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9429b-272">Minimum supported server</span></span><br/> | <span data-ttu-id="9429b-273">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9429b-273">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9429b-274">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9429b-274">Namespace</span></span><br/>                | <span data-ttu-id="9429b-275">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9429b-275">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="9429b-276">MOF</span><span class="sxs-lookup"><span data-stu-id="9429b-276">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9429b-277"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9429b-277"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9429b-278">DLL</span><span class="sxs-lookup"><span data-stu-id="9429b-278">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9429b-279"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9429b-279"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9429b-280">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9429b-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9429b-281">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="9429b-281">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="9429b-282">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="9429b-282">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="9429b-283">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="9429b-283">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="9429b-284">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="9429b-284">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

