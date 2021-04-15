---
description: Contiene le impostazioni utilizzate durante le operazioni di manutenzione.
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Classe Msvm_ServicingSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485269"
---
# <a name="msvm_servicingsettings-class"></a><span data-ttu-id="882ea-103">\_Classe MSVM ServicingSettings</span><span class="sxs-lookup"><span data-stu-id="882ea-103">Msvm\_ServicingSettings class</span></span>

<span data-ttu-id="882ea-104">Contiene le impostazioni utilizzate durante le operazioni di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="882ea-104">Contains settings used during servicing operations.</span></span>

<span data-ttu-id="882ea-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="882ea-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="882ea-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="882ea-106">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="882ea-107">Members</span><span class="sxs-lookup"><span data-stu-id="882ea-107">Members</span></span>

<span data-ttu-id="882ea-108">La **classe \_ ServicingSettings di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="882ea-108">The **Msvm\_ServicingSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="882ea-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="882ea-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="882ea-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="882ea-110">Properties</span></span>

<span data-ttu-id="882ea-111">La **classe \_ ServicingSettings di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="882ea-111">The **Msvm\_ServicingSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="882ea-112">**Versione**</span><span class="sxs-lookup"><span data-stu-id="882ea-112">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="882ea-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="882ea-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="882ea-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="882ea-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="882ea-115">Contiene la versione della definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="882ea-115">Contains the class definition's version.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="882ea-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="882ea-116">Requirements</span></span>



| <span data-ttu-id="882ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="882ea-117">Requirement</span></span> | <span data-ttu-id="882ea-118">Valore</span><span class="sxs-lookup"><span data-stu-id="882ea-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="882ea-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="882ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="882ea-120">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="882ea-120">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="882ea-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="882ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="882ea-122">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="882ea-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="882ea-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="882ea-123">Namespace</span></span><br/>                | <span data-ttu-id="882ea-124">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="882ea-124">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="882ea-125">MOF</span><span class="sxs-lookup"><span data-stu-id="882ea-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="882ea-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="882ea-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="882ea-127">DLL</span><span class="sxs-lookup"><span data-stu-id="882ea-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="882ea-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="882ea-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




