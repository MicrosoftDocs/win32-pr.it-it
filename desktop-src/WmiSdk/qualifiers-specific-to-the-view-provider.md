---
description: Di seguito sono elencati i qualificatori utilizzati per definire le classi del provider di visualizzazione.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Qualificatori specifici del provider di visualizzazione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 76f28e4ba3433c168e1d0bf86887ee93df953444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232903"
---
# <a name="qualifiers-specific-to-the-view-provider"></a><span data-ttu-id="d01d4-103">Qualificatori specifici del provider di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="d01d4-103">Qualifiers Specific to the View Provider</span></span>

<span data-ttu-id="d01d4-104">Di seguito sono elencati i qualificatori utilizzati per definire le classi del provider di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d01d4-104">The following lists the qualifiers use to define View Provider classes.</span></span>

> [!Note]  
> <span data-ttu-id="d01d4-105">La classe del provider di visualizzazione supporta solo i nomi NetBIOS quando si utilizzano riferimenti remoti.</span><span class="sxs-lookup"><span data-stu-id="d01d4-105">The View provider class only supports NetBIOS names when using remote references.</span></span> <span data-ttu-id="d01d4-106">Se si usa un indirizzo IP o un nome DNS in un riferimento remoto, la connessione ha esito negativo con un errore 0x800706ba.</span><span class="sxs-lookup"><span data-stu-id="d01d4-106">If you use an IP address or a DNS name in a remote reference, then the connection fails with a 0x800706ba error.</span></span>

 

<dt>

<span data-ttu-id="d01d4-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Diretto**</span><span class="sxs-lookup"><span data-stu-id="d01d4-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Direct**</span></span>
</dt> <dd>

<span data-ttu-id="d01d4-108">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d01d4-108">Data type: **boolean**</span></span>

<span data-ttu-id="d01d4-109">Utilizzato con le proprietà di associazione di visualizzazione per impedire il mapping dei riferimenti di associazione a un riferimento alla visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d01d4-109">Used with view association properties to prevent association references from being mapped to a view reference.</span></span>

<span data-ttu-id="d01d4-110">Nell'esempio seguente viene definita la proprietà **GroupComponent** come riferimento di associazione di cui non è stato eseguito il mapping nel riferimento alla vista.</span><span class="sxs-lookup"><span data-stu-id="d01d4-110">The following example defines the property **GroupComponent** as an association reference that is not mapped in the view reference.</span></span>


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span data-ttu-id="d01d4-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span><span class="sxs-lookup"><span data-stu-id="d01d4-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span></span>
</dt> <dd>

<span data-ttu-id="d01d4-112">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d01d4-112">Data type: **boolean**</span></span>

<span data-ttu-id="d01d4-113">Valore predefinito per una proprietà della classe di visualizzazione basata su una proprietà della classe di origine con un valore predefinito diverso.</span><span class="sxs-lookup"><span data-stu-id="d01d4-113">Default value for a view class property based on a source class property with a different default value.</span></span> <span data-ttu-id="d01d4-114">La classe di origine sottostante è implicita nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d01d4-114">The underlying source class is implied by the view.</span></span>

<span data-ttu-id="d01d4-115">Ad esempio, la classe di origine [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) ha una proprietà [booleana](boolean.md) **RunRepeatedly** che indica se il processo deve essere eseguito periodicamente o solo una volta.</span><span class="sxs-lookup"><span data-stu-id="d01d4-115">For example, the source class [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) has a [boolean](boolean.md) property **RunRepeatedly** that indicates whether the job is to be carried out periodically or one time only.</span></span> <span data-ttu-id="d01d4-116">Il valore predefinito di **RunRepeatedly** non è true per **\_ ScheduledJob Win32**, ma è true per la classe di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d01d4-116">The default value of **RunRepeatedly** is not True for **Win32\_ScheduledJob**, but is True for the view class.</span></span>


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span data-ttu-id="d01d4-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span><span class="sxs-lookup"><span data-stu-id="d01d4-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span></span>
</dt> <dd>

<span data-ttu-id="d01d4-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01d4-118">Data type: **string**</span></span>

<span data-ttu-id="d01d4-119">Definisce la modalità di Unione delle istanze della classe di origine nelle classi di visualizzazione join.</span><span class="sxs-lookup"><span data-stu-id="d01d4-119">Defines how source class instances are joined in join view classes.</span></span> <span data-ttu-id="d01d4-120">Nell'esempio seguente viene illustrato come utilizzare il qualificatore **JoinOn** per unire due classi di origine.</span><span class="sxs-lookup"><span data-stu-id="d01d4-120">The following example shows how to use the **JoinOn** qualifier to join two source classes.</span></span>


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span data-ttu-id="d01d4-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span><span class="sxs-lookup"><span data-stu-id="d01d4-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span></span>
</dt> <dd>

