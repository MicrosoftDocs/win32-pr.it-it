---
title: Classe SystemRestoreConfig
description: Fornisce le proprietà per controllare la frequenza di creazione di punti di ripristino pianificati e la quantità di spazio su disco utilizzata in ogni unità.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Ripristino del sistema della classe SystemRestoreConfig
- Ripristino del sistema della classe SystemRestoreConfig, descritto
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400717"
---
# <a name="systemrestoreconfig-class"></a><span data-ttu-id="0bb49-105">Classe SystemRestoreConfig</span><span class="sxs-lookup"><span data-stu-id="0bb49-105">SystemRestoreConfig class</span></span>

<span data-ttu-id="0bb49-106">Fornisce le proprietà per controllare la frequenza di creazione di punti di ripristino pianificati e la quantità di spazio su disco utilizzata in ogni unità.</span><span class="sxs-lookup"><span data-stu-id="0bb49-106">Provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed on each drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb49-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bb49-107">Syntax</span></span>

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a><span data-ttu-id="0bb49-108">Members</span><span class="sxs-lookup"><span data-stu-id="0bb49-108">Members</span></span>

<span data-ttu-id="0bb49-109">La classe **SystemRestoreConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0bb49-109">The **SystemRestoreConfig** class has these types of members:</span></span>

