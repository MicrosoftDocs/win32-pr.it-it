---
description: Rappresenta le impostazioni per i Servizi terminal del computer virtuale in un host.
ms.assetid: 1f8d0718-09da-4231-95eb-cc63b6f324dd
title: Classe Msvm_TerminalServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalServiceSettingData
- Msvm_TerminalServiceSettingData.InstanceID
- Msvm_TerminalServiceSettingData.Caption
- Msvm_TerminalServiceSettingData.Description
- Msvm_TerminalServiceSettingData.ElementName
- Msvm_TerminalServiceSettingData.ListenerPort
- Msvm_TerminalServiceSettingData.DisableSelfSignedCertificateGeneration
- Msvm_TerminalServiceSettingData.AuthCertificateHash
- Msvm_TerminalServiceSettingData.TrustedIssuerCertificateHashes
- Msvm_TerminalServiceSettingData.AllowedHashAlgorithms
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27d98971c847eab5042823e8a1524051a15fd679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753559"
---
# <a name="msvm_terminalservicesettingdata-class"></a><span data-ttu-id="23d24-103">\_Classe MSVM TerminalServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="23d24-103">Msvm\_TerminalServiceSettingData class</span></span>

<span data-ttu-id="23d24-104">Rappresenta le impostazioni per i Servizi terminal del computer virtuale in un host.</span><span class="sxs-lookup"><span data-stu-id="23d24-104">Represents the settings for the virtual computer terminal services on a host.</span></span> <span data-ttu-id="23d24-105">Non è possibile modificare direttamente le proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="23d24-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="23d24-106">Il client deve chiamare il metodo [**MSVM \_ TerminalService. ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) per modificare una di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="23d24-106">The client must call the [**Msvm\_TerminalService.ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="23d24-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="23d24-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23d24-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23d24-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Hyper-V Terminal Service Settings";
  string  Description = "Settings for the Hyper-V Terminal Service";
  string  ElementName = "Hyper-V Terminal Service Settings";
  uint32  ListenerPort;
  boolean DisableSelfSignedCertificateGeneration;
  uint8   AuthCertificateHash[];
  string  TrustedIssuerCertificateHashes[];
  string  AllowedHashAlgorithms[];
};
```

## <a name="members"></a><span data-ttu-id="23d24-109">Members</span><span class="sxs-lookup"><span data-stu-id="23d24-109">Members</span></span>

<span data-ttu-id="23d24-110">La **classe \_ TerminalServiceSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="23d24-110">The **Msvm\_TerminalServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="23d24-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23d24-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23d24-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23d24-112">Properties</span></span>

<span data-ttu-id="23d24-113">La **classe \_ TerminalServiceSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="23d24-113">The **Msvm\_TerminalServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23d24-114">**AllowedHashAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="23d24-114">**AllowedHashAlgorithms**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d24-115">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="23d24-115">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23d24-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23d24-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23d24-117">Elenco di algoritmi hash accettati per verificare la firma dei token di autenticazione federati.</span><span class="sxs-lookup"><span data-stu-id="23d24-117">The list of hash algorithms accepted for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="23d24-118">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="23d24-118">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="23d24-119">**AuthCertificateHash**</span><span class="sxs-lookup"><span data-stu-id="23d24-119">**AuthCertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d24-120">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="23d24-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="23d24-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23d24-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23d24-122">Hash del certificato da utilizzare per l'autenticazione remota.</span><span class="sxs-lookup"><span data-stu-id="23d24-122">The hash of the certificate to use for remote authentication.</span></span>

</dd> <dt>

<span data-ttu-id="23d24-123">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="23d24-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d24-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23d24-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23d24-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23d24-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23d24-126">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23d24-126">A short description of the object.</span></span> <span data-ttu-id="23d24-127">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23d24-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23d24-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="23d24-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d24-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23d24-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23d24-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23d24-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23d24-131">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="23d24-131">A description of the object.</span></span> <span data-ttu-id="23d24-132">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23d24-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23d24-133">**DisableSelfSignedCertificateGeneration**</span><span class="sxs-lookup"><span data-stu-id="23d24-133">**DisableSelfSignedCertificateGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d24-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23d24-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23d24-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23d24-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23d24-136">Disabilita la generazione di certificati autofirmati.</span><span class="sxs-lookup"><span data-stu-id="23d24-136">Disables self-signed certificate generation.</span></span>

</dd> <dt>

<span data-ttu-id="23d24-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="23d24-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d24-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23d24-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23d24-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23d24-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23d24-140">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23d24-140">A display name for the object.</span></span> <span data-ttu-id="23d24-141">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23d24-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23d24-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="23d24-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d24-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23d24-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23d24-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23d24-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23d24-145">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="23d24-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="23d24-146">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="23d24-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="23d24-147">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="23d24-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23d24-148">**ListenerPort**</span><span class="sxs-lookup"><span data-stu-id="23d24-148">**ListenerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d24-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23d24-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23d24-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23d24-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23d24-151">Porta di rete in cui verrà effettuata la connessione alla sessione remota iniziale.</span><span class="sxs-lookup"><span data-stu-id="23d24-151">The network port on which the initial remote session connection will be made.</span></span>

</dd> <dt>

<span data-ttu-id="23d24-152">**TrustedIssuerCertificateHashes**</span><span class="sxs-lookup"><span data-stu-id="23d24-152">**TrustedIssuerCertificateHashes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23d24-153">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="23d24-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23d24-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23d24-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23d24-155">Elenco di hash del certificato dell'autorità emittente attendibile per la verifica della firma dei token di autenticazione federati.</span><span class="sxs-lookup"><span data-stu-id="23d24-155">The list of trusted issuer certificate hashes for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="23d24-156">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="23d24-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23d24-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23d24-157">Requirements</span></span>



| <span data-ttu-id="23d24-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="23d24-158">Requirement</span></span> | <span data-ttu-id="23d24-159">Valore</span><span class="sxs-lookup"><span data-stu-id="23d24-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23d24-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23d24-160">Minimum supported client</span></span><br/> | <span data-ttu-id="23d24-161">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="23d24-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23d24-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23d24-162">Minimum supported server</span></span><br/> | <span data-ttu-id="23d24-163">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="23d24-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23d24-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="23d24-164">Namespace</span></span><br/>                | <span data-ttu-id="23d24-165">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="23d24-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23d24-166">MOF</span><span class="sxs-lookup"><span data-stu-id="23d24-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23d24-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23d24-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23d24-168">DLL</span><span class="sxs-lookup"><span data-stu-id="23d24-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23d24-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23d24-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

