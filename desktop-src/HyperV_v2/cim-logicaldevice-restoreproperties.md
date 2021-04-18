---
description: Richiede che il dispositivo ristabilisca la configurazione, l'installazione e/o le informazioni sullo stato da un archivio di backup.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Metodo RestoreProperties della classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317218"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="0f802-103">Metodo RestoreProperties della classe CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="0f802-103">RestoreProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="0f802-104">Richiede che il dispositivo ristabilisca la configurazione, l'installazione e/o le informazioni sullo stato da un archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="0f802-104">Requests that the Device re-establish its configuration, setup and/or state information from a backing store.</span></span> <span data-ttu-id="0f802-105">Lo scopo è quello di acquisire queste informazioni in un momento precedente (tramite il metodo SaveProperties) e usarle per restituire un dispositivo a questa "condizione" precedente.</span><span class="sxs-lookup"><span data-stu-id="0f802-105">The intent is to capture this information at an earlier time (via the SaveProperties method), and use it to return a Device to this earlier "condition".</span></span> <span data-ttu-id="0f802-106">Questo metodo potrebbe non essere supportato da tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0f802-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="0f802-107">Il metodo deve restituire 0 se ha esito positivo, 1 se la richiesta non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="0f802-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="0f802-108">In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore ValueMap nel metodo.</span><span class="sxs-lookup"><span data-stu-id="0f802-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="0f802-109">Le stringhe a cui è stato convertito il contenuto ValueMap possono anche essere specificate nella sottoclasse come qualificatore della matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="0f802-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f802-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f802-110">Syntax</span></span>


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a><span data-ttu-id="0f802-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f802-111">Parameters</span></span>

<span data-ttu-id="0f802-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0f802-112">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f802-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f802-113">Requirements</span></span>



| <span data-ttu-id="0f802-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f802-114">Requirement</span></span> | <span data-ttu-id="0f802-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0f802-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f802-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f802-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0f802-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0f802-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0f802-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f802-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0f802-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0f802-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0f802-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0f802-120">Namespace</span></span><br/>                | <span data-ttu-id="0f802-121">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0f802-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0f802-122">MOF</span><span class="sxs-lookup"><span data-stu-id="0f802-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f802-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f802-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f802-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0f802-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f802-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f802-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f802-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f802-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f802-127">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0f802-127">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




