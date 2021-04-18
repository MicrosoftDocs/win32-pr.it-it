---
description: Funge da classe padre per la \_ \_ classe di sistema Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: Classe __Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313213"
---
# <a name="__provider-class"></a><span data-ttu-id="db9b8-103">\_\_Classe provider</span><span class="sxs-lookup"><span data-stu-id="db9b8-103">\_\_Provider class</span></span>

<span data-ttu-id="db9b8-104">La classe di sistema del **\_ \_ provider** è una classe di base astratta che funge da classe padre per la classe di sistema [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="db9b8-104">The **\_\_Provider** system class is an abstract base class that serves as the parent class for the [**\_\_Win32Provider**](--win32provider.md) system class.</span></span>

<span data-ttu-id="db9b8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="db9b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="db9b8-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="db9b8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9b8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db9b8-107">Syntax</span></span>

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="db9b8-108">Members</span><span class="sxs-lookup"><span data-stu-id="db9b8-108">Members</span></span>

<span data-ttu-id="db9b8-109">La classe del **\_ \_ provider** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="db9b8-109">The **\_\_Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="db9b8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="db9b8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db9b8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="db9b8-111">Properties</span></span>

<span data-ttu-id="db9b8-112">La classe del **\_ \_ provider** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="db9b8-112">The **\_\_Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db9b8-113">**Nome**</span><span class="sxs-lookup"><span data-stu-id="db9b8-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db9b8-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="db9b8-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db9b8-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="db9b8-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="db9b8-116">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="db9b8-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="db9b8-117">Stringa indipendente dalla lingua che identifica in modo univoco il provider.</span><span class="sxs-lookup"><span data-stu-id="db9b8-117">Language-neutral string that uniquely identifies the provider.</span></span> <span data-ttu-id="db9b8-118">Per evitare conflitti di denominazione, è consigliabile il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="db9b8-118">The following format is suggested to prevent naming conflicts:</span></span>

<span data-ttu-id="db9b8-119">\|versione provider \| Fornitore</span><span class="sxs-lookup"><span data-stu-id="db9b8-119">vendor\|provider\|version</span></span>

<span data-ttu-id="db9b8-120">Questo nome di provider rappresenta ad esempio la versione 1,0 di Microsoft TestProvider:</span><span class="sxs-lookup"><span data-stu-id="db9b8-120">For example, this provider name represents version 1.0 of the Microsoft TestProvider:</span></span>

<span data-ttu-id="db9b8-121">"Microsoft \| TestProvider \| v 1.0"</span><span class="sxs-lookup"><span data-stu-id="db9b8-121">"Microsoft\|TestProvider\|V1.0"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db9b8-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="db9b8-122">Remarks</span></span>

<span data-ttu-id="db9b8-123">La classe **\_ \_ provider** è derivata da [**\_ \_ SystemClass**](--systemclass.md), che non dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="db9b8-123">The **\_\_Provider** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="db9b8-124">I provider creano istanze [**\_ \_ Win32Provider**](--win32provider.md) per specificare le informazioni relative all'implementazione fisica.</span><span class="sxs-lookup"><span data-stu-id="db9b8-124">Providers create [**\_\_Win32Provider**](--win32provider.md) instances to specify information about their physical implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9b8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db9b8-125">Requirements</span></span>



| <span data-ttu-id="db9b8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="db9b8-126">Requirement</span></span> | <span data-ttu-id="db9b8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="db9b8-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="db9b8-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db9b8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="db9b8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db9b8-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="db9b8-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db9b8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="db9b8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db9b8-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="db9b8-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="db9b8-132">Namespace</span></span><br/>                | <span data-ttu-id="db9b8-133">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="db9b8-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="db9b8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db9b8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9b8-135">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="db9b8-135">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="db9b8-136">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="db9b8-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="db9b8-137">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="db9b8-137">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

