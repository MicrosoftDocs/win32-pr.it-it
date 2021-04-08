---
title: Classe Win32_SessionBrokerFarmAccount
description: La \_ classe Win32 SessionBrokerFarmAccount non è più disponibile per l'uso in Windows Server 2012. | Classe Win32_SessionBrokerFarmAccount
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionBrokerFarmAccount Servizi Desktop remoto
- Classe Win32_SessionBrokerFarmAccount Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761849"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="b2268-106">Win32 \_ SessionBrokerFarmAccount (classe)</span><span class="sxs-lookup"><span data-stu-id="b2268-106">Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="b2268-107">\[La classe **Win32 \_ SessionBrokerFarmAccount** non è più disponibile per l'uso in Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="b2268-107">\[The **Win32\_SessionBrokerFarmAccount** class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="b2268-108">Definisce un account farm Broker di sessione.</span><span class="sxs-lookup"><span data-stu-id="b2268-108">Defines a session broker farm account.</span></span>

<span data-ttu-id="b2268-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b2268-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2268-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2268-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a><span data-ttu-id="b2268-111">Members</span><span class="sxs-lookup"><span data-stu-id="b2268-111">Members</span></span>

<span data-ttu-id="b2268-112">La classe **Win32 \_ SessionBrokerFarmAccount** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b2268-112">The **Win32\_SessionBrokerFarmAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="b2268-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b2268-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="b2268-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2268-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b2268-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="b2268-115">Methods</span></span>

<span data-ttu-id="b2268-116">La classe **Win32 \_ SessionBrokerFarmAccount** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b2268-116">The **Win32\_SessionBrokerFarmAccount** class has these methods.</span></span>



| <span data-ttu-id="b2268-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="b2268-117">Method</span></span>                                                      | <span data-ttu-id="b2268-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2268-118">Description</span></span>                          |
|:------------------------------------------------------------|:-------------------------------------|
| [<span data-ttu-id="b2268-119">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="b2268-119">**DeleteEx**</span></span>](deleteex-win32-sessionbrokerfarmaccount.md) | <span data-ttu-id="b2268-120">Elimina l'account farm.</span><span class="sxs-lookup"><span data-stu-id="b2268-120">Deletes the farm account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b2268-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2268-121">Properties</span></span>

<span data-ttu-id="b2268-122">La classe **Win32 \_ SessionBrokerFarmAccount** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2268-122">The **Win32\_SessionBrokerFarmAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2268-123">**AccountDomain**</span><span class="sxs-lookup"><span data-stu-id="b2268-123">**AccountDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2268-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2268-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2268-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2268-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b2268-126">Nome del dominio a cui appartiene l'account farm.</span><span class="sxs-lookup"><span data-stu-id="b2268-126">The name of the domain the farm account belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="b2268-127">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="b2268-127">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2268-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2268-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2268-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2268-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b2268-130">Nome dell'account farm.</span><span class="sxs-lookup"><span data-stu-id="b2268-130">The name of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="b2268-131">**AccountPassword**</span><span class="sxs-lookup"><span data-stu-id="b2268-131">**AccountPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2268-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2268-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2268-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2268-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b2268-134">Password dell'account farm.</span><span class="sxs-lookup"><span data-stu-id="b2268-134">The password of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="b2268-135">**AccountSPN1**</span><span class="sxs-lookup"><span data-stu-id="b2268-135">**AccountSPN1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2268-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2268-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2268-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2268-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2268-138">Primo nome dell'entità servizio (SPN) associato all'account farm.</span><span class="sxs-lookup"><span data-stu-id="b2268-138">The first service principal name (SPN) associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="b2268-139">**AccountSPN2**</span><span class="sxs-lookup"><span data-stu-id="b2268-139">**AccountSPN2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2268-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2268-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2268-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2268-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2268-142">Secondo SPN associato all'account della farm.</span><span class="sxs-lookup"><span data-stu-id="b2268-142">The second SPN associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="b2268-143">**ComputerDNSName**</span><span class="sxs-lookup"><span data-stu-id="b2268-143">**ComputerDNSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2268-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2268-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2268-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2268-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b2268-146">Nome DNS del computer associato all'account della farm.</span><span class="sxs-lookup"><span data-stu-id="b2268-146">The DNS name of the computer associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="b2268-147">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="b2268-147">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2268-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2268-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2268-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2268-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2268-150">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2268-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2268-151">Nome della farm di broker di sessione.</span><span class="sxs-lookup"><span data-stu-id="b2268-151">The name of the session broker farm.</span></span>

</dd> <dt>

<span data-ttu-id="b2268-152">**Manuale**</span><span class="sxs-lookup"><span data-stu-id="b2268-152">**Manual**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2268-153">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2268-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2268-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2268-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b2268-155">Indica se la password per l'account viene aggiornata manualmente.</span><span class="sxs-lookup"><span data-stu-id="b2268-155">Indicates if the password for the account is updated manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2268-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2268-156">Requirements</span></span>



| <span data-ttu-id="b2268-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2268-157">Requirement</span></span> | <span data-ttu-id="b2268-158">Valore</span><span class="sxs-lookup"><span data-stu-id="b2268-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2268-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2268-159">Minimum supported client</span></span><br/> | <span data-ttu-id="b2268-160">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b2268-160">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b2268-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2268-161">Minimum supported server</span></span><br/> | <span data-ttu-id="b2268-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2268-162">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b2268-163">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b2268-163">End of client support</span></span><br/>    | <span data-ttu-id="b2268-164">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b2268-164">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b2268-165">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b2268-165">End of server support</span></span><br/>    | <span data-ttu-id="b2268-166">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2268-166">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b2268-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2268-167">Namespace</span></span><br/>                | <span data-ttu-id="b2268-168">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b2268-168">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="b2268-169">MOF</span><span class="sxs-lookup"><span data-stu-id="b2268-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2268-170"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2268-170"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2268-171">DLL</span><span class="sxs-lookup"><span data-stu-id="b2268-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2268-172"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2268-172"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

