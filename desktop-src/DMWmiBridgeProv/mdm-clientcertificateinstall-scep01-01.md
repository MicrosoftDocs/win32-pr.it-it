---
title: Classe MDM_ClientCertificateInstall_SCEP01_01
description: La \_ classe MDM ClientCertificateInstall \_ SCEP01 \_ 01 consente di accedere al nodo per l'installazione del certificato SCEP, usando ID univoci per distinguere le diverse richieste di installazione del certificato.
ms.assetid: 273e6ef7-fd00-4049-bb8b-b9900b3d250b
keywords:
- Classe MDM_ClientCertificateInstall_SCEP01_01
- Classe MDM_ClientCertificateInstall_SCEP01_01, descritta
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01.InstanceID
- MDM_ClientCertificateInstall_SCEP01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f8db7decb2e3ae0674381b2f17df10f82ee38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874202"
---
# <a name="mdm_clientcertificateinstall_scep01_01-class"></a><span data-ttu-id="c6ddd-105">\_Classe MDM ClientCertificateInstall \_ SCEP01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="c6ddd-105">MDM\_ClientCertificateInstall\_SCEP01\_01 class</span></span>

<span data-ttu-id="c6ddd-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c6ddd-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c6ddd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c6ddd-108">La classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** consente di accedere al nodo per l'installazione del certificato SCEP, usando ID univoci per distinguere le diverse richieste di installazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-108">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class enables access to the node for SCEP certificate installation, using unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="c6ddd-109">Obbligatorio per l'installazione del certificato SCEP.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-109">Required for SCEP certificate installation.</span></span>

<span data-ttu-id="c6ddd-110">Le operazioni supportate sono Get, Add ed Delete.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-110">Supported operations are Get, Add and Delete.</span></span>

<span data-ttu-id="c6ddd-111">Se si chiama Delete nel nodo, è necessario eliminare il certificato SCEP corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-111">Calling Delete on the this node should delete the corresponding SCEP certificate.</span></span>

<span data-ttu-id="c6ddd-112">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ddd-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6ddd-113">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_SCEP01_01
{
  string InstanceID;
  string ParentID;
  string CertThumbprint;
  sint32 Status;
  sint32 ErrorCode;
  string RespondentServerUrl;
};
```

## <a name="members"></a><span data-ttu-id="c6ddd-114">Members</span><span class="sxs-lookup"><span data-stu-id="c6ddd-114">Members</span></span>

<span data-ttu-id="c6ddd-115">La classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c6ddd-115">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="c6ddd-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6ddd-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6ddd-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6ddd-117">Properties</span></span>

<span data-ttu-id="c6ddd-118">La classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-118">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c6ddd-119">CertThumbprint</span><span class="sxs-lookup"><span data-stu-id="c6ddd-119">CertThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-certthumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ddd-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6ddd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6ddd-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c6ddd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6ddd-122">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="c6ddd-122">ErrorCode</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-errorcode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ddd-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ddd-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ddd-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c6ddd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c6ddd-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c6ddd-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ddd-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6ddd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6ddd-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6ddd-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ddd-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c6ddd-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c6ddd-129">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="c6ddd-130">Per questa classe, un ID univoco per distinguere le diverse richieste di installazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-130">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

<span data-ttu-id="c6ddd-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c6ddd-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ddd-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6ddd-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6ddd-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6ddd-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6ddd-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c6ddd-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c6ddd-135">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="c6ddd-135">Describes the full path to the parent node.</span></span>

<span data-ttu-id="c6ddd-136">La stringa è "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span><span class="sxs-lookup"><span data-stu-id="c6ddd-136">The string is "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span></span>

</dd> <dt>

[<span data-ttu-id="c6ddd-137">RespondentServerUrl</span><span class="sxs-lookup"><span data-stu-id="c6ddd-137">RespondentServerUrl</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-respondentserverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ddd-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6ddd-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6ddd-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c6ddd-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6ddd-140">Status</span><span class="sxs-lookup"><span data-stu-id="c6ddd-140">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6ddd-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6ddd-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6ddd-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c6ddd-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6ddd-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6ddd-143">Requirements</span></span>



| <span data-ttu-id="c6ddd-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ddd-144">Requirement</span></span> | <span data-ttu-id="c6ddd-145">Valore</span><span class="sxs-lookup"><span data-stu-id="c6ddd-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ddd-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6ddd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ddd-147">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c6ddd-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6ddd-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6ddd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ddd-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c6ddd-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c6ddd-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c6ddd-150">Namespace</span></span><br/>                | <span data-ttu-id="c6ddd-151">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="c6ddd-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c6ddd-152">MOF</span><span class="sxs-lookup"><span data-stu-id="c6ddd-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6ddd-153"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6ddd-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6ddd-154">DLL</span><span class="sxs-lookup"><span data-stu-id="c6ddd-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6ddd-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6ddd-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6ddd-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6ddd-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ddd-157">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="c6ddd-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

