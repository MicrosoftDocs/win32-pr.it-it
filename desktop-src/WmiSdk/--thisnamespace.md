---
description: Include i privilegi di protezione per lo spazio dei nomi sotto forma di descrittore di sicurezza.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: Classe __thisNAMESPACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316587"
---
# <a name="__thisnamespace-class"></a><span data-ttu-id="6258c-103">\_\_Classe thisNAMESPACE</span><span class="sxs-lookup"><span data-stu-id="6258c-103">\_\_thisNAMESPACE class</span></span>

<span data-ttu-id="6258c-104">La classe di sistema **\_ \_ thisNamespace** include i privilegi di protezione per lo spazio dei nomi sotto forma di descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6258c-104">The **\_\_thisNAMESPACE** system class holds the security rights for the namespace in the form of a security descriptor.</span></span> <span data-ttu-id="6258c-105">Questa classe e una singola istanza si trovano in tutti gli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6258c-105">This class and a single instance is found in all namespaces.</span></span>

<span data-ttu-id="6258c-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6258c-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6258c-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6258c-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6258c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6258c-108">Syntax</span></span>

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a><span data-ttu-id="6258c-109">Members</span><span class="sxs-lookup"><span data-stu-id="6258c-109">Members</span></span>

<span data-ttu-id="6258c-110">La classe **\_ \_ thisNamespace** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6258c-110">The **\_\_thisNAMESPACE** class has these types of members:</span></span>

-   [<span data-ttu-id="6258c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6258c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6258c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6258c-112">Properties</span></span>

<span data-ttu-id="6258c-113">La classe **\_ \_ thisNamespace** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6258c-113">The **\_\_thisNAMESPACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6258c-114">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="6258c-114">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6258c-115">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6258c-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6258c-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6258c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6258c-117">Descrittore di sicurezza che descrive chi può accedere allo spazio dei nomi e chi può leggere o scrivere nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6258c-117">Security descriptor describing who can access the namespace and who can read from or write to the namespace.</span></span> <span data-ttu-id="6258c-118">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="6258c-118">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="6258c-119">Per ulteriori informazioni sul formato dei descrittori di sicurezza, vedere [descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) nella sezione sicurezza del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6258c-119">For more information about the format of security descriptors, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors) in the Security section of the Windows SDK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6258c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="6258c-120">Remarks</span></span>

<span data-ttu-id="6258c-121">L'istanza singleton di **\_ \_ thisNamespace** è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6258c-121">The singleton instance of **\_\_thisNAMESPACE** is read-only.</span></span> <span data-ttu-id="6258c-122">Per modificare le impostazioni della proprietà del descrittore di sicurezza, utilizzare i metodi della classe [**\_ \_ SystemSecurity**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="6258c-122">To change the settings of the security descriptor property, use the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span> <span data-ttu-id="6258c-123">La classe **\_ \_ thisNamespace** deriva da [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="6258c-123">The **\_\_thisNAMESPACE** class derives from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6258c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6258c-124">Requirements</span></span>



| <span data-ttu-id="6258c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6258c-125">Requirement</span></span> | <span data-ttu-id="6258c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6258c-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6258c-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6258c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6258c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6258c-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6258c-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6258c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6258c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6258c-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6258c-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6258c-131">Namespace</span></span><br/>                | <span data-ttu-id="6258c-132">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6258c-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6258c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6258c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6258c-134">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="6258c-134">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="6258c-135">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="6258c-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

