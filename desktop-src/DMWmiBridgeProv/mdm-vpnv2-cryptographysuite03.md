---
title: Classe MDM_VPNv2_CryptographySuite03
description: La \_ classe MDM VPNv2 \_ CryptographySuite03 contiene informazioni di crittografia per il profilo VPN nativo.
ms.assetid: d8d16d43-bd54-4ca8-a850-ce48390df7d6
keywords:
- Classe MDM_VPNv2_CryptographySuite03
- Classe MDM_VPNv2_CryptographySuite03, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_CryptographySuite03
- MDM_VPNv2_CryptographySuite03.InstanceID
- MDM_VPNv2_CryptographySuite03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553f2dcddd4d7c7e0926945a80f74f6aba2a9467
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476769"
---
# <a name="mdm_vpnv2_cryptographysuite03-class"></a><span data-ttu-id="12fb0-105">\_Classe MDM VPNv2 \_ CryptographySuite03</span><span class="sxs-lookup"><span data-stu-id="12fb0-105">MDM\_VPNv2\_CryptographySuite03 class</span></span>

<span data-ttu-id="12fb0-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="12fb0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="12fb0-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="12fb0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="12fb0-108">La classe **MDM \_ VPNv2 \_ CryptographySuite03** contiene informazioni di crittografia per il profilo VPN nativo.</span><span class="sxs-lookup"><span data-stu-id="12fb0-108">The **MDM\_VPNv2\_CryptographySuite03** class contains cryptography information for the native VPN profile.</span></span>

<span data-ttu-id="12fb0-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="12fb0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fb0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12fb0-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_CryptographySuite03
{
  string InstanceID;
  string ParentID;
  string AuthenticationTransformConstants;
  string CipherTransformConstants;
  string EncryptionMethod;
  string IntegrityCheckMethod;
  string DHGroup;
  string PfsGroup;
};
```

## <a name="members"></a><span data-ttu-id="12fb0-111">Members</span><span class="sxs-lookup"><span data-stu-id="12fb0-111">Members</span></span>

<span data-ttu-id="12fb0-112">La classe **MDM \_ VPNv2 \_ CryptographySuite03** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="12fb0-112">The **MDM\_VPNv2\_CryptographySuite03** class has these types of members:</span></span>

-   [<span data-ttu-id="12fb0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12fb0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12fb0-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="12fb0-114">Properties</span></span>

<span data-ttu-id="12fb0-115">La classe **MDM \_ VPNv2 \_ CryptographySuite03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="12fb0-115">The **MDM\_VPNv2\_CryptographySuite03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="12fb0-116">AuthenticationTransformConstants</span><span class="sxs-lookup"><span data-stu-id="12fb0-116">AuthenticationTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-authenticationtransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12fb0-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12fb0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="12fb0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12fb0-119">CipherTransformConstants</span><span class="sxs-lookup"><span data-stu-id="12fb0-119">CipherTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-ciphertransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12fb0-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12fb0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="12fb0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12fb0-122">DHGroup</span><span class="sxs-lookup"><span data-stu-id="12fb0-122">DHGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-dhgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12fb0-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12fb0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="12fb0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="12fb0-125">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="12fb0-125">EncryptionMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12fb0-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12fb0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="12fb0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="12fb0-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="12fb0-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12fb0-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12fb0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12fb0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="12fb0-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="12fb0-132">Nodo contenente le proprietà dei tunnel IPSec.</span><span class="sxs-lookup"><span data-stu-id="12fb0-132">Node containing the properties of IPSec tunnels.</span></span>

</dd> <dt>

[<span data-ttu-id="12fb0-133">IntegrityCheckMethod</span><span class="sxs-lookup"><span data-stu-id="12fb0-133">IntegrityCheckMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-integritycheckmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12fb0-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12fb0-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="12fb0-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="12fb0-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="12fb0-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12fb0-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12fb0-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="12fb0-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-139">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="12fb0-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="12fb0-140">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="12fb0-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="12fb0-141">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span><span class="sxs-lookup"><span data-stu-id="12fb0-141">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="12fb0-142">PfsGroup</span><span class="sxs-lookup"><span data-stu-id="12fb0-142">PfsGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-pfsgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="12fb0-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="12fb0-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12fb0-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="12fb0-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12fb0-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12fb0-145">Requirements</span></span>



| <span data-ttu-id="12fb0-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="12fb0-146">Requirement</span></span> | <span data-ttu-id="12fb0-147">Valore</span><span class="sxs-lookup"><span data-stu-id="12fb0-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12fb0-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12fb0-148">Minimum supported client</span></span><br/> | <span data-ttu-id="12fb0-149">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="12fb0-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12fb0-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12fb0-150">Minimum supported server</span></span><br/> | <span data-ttu-id="12fb0-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="12fb0-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="12fb0-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="12fb0-152">Namespace</span></span><br/>                | <span data-ttu-id="12fb0-153">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="12fb0-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="12fb0-154">MOF</span><span class="sxs-lookup"><span data-stu-id="12fb0-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12fb0-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12fb0-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="12fb0-156">DLL</span><span class="sxs-lookup"><span data-stu-id="12fb0-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12fb0-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12fb0-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

