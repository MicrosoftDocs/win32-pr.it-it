---
title: Classe MDM_VPNv2_Eap04
description: La \_ classe MDM VPNv2 \_ Eap04 contiene le informazioni XML di configurazione necessarie quando il profilo nativo specifica l'autenticazione EAP.
ms.assetid: 87a78743-1ee6-4b86-bfbf-62ba9059535a
keywords:
- Classe MDM_VPNv2_Eap04
- Classe MDM_VPNv2_Eap04, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_Eap04
- MDM_VPNv2_Eap04.InstanceID
- MDM_VPNv2_Eap04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9270bf1cae37c345fe81be674e9d9afc2c533bc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743162"
---
# <a name="mdm_vpnv2_eap04-class"></a><span data-ttu-id="ff4e8-105">\_Classe MDM VPNv2 \_ Eap04</span><span class="sxs-lookup"><span data-stu-id="ff4e8-105">MDM\_VPNv2\_Eap04 class</span></span>

<span data-ttu-id="ff4e8-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ff4e8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ff4e8-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ff4e8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ff4e8-108">La classe **MDM \_ VPNv2 \_ Eap04** contiene le informazioni XML di configurazione necessarie quando il profilo nativo specifica l'autenticazione EAP.</span><span class="sxs-lookup"><span data-stu-id="ff4e8-108">The **MDM\_VPNv2\_Eap04** class contains the required configuration XML information when the native profile specifies EAP authentication.</span></span>

<span data-ttu-id="ff4e8-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ff4e8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4e8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff4e8-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Eap04
{
  string InstanceID;
  string ParentID;
  string Configuration;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="ff4e8-111">Members</span><span class="sxs-lookup"><span data-stu-id="ff4e8-111">Members</span></span>

<span data-ttu-id="ff4e8-112">La classe **MDM \_ VPNv2 \_ Eap04** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ff4e8-112">The **MDM\_VPNv2\_Eap04** class has these types of members:</span></span>

-   [<span data-ttu-id="ff4e8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ff4e8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff4e8-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ff4e8-114">Properties</span></span>

<span data-ttu-id="ff4e8-115">La classe **MDM \_ VPNv2 \_ Eap04** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ff4e8-115">The **MDM\_VPNv2\_Eap04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ff4e8-116">Configuration</span><span class="sxs-lookup"><span data-stu-id="ff4e8-116">Configuration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-eap-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff4e8-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ff4e8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff4e8-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ff4e8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ff4e8-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ff4e8-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff4e8-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ff4e8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff4e8-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ff4e8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff4e8-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ff4e8-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ff4e8-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ff4e8-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="ff4e8-124">Per questa classe la stringa è "EAP"</span><span class="sxs-lookup"><span data-stu-id="ff4e8-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

<span data-ttu-id="ff4e8-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ff4e8-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff4e8-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ff4e8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff4e8-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ff4e8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff4e8-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ff4e8-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ff4e8-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ff4e8-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="ff4e8-130">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span><span class="sxs-lookup"><span data-stu-id="ff4e8-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> <dt>

[<span data-ttu-id="ff4e8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff4e8-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff4e8-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ff4e8-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff4e8-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ff4e8-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff4e8-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff4e8-134">Requirements</span></span>



| <span data-ttu-id="ff4e8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff4e8-135">Requirement</span></span> | <span data-ttu-id="ff4e8-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ff4e8-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff4e8-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff4e8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ff4e8-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ff4e8-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff4e8-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff4e8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ff4e8-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ff4e8-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ff4e8-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ff4e8-141">Namespace</span></span><br/>                | <span data-ttu-id="ff4e8-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ff4e8-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ff4e8-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ff4e8-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff4e8-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff4e8-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff4e8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ff4e8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff4e8-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff4e8-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff4e8-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff4e8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff4e8-148">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="ff4e8-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

