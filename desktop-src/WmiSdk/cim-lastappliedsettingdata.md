---
description: Associazione tra un oggetto e un altro oggetto a cui è stato applicato.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: Classe CIM_LastAppliedSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324712"
---
# <a name="cim_lastappliedsettingdata-class"></a><span data-ttu-id="4d869-103">CIM \_ LastAppliedSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="4d869-103">CIM\_LastAppliedSettingData class</span></span>

<span data-ttu-id="4d869-104">Associazione tra un oggetto e un altro oggetto a cui è stato applicato.</span><span class="sxs-lookup"><span data-stu-id="4d869-104">An association between an object and another object which has been applied to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d869-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4d869-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4d869-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4d869-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4d869-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4d869-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d869-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d869-108">Syntax</span></span>

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a><span data-ttu-id="4d869-109">Members</span><span class="sxs-lookup"><span data-stu-id="4d869-109">Members</span></span>

<span data-ttu-id="4d869-110">La classe **CIM \_ LastAppliedSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4d869-110">The **CIM\_LastAppliedSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4d869-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d869-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d869-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d869-112">Properties</span></span>

<span data-ttu-id="4d869-113">La classe **CIM \_ LastAppliedSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d869-113">The **CIM\_LastAppliedSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d869-114">**AppliedObject**</span><span class="sxs-lookup"><span data-stu-id="4d869-114">**AppliedObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d869-115">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="4d869-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4d869-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d869-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d869-117">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="4d869-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4d869-118">Oggetto applicato all'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4d869-118">The object that was applied to the target object.</span></span>

</dd> <dt>

<span data-ttu-id="4d869-119">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="4d869-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d869-120">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="4d869-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4d869-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d869-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d869-122">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="4d869-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4d869-123">Oggetto che era la destinazione dell'applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4d869-123">The object that was the target of the object's application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d869-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d869-124">Requirements</span></span>



| <span data-ttu-id="4d869-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d869-125">Requirement</span></span> | <span data-ttu-id="4d869-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4d869-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="4d869-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d869-127">Namespace</span></span><br/> | <span data-ttu-id="4d869-128">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4d869-128">Root\\CIMV2</span></span><br/> |



 

 




