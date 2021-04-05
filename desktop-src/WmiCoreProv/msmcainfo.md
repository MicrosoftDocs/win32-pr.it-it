---
description: Classe di base astratta da cui derivano tutte le classi di dati del provider MCA (Machine Check Architecture), ad esempio MSMCAInfo \_ RawMCAData. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Classe MSMCAInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049474"
---
# <a name="msmcainfo-class"></a><span data-ttu-id="5fbfd-104">Classe MSMCAInfo</span><span class="sxs-lookup"><span data-stu-id="5fbfd-104">MSMCAInfo class</span></span>

<span data-ttu-id="5fbfd-105">La classe **MSMCAInfo** è una classe di base astratta da cui derivano tutte le classi di dati del provider MCA (Machine Check Architecture), ad esempio [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md).</span><span class="sxs-lookup"><span data-stu-id="5fbfd-105">The **MSMCAInfo** class is an abstract base class from which all Machine Check Architecture (MCA) provider data classes, such as [**MSMCAInfo\_RawMCAData**](msmcainfo-rawmcadata.md), are derived.</span></span> <span data-ttu-id="5fbfd-106">Il provider MCA dispone anche di classi di evento, derivate da [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="5fbfd-106">The MCA provider also has event classes, derived from [**WMIEvent**](wmievent.md).</span></span> <span data-ttu-id="5fbfd-107">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="5fbfd-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="5fbfd-108">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5fbfd-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5fbfd-109">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5fbfd-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fbfd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fbfd-110">Syntax</span></span>

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a><span data-ttu-id="5fbfd-111">Members</span><span class="sxs-lookup"><span data-stu-id="5fbfd-111">Members</span></span>

<span data-ttu-id="5fbfd-112">La classe **MSMCAInfo** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="5fbfd-112">The **MSMCAInfo** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fbfd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fbfd-113">Requirements</span></span>



| <span data-ttu-id="5fbfd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fbfd-114">Requirement</span></span> | <span data-ttu-id="5fbfd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5fbfd-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbfd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fbfd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5fbfd-117">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5fbfd-117">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="5fbfd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fbfd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5fbfd-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5fbfd-119">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="5fbfd-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5fbfd-120">Namespace</span></span><br/>                | <span data-ttu-id="5fbfd-121">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="5fbfd-121">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="5fbfd-122">MOF</span><span class="sxs-lookup"><span data-stu-id="5fbfd-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fbfd-123"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fbfd-123"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fbfd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5fbfd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fbfd-125"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fbfd-125"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fbfd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fbfd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbfd-127">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="5fbfd-127">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="5fbfd-128">**\_Intestazione MSMCAEvent**</span><span class="sxs-lookup"><span data-stu-id="5fbfd-128">**MSMCAEvent\_Header**</span></span>](msmcaevent-header.md)
</dt> <dt>

[<span data-ttu-id="5fbfd-129">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="5fbfd-129">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




