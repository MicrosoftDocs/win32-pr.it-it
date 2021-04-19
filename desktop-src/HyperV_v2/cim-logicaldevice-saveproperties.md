---
description: Richiede che il dispositivo acquisisca la configurazione corrente, il programma di installazione e/o le informazioni sullo stato in un archivio di backup.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Metodo SaveProperties della classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317768"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="aa62b-103">Metodo SaveProperties della classe CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="aa62b-103">SaveProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="aa62b-104">Richiede che il dispositivo acquisisca la configurazione corrente, il programma di installazione e/o le informazioni sullo stato in un archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="aa62b-104">Requests that the Device capture its current configuration, setup and/or state information in a backing store.</span></span> <span data-ttu-id="aa62b-105">L'obiettivo è quello di usare queste informazioni in un secondo momento (tramite il metodo RestoreProperties), per restituire un dispositivo alla relativa condizione "Condition".</span><span class="sxs-lookup"><span data-stu-id="aa62b-105">The goal would be to use this information at a later time (via the RestoreProperties method), to return a Device to its present "condition".</span></span> <span data-ttu-id="aa62b-106">Questo metodo potrebbe non essere supportato da tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="aa62b-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="aa62b-107">Il metodo deve restituire 0 se ha esito positivo, 1 se la richiesta non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="aa62b-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="aa62b-108">In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore ValueMap nel metodo.</span><span class="sxs-lookup"><span data-stu-id="aa62b-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="aa62b-109">Le stringhe a cui è stato convertito il contenuto ValueMap possono anche essere specificate nella sottoclasse come qualificatore della matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="aa62b-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa62b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa62b-110">Syntax</span></span>


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a><span data-ttu-id="aa62b-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa62b-111">Parameters</span></span>

<span data-ttu-id="aa62b-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="aa62b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa62b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa62b-113">Return value</span></span>

<span data-ttu-id="aa62b-114">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="aa62b-114">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa62b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa62b-115">Requirements</span></span>



| <span data-ttu-id="aa62b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa62b-116">Requirement</span></span> | <span data-ttu-id="aa62b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="aa62b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa62b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa62b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aa62b-119">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="aa62b-119">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="aa62b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa62b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aa62b-121">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="aa62b-121">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="aa62b-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aa62b-122">Namespace</span></span><br/>                | <span data-ttu-id="aa62b-123">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="aa62b-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aa62b-124">MOF</span><span class="sxs-lookup"><span data-stu-id="aa62b-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa62b-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa62b-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa62b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="aa62b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa62b-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa62b-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa62b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa62b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa62b-129">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="aa62b-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




