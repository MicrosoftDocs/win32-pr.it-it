---
title: Classe MDM_Policy_Config01_Location02
description: La \_ \_ \_ classe Config01 LOCATION02 di criteri MDM configura il servizio di posizione del dispositivo.
ms.assetid: 8a40628e-1167-45ed-89bf-f3383dfb08d4
keywords:
- Classe MDM_Policy_Config01_Location02
- Classe MDM_Policy_Config01_Location02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Location02
- MDM_Policy_Config01_Location02.InstanceID
- MDM_Policy_Config01_Location02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ced896905395d577546630ff97e4eff45719773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873781"
---
# <a name="mdm_policy_config01_location02-class"></a><span data-ttu-id="a5066-105">\_ \_ Classe Config01 Location02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="a5066-105">MDM\_Policy\_Config01\_Location02 class</span></span>

<span data-ttu-id="a5066-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="a5066-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a5066-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="a5066-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a5066-108">La \_ \_ \_ classe Config01 LOCATION02 di criteri MDM configura il servizio di posizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5066-108">The MDM\_Policy\_Config01\_Location02 class configures the location service of the device.</span></span>

<span data-ttu-id="a5066-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a5066-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5066-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5066-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Location02
{
  string InstanceID;
  string ParentID;
  sint32 EnableLocation;
};
```

## <a name="members"></a><span data-ttu-id="a5066-111">Members</span><span class="sxs-lookup"><span data-stu-id="a5066-111">Members</span></span>

<span data-ttu-id="a5066-112">La **classe \_ \_ Config01 \_ Location02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a5066-112">The **MDM\_Policy\_Config01\_Location02** class has these types of members:</span></span>

-   [<span data-ttu-id="a5066-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5066-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5066-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5066-114">Properties</span></span>

<span data-ttu-id="a5066-115">La **classe \_ \_ \_ Location02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a5066-115">The **MDM\_Policy\_Config01\_Location02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5066-116">**EnableLocation**</span><span class="sxs-lookup"><span data-stu-id="a5066-116">**EnableLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5066-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a5066-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5066-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a5066-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5066-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a5066-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5066-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5066-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5066-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5066-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5066-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a5066-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5066-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a5066-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5066-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5066-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5066-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5066-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5066-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a5066-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5066-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5066-127">Requirements</span></span>



| <span data-ttu-id="a5066-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5066-128">Requirement</span></span> | <span data-ttu-id="a5066-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a5066-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5066-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5066-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a5066-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a5066-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5066-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5066-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a5066-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a5066-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a5066-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a5066-134">Namespace</span></span><br/>                | <span data-ttu-id="a5066-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="a5066-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a5066-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a5066-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5066-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5066-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5066-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a5066-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5066-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5066-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

