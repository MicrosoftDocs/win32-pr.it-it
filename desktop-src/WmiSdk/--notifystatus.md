---
description: Funge da classe padre per le classi di errore definite dal provider.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: Classe __NotifyStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759440"
---
# <a name="__notifystatus-class"></a><span data-ttu-id="0bb04-103">\_\_Classe NotifyStatus</span><span class="sxs-lookup"><span data-stu-id="0bb04-103">\_\_NotifyStatus class</span></span>

<span data-ttu-id="0bb04-104">La classe di sistema astratta **\_ \_ NotifyStatus** funge da classe padre per le classi di errore definite dal provider.</span><span class="sxs-lookup"><span data-stu-id="0bb04-104">The **\_\_NotifyStatus** abstract system class serves as the parent class for provider-defined error classes.</span></span>

<span data-ttu-id="0bb04-105">La sintassi seguente è semplificata dal codice Managed Object Format (MF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0bb04-105">The following syntax is simplified from Managed Object Format (MF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb04-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bb04-106">Syntax</span></span>

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="0bb04-107">Members</span><span class="sxs-lookup"><span data-stu-id="0bb04-107">Members</span></span>

<span data-ttu-id="0bb04-108">La classe **\_ \_ NotifyStatus** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0bb04-108">The **\_\_NotifyStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="0bb04-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0bb04-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bb04-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0bb04-110">Properties</span></span>

<span data-ttu-id="0bb04-111">La classe **\_ \_ NotifyStatus** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0bb04-111">The **\_\_NotifyStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0bb04-112">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="0bb04-112">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb04-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bb04-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bb04-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb04-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bb04-115">Contiene un codice di errore o informazioni per un'operazione.</span><span class="sxs-lookup"><span data-stu-id="0bb04-115">Contains an error or information code for an operation.</span></span> <span data-ttu-id="0bb04-116">Può trattarsi di qualsiasi codice definito dall'utente, ma il valore 0 (zero) è in genere riservato per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0bb04-116">This can be any user-defined code, but the value 0 (zero) is usually reserved to indicate success.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bb04-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0bb04-117">Remarks</span></span>

<span data-ttu-id="0bb04-118">Sebbene la classe **\_ \_ NotifyStatus** possa essere la classe padre per le classi di errore definite dal provider, è consigliabile che i provider derivano invece le classi di errore da [**\_ \_ ExtendedStatus**](--extendedstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="0bb04-118">Although the **\_\_NotifyStatus** class can be the parent class for provider-defined error classes, it is recommended that providers derive error classes from [**\_\_ExtendedStatus**](--extendedstatus.md) instead.</span></span> <span data-ttu-id="0bb04-119">L'uso di **\_ \_ ExtendedStatus** consente una maggiore standardizzazione delle classi Error.</span><span class="sxs-lookup"><span data-stu-id="0bb04-119">Using **\_\_ExtendedStatus** allows for greater standardization of error classes.</span></span>

<span data-ttu-id="0bb04-120">I provider non devono mai creare direttamente istanze di **\_ \_ NotifyStatus** , perché queste istanze non contengono più informazioni rispetto a un semplice codice restituito.</span><span class="sxs-lookup"><span data-stu-id="0bb04-120">Providers should never create instances of **\_\_NotifyStatus** directly, because these instances convey no more information than a simple return code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb04-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bb04-121">Requirements</span></span>



| <span data-ttu-id="0bb04-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb04-122">Requirement</span></span> | <span data-ttu-id="0bb04-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0bb04-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0bb04-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bb04-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb04-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0bb04-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0bb04-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bb04-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb04-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bb04-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0bb04-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0bb04-128">Namespace</span></span><br/>                | <span data-ttu-id="0bb04-129">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="0bb04-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0bb04-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bb04-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb04-131">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="0bb04-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




