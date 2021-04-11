---
description: Contiene le informazioni sulla batteria da impostare.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: Struttura BATTERY_SET_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131674"
---
# <a name="battery_set_information-structure"></a><span data-ttu-id="96231-103">\_ \_ Struttura delle informazioni sui set di batterie</span><span class="sxs-lookup"><span data-stu-id="96231-103">BATTERY\_SET\_INFORMATION structure</span></span>

<span data-ttu-id="96231-104">Contiene le informazioni sulla batteria da impostare.</span><span class="sxs-lookup"><span data-stu-id="96231-104">Contains battery information to be set.</span></span> <span data-ttu-id="96231-105">Questa struttura viene utilizzata con il codice di controllo [**\_ \_ \_ delle informazioni del set di batterie IOCTL**](ioctl-battery-set-information.md) .</span><span class="sxs-lookup"><span data-stu-id="96231-105">This structure is used with the [**IOCTL\_BATTERY\_SET\_INFORMATION**](ioctl-battery-set-information.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="96231-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96231-106">Syntax</span></span>


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="96231-107">Members</span><span class="sxs-lookup"><span data-stu-id="96231-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="96231-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="96231-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="96231-109">Tag della batteria corrente per la batteria.</span><span class="sxs-lookup"><span data-stu-id="96231-109">The current battery tag for the battery.</span></span> <span data-ttu-id="96231-110">Le informazioni per una batteria che corrispondono al tag possono essere restituite solo.</span><span class="sxs-lookup"><span data-stu-id="96231-110">Information for a battery matching the tag can only be returned.</span></span> <span data-ttu-id="96231-111">Ogni volta che questo valore non corrisponde al tag corrente della batteria, la richiesta IOCTL viene completata con il \_ file di errore \_ non \_ trovato, che indica al chiamante che la batteria per cui è presente un tag non esiste più.</span><span class="sxs-lookup"><span data-stu-id="96231-111">Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag for no longer exists.</span></span> <span data-ttu-id="96231-112">Il chiamante può scegliere di usare l'operazione di [**\_ tag di \_ query \_ della batteria IOCTL**](ioctl-battery-query-tag.md) per determinare il tag della batteria appena installata, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="96231-112">The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if one exists.</span></span> <span data-ttu-id="96231-113">Per ulteriori informazioni, vedere la pagina relativa ai [tag della batteria](battery-information.md) .</span><span class="sxs-lookup"><span data-stu-id="96231-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

<span data-ttu-id="96231-114">Quando viene eseguita una richiesta di informazioni sulle query, questo valore viene verificato.</span><span class="sxs-lookup"><span data-stu-id="96231-114">When a query information request is made, this value is verified.</span></span> <span data-ttu-id="96231-115">Inoltre, se la richiesta è in corso mentre questo valore viene modificato, la richiesta viene interrotta con lo stato del file di errore \_ \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="96231-115">In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="96231-116">**InformationLevel**</span><span class="sxs-lookup"><span data-stu-id="96231-116">**InformationLevel**</span></span>
</dt> <dd>

<span data-ttu-id="96231-117">Informazioni sulla batteria da impostare.</span><span class="sxs-lookup"><span data-stu-id="96231-117">The battery information to be set.</span></span> <span data-ttu-id="96231-118">Il tipo di dati nel membro del **buffer** dipende dal valore di questo membro.</span><span class="sxs-lookup"><span data-stu-id="96231-118">The type of data in the **Buffer** member depends on the value of this member.</span></span> <span data-ttu-id="96231-119">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="96231-119">This member can be one of the following values.</span></span>



| <span data-ttu-id="96231-120">Valore</span><span class="sxs-lookup"><span data-stu-id="96231-120">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="96231-121">Significato</span><span class="sxs-lookup"><span data-stu-id="96231-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <span data-ttu-id="96231-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="96231-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="96231-123">Informa il dispositivo della batteria che l'utente ha richiesto la ricarica della batteria in questo momento.</span><span class="sxs-lookup"><span data-stu-id="96231-123">Informs the battery device that the user has requested that the battery should be charging at this time.</span></span> <span data-ttu-id="96231-124">Ad esempio, con uno Smart Battery/Charger/Selector, l'applicazione potrebbe addebitare una batteria alla volta.</span><span class="sxs-lookup"><span data-stu-id="96231-124">For example, with a smart battery/charger/selector, the application could charge one battery at a time.</span></span> <span data-ttu-id="96231-125">Il membro **buffer** di questa struttura viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="96231-125">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <span data-ttu-id="96231-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="96231-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="96231-127">Imposta la regolazione della distorsione critica della batteria.</span><span class="sxs-lookup"><span data-stu-id="96231-127">Sets the battery's critical bias adjustment.</span></span> <span data-ttu-id="96231-128">Si noti che non è previsto che questo valore venga normalmente modificato dal software ed è presente nelle interfacce solo come funzionalità di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="96231-128">Note it is not envisioned that this value would normally be changed by software, and is present in the interfaces only as a maintenance feature.</span></span> <span data-ttu-id="96231-129">Non tutte le batterie possono mantenere questa impostazione e le informazioni sulla batteria devono essere lette per confermare che la batteria ha accettato l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="96231-129">Not all batteries can maintain such a setting, and the battery information should be read to confirm that the battery accepted the setting.</span></span><br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <span data-ttu-id="96231-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="96231-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="96231-131">Informa il dispositivo della batteria che l'utente ha richiesto di scaricare la batteria in questo momento.</span><span class="sxs-lookup"><span data-stu-id="96231-131">Informs the battery device that the user has requested that the battery be discharging at this time.</span></span> <span data-ttu-id="96231-132">Ad esempio, questo può essere usato per indicare la batteria che l'utente attualmente vuole potenziare al sistema.</span><span class="sxs-lookup"><span data-stu-id="96231-132">For example, this could be used to indicate which battery the user currently wants to power the system.</span></span> <span data-ttu-id="96231-133">Il membro **buffer** di questa struttura viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="96231-133">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                          |



 

</dd> <dt>

<span data-ttu-id="96231-134">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="96231-134">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="96231-135">Informazioni sulla batteria da impostare.</span><span class="sxs-lookup"><span data-stu-id="96231-135">The battery information to be set.</span></span> <span data-ttu-id="96231-136">I dati dipendono dal valore di **InformationLevel**.</span><span class="sxs-lookup"><span data-stu-id="96231-136">The data depends on the value of **InformationLevel**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96231-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="96231-137">Remarks</span></span>

<span data-ttu-id="96231-138">La struttura delle **\_ \_ informazioni sul set di batterie** è una struttura a lunghezza variabile ed è necessario allocare un buffer di dimensioni appropriate per le informazioni da includere nella struttura.</span><span class="sxs-lookup"><span data-stu-id="96231-138">The **BATTERY\_SET\_INFORMATION** structure is a variable-length structure, and you must allocate a buffer of suitable size for the information to be included in the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="96231-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96231-139">Requirements</span></span>



| <span data-ttu-id="96231-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="96231-140">Requirement</span></span> | <span data-ttu-id="96231-141">Valore</span><span class="sxs-lookup"><span data-stu-id="96231-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96231-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96231-142">Minimum supported client</span></span><br/> | <span data-ttu-id="96231-143">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="96231-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="96231-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96231-144">Minimum supported server</span></span><br/> | <span data-ttu-id="96231-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96231-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="96231-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96231-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="96231-147"><dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="96231-147"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96231-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96231-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96231-149">**\_ \_ informazioni sui set di batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="96231-149">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

 