-   [<span data-ttu-id="0bb49-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0bb49-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bb49-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0bb49-111">Properties</span></span>

<span data-ttu-id="0bb49-112">La classe **SystemRestoreConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0bb49-112">The **SystemRestoreConfig** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0bb49-113">**DiskPercent**</span><span class="sxs-lookup"><span data-stu-id="0bb49-113">**DiskPercent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb49-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bb49-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bb49-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb49-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bb49-116">Quantità massima di spazio su disco in ogni unità che può essere utilizzata da ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="0bb49-116">The maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="0bb49-117">Questo valore viene specificato come percentuale dello spazio totale dell'unità.</span><span class="sxs-lookup"><span data-stu-id="0bb49-117">This value is specified as a percentage of the total drive space.</span></span> <span data-ttu-id="0bb49-118">Il valore predefinito è 12%.</span><span class="sxs-lookup"><span data-stu-id="0bb49-118">The default value is 12 percent.</span></span>

<span data-ttu-id="0bb49-119">**Windows Vista:** Riceve un valore dal Servizio Copia Shadow del volume (VSS).</span><span class="sxs-lookup"><span data-stu-id="0bb49-119">**Windows Vista:** Receives a value from the Volume Shadow Copy Service (VSS).</span></span> <span data-ttu-id="0bb49-120">Questa è la quantità massima di spazio su disco in ogni unità che può essere usata da ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="0bb49-120">This this is the maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="0bb49-121">Il valore predefinito è pari al 15% dello spazio totale dell'unità o al 30% dello spazio libero disponibile, a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="0bb49-121">The default value is 15 percent of the total drive space or 30 percent of the available free space, whichever is smaller.</span></span>

</dd> <dt>

<span data-ttu-id="0bb49-122">**RPGlobalInterval**</span><span class="sxs-lookup"><span data-stu-id="0bb49-122">**RPGlobalInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb49-123">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bb49-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bb49-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb49-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bb49-125">Intervallo di tempo assoluto in cui vengono creati i checkpoint di sistema pianificati, in secondi.</span><span class="sxs-lookup"><span data-stu-id="0bb49-125">The absolute time interval at which scheduled system checkpoints are created, in seconds.</span></span> <span data-ttu-id="0bb49-126">Il valore predefinito è 86.400 (24 ore).</span><span class="sxs-lookup"><span data-stu-id="0bb49-126">The default value is 86,400 (24 hours).</span></span>

<span data-ttu-id="0bb49-127">**Windows Vista:** Riceve un valore dall'utilità di pianificazione per ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="0bb49-127">**Windows Vista:** Receives a value from the task scheduler for System Restore.</span></span> <span data-ttu-id="0bb49-128">Zero se l'attività è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="0bb49-128">Zero if the task is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0bb49-129">**RPLifeInterval**</span><span class="sxs-lookup"><span data-stu-id="0bb49-129">**RPLifeInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb49-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bb49-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bb49-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb49-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bb49-132">Intervallo di tempo per il quale i punti di ripristino vengono conservati, in secondi.</span><span class="sxs-lookup"><span data-stu-id="0bb49-132">The time interval for which restore points are preserved, in seconds.</span></span> <span data-ttu-id="0bb49-133">Quando un punto di ripristino diventa precedente a questo intervallo specificato, viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="0bb49-133">When a restore point becomes older than this specified interval, it is deleted.</span></span> <span data-ttu-id="0bb49-134">Il limite di validità predefinito è 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="0bb49-134">The default age limit is 90 days.</span></span>

<span data-ttu-id="0bb49-135">**Windows Vista:** Riceve il valore **UINTMAX**.</span><span class="sxs-lookup"><span data-stu-id="0bb49-135">**Windows Vista:** Receives a value of **UINTMAX**.</span></span>

</dd> <dt>

<span data-ttu-id="0bb49-136">**RPSessionInterval**</span><span class="sxs-lookup"><span data-stu-id="0bb49-136">**RPSessionInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bb49-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bb49-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bb49-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bb49-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bb49-139">Intervallo di tempo in secondi durante il quale i checkpoint di sistema pianificati vengono creati durante la sessione.</span><span class="sxs-lookup"><span data-stu-id="0bb49-139">The time interval at which scheduled system checkpoints are created during the session, in seconds.</span></span> <span data-ttu-id="0bb49-140">Il valore predefinito è zero, che indica che la funzionalità è disattivata.</span><span class="sxs-lookup"><span data-stu-id="0bb49-140">The default value is zero, indicating that the feature is turned off.</span></span>

<span data-ttu-id="0bb49-141">**Windows Vista:** Riceve zero se ripristino configurazione di sistema è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0bb49-141">**Windows Vista:** Receives zero if System Restore is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0bb49-142">Esempio</span><span class="sxs-lookup"><span data-stu-id="0bb49-142">Examples</span></span>

<span data-ttu-id="0bb49-143">Il codice di esempio seguente non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0bb49-143">The following sample code is not supported.</span></span> <span data-ttu-id="0bb49-144">Utilizzare lo strumento da riga di comando Vssadmin.exe per modificare la dimensione dello spazio riservato sull'unità.</span><span class="sxs-lookup"><span data-stu-id="0bb49-144">Use the command-line tool Vssadmin.exe to change the size of reserved drive space.</span></span>

<span data-ttu-id="0bb49-145">**Windows XP:** Questo esempio è supportato.</span><span class="sxs-lookup"><span data-stu-id="0bb49-145">**Windows XP:** This sample is supported.</span></span>


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a><span data-ttu-id="0bb49-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bb49-146">Requirements</span></span>



| <span data-ttu-id="0bb49-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb49-147">Requirement</span></span> | <span data-ttu-id="0bb49-148">Valore</span><span class="sxs-lookup"><span data-stu-id="0bb49-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0bb49-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bb49-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb49-150">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0bb49-150">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0bb49-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bb49-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb49-152">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0bb49-152">None supported</span></span><br/>                                                         |
| <span data-ttu-id="0bb49-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0bb49-153">Namespace</span></span><br/>                | <span data-ttu-id="0bb49-154">\\Impostazioni predefinite radice</span><span class="sxs-lookup"><span data-stu-id="0bb49-154">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="0bb49-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0bb49-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bb49-156"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bb49-156"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bb49-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bb49-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb49-158">Punti di ripristino</span><span class="sxs-lookup"><span data-stu-id="0bb49-158">Restore Points</span></span>](restore-points.md)
</dt> <dt>

[<span data-ttu-id="0bb49-159">Strumentazione gestione Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="0bb49-159">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

