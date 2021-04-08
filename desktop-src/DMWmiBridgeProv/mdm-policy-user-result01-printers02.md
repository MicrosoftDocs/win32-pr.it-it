---
title: Classe MDM_Policy_User_Result01_Printers02
description: La \_ classe del criterio MDM \_ utente \_ Result01 \_ Printers02 rappresenta i criteri di stampa disponibili.
ms.assetid: c9555ba3-589c-4b9f-8fad-86fcda031555
keywords:
- Classe MDM_Policy_User_Result01_Printers02
- Classe MDM_Policy_User_Result01_Printers02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Printers02
- MDM_Policy_User_Result01_Printers02.InstanceID
- MDM_Policy_User_Result01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a93e2547fbdd8d2d8883d187fca758d5d0b592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740087"
---
# <a name="mdm_policy_user_result01_printers02-class"></a><span data-ttu-id="13c2c-105">\_Utente criteri \_ MDM \_ Result01 \_ classe Printers02</span><span class="sxs-lookup"><span data-stu-id="13c2c-105">MDM\_Policy\_User\_Result01\_Printers02 class</span></span>

<span data-ttu-id="13c2c-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="13c2c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="13c2c-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="13c2c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="13c2c-108">La \_ classe del criterio MDM \_ utente \_ Result01 \_ Printers02 rappresenta i criteri di stampa disponibili.</span><span class="sxs-lookup"><span data-stu-id="13c2c-108">The MDM\_Policy\_User\_Result01\_Printers02 class represents the available printer policies.</span></span>

<span data-ttu-id="13c2c-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="13c2c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c2c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13c2c-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a><span data-ttu-id="13c2c-111">Members</span><span class="sxs-lookup"><span data-stu-id="13c2c-111">Members</span></span>

<span data-ttu-id="13c2c-112">La **classe \_ \_ \_ Result01 \_ Printers02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="13c2c-112">The **MDM\_Policy\_User\_Result01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="13c2c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13c2c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13c2c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13c2c-114">Properties</span></span>

<span data-ttu-id="13c2c-115">La **classe \_ \_ \_ Result01 \_ Printers02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="13c2c-115">The **MDM\_Policy\_User\_Result01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13c2c-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="13c2c-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c2c-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13c2c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13c2c-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13c2c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13c2c-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13c2c-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13c2c-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="13c2c-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c2c-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13c2c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13c2c-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13c2c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13c2c-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13c2c-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13c2c-124">\_Utente PointAndPrintRestrictions</span><span class="sxs-lookup"><span data-stu-id="13c2c-124">PointAndPrintRestrictions\_User</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c2c-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13c2c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13c2c-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13c2c-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13c2c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13c2c-127">Requirements</span></span>



| <span data-ttu-id="13c2c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="13c2c-128">Requirement</span></span> | <span data-ttu-id="13c2c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="13c2c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c2c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13c2c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="13c2c-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="13c2c-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13c2c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13c2c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="13c2c-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="13c2c-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="13c2c-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13c2c-134">Namespace</span></span><br/>                | <span data-ttu-id="13c2c-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="13c2c-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="13c2c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="13c2c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13c2c-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13c2c-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="13c2c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="13c2c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13c2c-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13c2c-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

