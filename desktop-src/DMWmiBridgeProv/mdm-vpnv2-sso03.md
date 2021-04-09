---
title: Classe MDM_VPNv2_Sso03
description: La \_ classe MDM VPNv2 \_ Sso03 può essere usata per selezionare un certificato diverso dal certificato di autenticazione VPN per l'autenticazione Kerberos nel caso della conformità del dispositivo.
ms.assetid: 179b6b69-1319-4310-aebc-f61550af6c77
keywords:
- Classe MDM_VPNv2_Sso03
- Classe MDM_VPNv2_Sso03, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_Sso03
- MDM_VPNv2_Sso03.InstanceID
- MDM_VPNv2_Sso03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5f3f10d365e1405981e206963cd98f0b7f803c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964612"
---
# <a name="mdm_vpnv2_sso03-class"></a><span data-ttu-id="ca812-105">\_Classe MDM VPNv2 \_ Sso03</span><span class="sxs-lookup"><span data-stu-id="ca812-105">MDM\_VPNv2\_Sso03 class</span></span>

<span data-ttu-id="ca812-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ca812-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ca812-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ca812-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ca812-108">La classe **MDM \_ VPNv2 \_ Sso03** può essere usata per selezionare un certificato diverso dal certificato di autenticazione VPN per l'autenticazione Kerberos nel caso della conformità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca812-108">The **MDM\_VPNv2\_Sso03** class can be used to select a certificate different from the VPN Authentication certificate for the Kerberos Authentication in the case of Device Compliance.</span></span>

<span data-ttu-id="ca812-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ca812-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca812-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca812-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Sso03
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
  string  IssuerHash;
  string  Eku;
};
```

## <a name="members"></a><span data-ttu-id="ca812-111">Members</span><span class="sxs-lookup"><span data-stu-id="ca812-111">Members</span></span>

<span data-ttu-id="ca812-112">La classe **MDM \_ VPNv2 \_ Sso03** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ca812-112">The **MDM\_VPNv2\_Sso03** class has these types of members:</span></span>

-   [<span data-ttu-id="ca812-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca812-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca812-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca812-114">Properties</span></span>

<span data-ttu-id="ca812-115">La classe **MDM \_ VPNv2 \_ Sso03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca812-115">The **MDM\_VPNv2\_Sso03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ca812-116">EKU</span><span class="sxs-lookup"><span data-stu-id="ca812-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca812-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca812-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca812-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca812-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca812-119">Enabled</span><span class="sxs-lookup"><span data-stu-id="ca812-119">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca812-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ca812-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca812-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca812-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca812-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ca812-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca812-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca812-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca812-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca812-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca812-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca812-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca812-126">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ca812-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="ca812-127">IssuerHash</span><span class="sxs-lookup"><span data-stu-id="ca812-127">IssuerHash</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-issuerhash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca812-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca812-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca812-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ca812-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca812-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ca812-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca812-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca812-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca812-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca812-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca812-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca812-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca812-134">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ca812-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="ca812-135">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span><span class="sxs-lookup"><span data-stu-id="ca812-135">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca812-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca812-136">Requirements</span></span>



| <span data-ttu-id="ca812-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca812-137">Requirement</span></span> | <span data-ttu-id="ca812-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ca812-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca812-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca812-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ca812-140">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ca812-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca812-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca812-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ca812-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ca812-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ca812-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca812-143">Namespace</span></span><br/>                | <span data-ttu-id="ca812-144">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ca812-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ca812-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ca812-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca812-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca812-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca812-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ca812-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca812-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca812-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca812-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca812-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca812-150">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="ca812-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

