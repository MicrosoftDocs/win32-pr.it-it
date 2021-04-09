---
title: Classe MDM_ClientCertificateInstall_PFXCertInstall01_01
description: La \_ classe MDM ClientCertificateInstall \_ PFXCertInstall01 \_ 01 consente all'azienda di usare ID univoci per distinguere le diverse richieste di installazione del certificato.
ms.assetid: 13b4d646-b49e-4a9d-b644-b52279249063
keywords:
- Classe MDM_ClientCertificateInstall_PFXCertInstall01_01
- Classe MDM_ClientCertificateInstall_PFXCertInstall01_01, descritta
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01.InstanceID
- MDM_ClientCertificateInstall_PFXCertInstall01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed0bbbfad0e61a95fa8130921e639de1772233d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120662"
---
# <a name="mdm_clientcertificateinstall_pfxcertinstall01_01-class"></a><span data-ttu-id="9eac3-105">\_Classe MDM ClientCertificateInstall \_ PFXCertInstall01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="9eac3-105">MDM\_ClientCertificateInstall\_PFXCertInstall01\_01 class</span></span>

<span data-ttu-id="9eac3-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9eac3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9eac3-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9eac3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9eac3-108">La classe **MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** consente all'azienda di usare ID univoci per distinguere le diverse richieste di installazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="9eac3-108">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class enables the enterprise to use unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="9eac3-109">Obbligatorio per l'installazione del certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="9eac3-109">Required for PFX certificate installation.</span></span> <span data-ttu-id="9eac3-110">Se si chiama Delete sul nodo, è necessario eliminare i certificati e le chiavi installate dal BLOB PFX corrispondente.</span><span class="sxs-lookup"><span data-stu-id="9eac3-110">Calling Delete on the this node, should delete the certificates and the keys that were installed by the corresponding PFX blob.</span></span>

<span data-ttu-id="9eac3-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9eac3-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eac3-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eac3-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_PFXCertInstall01_01
{
  string  InstanceID;
  string  ParentID;
  sint32  KeyLocation;
  string  ContainerName;
  string  PFXCertBlob;
  string  PFXCertPassword;
  sint32  PFXCertPasswordEncryptionType;
  boolean PFXKeyExportable;
  string  Thumbprint;
  sint32  Status;
  string  PFXCertPasswordEncryptionStore;
};
```

## <a name="members"></a><span data-ttu-id="9eac3-113">Members</span><span class="sxs-lookup"><span data-stu-id="9eac3-113">Members</span></span>

<span data-ttu-id="9eac3-114">La classe **MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9eac3-114">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="9eac3-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9eac3-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9eac3-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9eac3-116">Properties</span></span>

<span data-ttu-id="9eac3-117">La classe **MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9eac3-117">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9eac3-118">ContainerName</span><span class="sxs-lookup"><span data-stu-id="9eac3-118">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9eac3-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eac3-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9eac3-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9eac3-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9eac3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9eac3-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9eac3-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9eac3-125">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9eac3-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="9eac3-126">Per questa classe, un ID univoco per distinguere le diverse richieste di installazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="9eac3-126">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

[<span data-ttu-id="9eac3-127">Posizione della sede</span><span class="sxs-lookup"><span data-stu-id="9eac3-127">KeyLocation</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-keylocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-128">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eac3-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eac3-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9eac3-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9eac3-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9eac3-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9eac3-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9eac3-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9eac3-134">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="9eac3-134">Describes the full path to the parent node.</span></span>

<span data-ttu-id="9eac3-135">La stringa è "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span><span class="sxs-lookup"><span data-stu-id="9eac3-135">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span></span>

</dd> <dt>

[<span data-ttu-id="9eac3-136">PFXCertBlob</span><span class="sxs-lookup"><span data-stu-id="9eac3-136">PFXCertBlob</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertblob)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9eac3-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eac3-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-139">Qualificatori: **OctetString**</span><span class="sxs-lookup"><span data-stu-id="9eac3-139">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eac3-140">PFXCertPassword</span><span class="sxs-lookup"><span data-stu-id="9eac3-140">PFXCertPassword</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9eac3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eac3-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eac3-143">PFXCertPasswordEncryptionStore</span><span class="sxs-lookup"><span data-stu-id="9eac3-143">PFXCertPasswordEncryptionStore</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptionstore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9eac3-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eac3-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eac3-146">PFXCertPasswordEncryptionType</span><span class="sxs-lookup"><span data-stu-id="9eac3-146">PFXCertPasswordEncryptionType</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptiontype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eac3-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eac3-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eac3-149">PFXKeyExportable</span><span class="sxs-lookup"><span data-stu-id="9eac3-149">PFXKeyExportable</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxkeyexportable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-150">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9eac3-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eac3-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eac3-152">Status</span><span class="sxs-lookup"><span data-stu-id="9eac3-152">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9eac3-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eac3-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9eac3-155">Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="9eac3-155">Thumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-thumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9eac3-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9eac3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9eac3-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9eac3-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9eac3-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eac3-158">Requirements</span></span>



| <span data-ttu-id="9eac3-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eac3-159">Requirement</span></span> | <span data-ttu-id="9eac3-160">Valore</span><span class="sxs-lookup"><span data-stu-id="9eac3-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eac3-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eac3-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9eac3-162">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9eac3-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9eac3-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eac3-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9eac3-164">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9eac3-164">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9eac3-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9eac3-165">Namespace</span></span><br/>                | <span data-ttu-id="9eac3-166">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="9eac3-166">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9eac3-167">MOF</span><span class="sxs-lookup"><span data-stu-id="9eac3-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9eac3-168"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9eac3-168"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9eac3-169">DLL</span><span class="sxs-lookup"><span data-stu-id="9eac3-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eac3-170"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eac3-170"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eac3-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eac3-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eac3-172">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="9eac3-172">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