<span data-ttu-id="d01d4-122">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d01d4-122">Data type: **string array**</span></span>

<span data-ttu-id="d01d4-123">Metodo di origine da eseguire per il metodo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d01d4-123">Source method to execute for the view method.</span></span> <span data-ttu-id="d01d4-124">Per una sintassi simile, vedere [qualificatore PropertySources](propertysources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="d01d4-124">For similar syntax, see [PropertySources Qualifier](propertysources-qualifier.md).</span></span> <span data-ttu-id="d01d4-125">La firma del metodo deve corrispondere esattamente alla firma della classe di origine.</span><span class="sxs-lookup"><span data-stu-id="d01d4-125">The signature of the method must match the signature of the source class exactly.</span></span> <span data-ttu-id="d01d4-126">Copiare la firma del metodo dal file MOF che definisce la classe di origine.</span><span class="sxs-lookup"><span data-stu-id="d01d4-126">Copy the method signature from the MOF file that defines the source class.</span></span> <span data-ttu-id="d01d4-127">Nell'esempio seguente viene definito un metodo del metodo [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) di [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="d01d4-127">The example below defines a method from the [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) method of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span></span>


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



<span data-ttu-id="d01d4-128">Questo qualificatore è valido solo quando viene utilizzato con le viste Union.</span><span class="sxs-lookup"><span data-stu-id="d01d4-128">This qualifier is only valid when it is used with union views.</span></span>

</dd> <dt>

<span data-ttu-id="d01d4-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d01d4-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="d01d4-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d01d4-130">Data type: **string**</span></span>

<span data-ttu-id="d01d4-131">Query WQL per filtrare le istanze dopo che sono state aggiunte a una classe join.</span><span class="sxs-lookup"><span data-stu-id="d01d4-131">WQL query to filter instances after they have been joined in a join class.</span></span>

</dd> <dt>

<span data-ttu-id="d01d4-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d01d4-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="d01d4-133">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d01d4-133">Data type: **string array**</span></span>

<span data-ttu-id="d01d4-134">Proprietà di origine da cui una proprietà della classe di visualizzazione Ottiene i dati.</span><span class="sxs-lookup"><span data-stu-id="d01d4-134">Source properties from which a view class property gets data.</span></span>

</dd> <dt>

<span data-ttu-id="d01d4-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Unione**</span><span class="sxs-lookup"><span data-stu-id="d01d4-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**</span></span>
</dt> <dd>

<span data-ttu-id="d01d4-136">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d01d4-136">Data type: **boolean**</span></span>

<span data-ttu-id="d01d4-137">Indica se si sta definendo una classe Union.</span><span class="sxs-lookup"><span data-stu-id="d01d4-137">Indicates whether you are defining a union class.</span></span> <span data-ttu-id="d01d4-138">Le viste Unione contengono istanze basate sull'Unione delle istanze di origine.</span><span class="sxs-lookup"><span data-stu-id="d01d4-138">Union views contain instances based on the union of source instances.</span></span> <span data-ttu-id="d01d4-139">È ad esempio possibile dichiarare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d01d4-139">For example, you might declare the following:</span></span>


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span data-ttu-id="d01d4-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d01d4-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="d01d4-141">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d01d4-141">Data type: **string array**</span></span>

<span data-ttu-id="d01d4-142">Set di query di WMI Query Language (WQL) che definiscono le istanze e le proprietà di origine utilizzate in una classe di visualizzazione specifica.</span><span class="sxs-lookup"><span data-stu-id="d01d4-142">Set of WMI Query Language (WQL) queries that define the source instances and properties used in a specific view class.</span></span> <span data-ttu-id="d01d4-143">La corrispondenza posizionale di tutti i qualificatori di matrice è importante.</span><span class="sxs-lookup"><span data-stu-id="d01d4-143">Positional correspondence of all the array qualifiers is important.</span></span>

</dd> <dt>

<span data-ttu-id="d01d4-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d01d4-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="d01d4-145">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d01d4-145">Data type: **string array**</span></span>

<span data-ttu-id="d01d4-146">Spazi dei nomi in cui si trovano le istanze di origine.</span><span class="sxs-lookup"><span data-stu-id="d01d4-146">Namespaces where the source instances are located.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d01d4-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d01d4-147">Requirements</span></span>



| <span data-ttu-id="d01d4-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01d4-148">Requirement</span></span> | <span data-ttu-id="d01d4-149">Valore</span><span class="sxs-lookup"><span data-stu-id="d01d4-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d01d4-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d01d4-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d01d4-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d01d4-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d01d4-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d01d4-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d01d4-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d01d4-153">Windows Server 2008</span></span><br/> |



 

