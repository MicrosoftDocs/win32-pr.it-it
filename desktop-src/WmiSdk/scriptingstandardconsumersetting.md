---
description: La classe singleton ScriptingStandardConsumerSetting fornisce dati di registrazione comuni a tutte le istanze della classe consumer standard ActiveScriptEventConsumer.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: Classe ScriptingStandardConsumerSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226823"
---
# <a name="scriptingstandardconsumersetting-class"></a><span data-ttu-id="83b9e-103">Classe ScriptingStandardConsumerSetting</span><span class="sxs-lookup"><span data-stu-id="83b9e-103">ScriptingStandardConsumerSetting class</span></span>

<span data-ttu-id="83b9e-104">La classe singleton **ScriptingStandardConsumerSetting** fornisce dati di registrazione comuni a tutte le istanze della classe consumer standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="83b9e-104">The singleton **ScriptingStandardConsumerSetting** class provides registration data that is common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) standard consumer class.</span></span> <span data-ttu-id="83b9e-105">Un'istanza di **ActiveScriptEventConsumer** usa le proprietà **MaximumScripts** e **timeout** .</span><span class="sxs-lookup"><span data-stu-id="83b9e-105">An **ActiveScriptEventConsumer** instance uses the **MaximumScripts** and **Timeout** properties.</span></span> <span data-ttu-id="83b9e-106">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="83b9e-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="83b9e-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="83b9e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="83b9e-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="83b9e-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b9e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83b9e-109">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a><span data-ttu-id="83b9e-110">Members</span><span class="sxs-lookup"><span data-stu-id="83b9e-110">Members</span></span>

<span data-ttu-id="83b9e-111">La classe **ScriptingStandardConsumerSetting** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="83b9e-111">The **ScriptingStandardConsumerSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="83b9e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83b9e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83b9e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83b9e-113">Properties</span></span>

<span data-ttu-id="83b9e-114">La classe **ScriptingStandardConsumerSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="83b9e-114">The **ScriptingStandardConsumerSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83b9e-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="83b9e-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83b9e-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83b9e-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83b9e-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83b9e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83b9e-118">Qualificatori: [**maxlen**](standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="83b9e-118">Qualifiers: [**MaxLen**](standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="83b9e-119">Una breve descrizione di un oggetto a una stringa di riga.</span><span class="sxs-lookup"><span data-stu-id="83b9e-119">A short description of an object a one line string.</span></span> <span data-ttu-id="83b9e-120">Contiene la stringa **ScriptingStandardConsumerSetting** perché si tratta di una classe singleton.</span><span class="sxs-lookup"><span data-stu-id="83b9e-120">Contains the string **ScriptingStandardConsumerSetting** because this is a singleton class.</span></span>

</dd> <dt>

<span data-ttu-id="83b9e-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="83b9e-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83b9e-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83b9e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83b9e-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83b9e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83b9e-124">Descrizione testuale di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="83b9e-124">A text description of an object.</span></span>

</dd> <dt>

<span data-ttu-id="83b9e-125">**MaximumScripts**</span><span class="sxs-lookup"><span data-stu-id="83b9e-125">**MaximumScripts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83b9e-126">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83b9e-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83b9e-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="83b9e-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="83b9e-128">Numero massimo di script eseguiti prima che un consumer avvii una nuova istanza.</span><span class="sxs-lookup"><span data-stu-id="83b9e-128">Maximum number of scripts that are run before a consumer starts a new instance.</span></span> <span data-ttu-id="83b9e-129">Per eliminare le perdite di memoria dagli script, arrestare regolarmente il consumer.</span><span class="sxs-lookup"><span data-stu-id="83b9e-129">To clear out memory leaks from scripts, shut down the consumer regularly.</span></span> <span data-ttu-id="83b9e-130">Il valore predefinito è 300.</span><span class="sxs-lookup"><span data-stu-id="83b9e-130">The default value is 300.</span></span>

</dd> <dt>

<span data-ttu-id="83b9e-131">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="83b9e-131">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83b9e-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="83b9e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83b9e-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="83b9e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83b9e-134">Qualificatori: [**maxlen**](standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="83b9e-134">Qualifiers: [**MaxLen**](standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="83b9e-135">Identificatore per l'oggetto Setting.</span><span class="sxs-lookup"><span data-stu-id="83b9e-135">Identifier for the setting object.</span></span>

</dd> <dt>

<span data-ttu-id="83b9e-136">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="83b9e-136">**Timeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83b9e-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83b9e-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83b9e-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="83b9e-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83b9e-139">Qualificatori: [**unità**](standard-qualifiers.md) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="83b9e-139">Qualifiers: [**units**](standard-qualifiers.md) ("Minutes")</span></span>
</dt> </dl>

<span data-ttu-id="83b9e-140">Numero massimo di minuti prima che un consumer avvii una nuova istanza.</span><span class="sxs-lookup"><span data-stu-id="83b9e-140">Maximum number of minutes before a consumer starts a new instance.</span></span> <span data-ttu-id="83b9e-141">Se è 0 (zero), la proprietà **MaximumScripts** controlla la durata del consumer.</span><span class="sxs-lookup"><span data-stu-id="83b9e-141">If 0 (zero), the **MaximumScripts** property controls the consumer lifetime.</span></span> <span data-ttu-id="83b9e-142">L'intervallo valido per il **timeout** è compreso tra 0 e 71.000 e il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="83b9e-142">The valid range for **Timeout** is 0 through 71,000 and the default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83b9e-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="83b9e-143">Remarks</span></span>

<span data-ttu-id="83b9e-144">La singola istanza della classe **ScriptingStandardConsumerSetting** risiede nello \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="83b9e-144">The single instance of the **ScriptingStandardConsumerSetting** class resides in the root\\cimv2 namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="83b9e-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83b9e-145">Requirements</span></span>



| <span data-ttu-id="83b9e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b9e-146">Requirement</span></span> | <span data-ttu-id="83b9e-147">Valore</span><span class="sxs-lookup"><span data-stu-id="83b9e-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83b9e-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83b9e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="83b9e-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83b9e-149">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="83b9e-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83b9e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="83b9e-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83b9e-151">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="83b9e-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83b9e-152">Namespace</span></span><br/>                | <span data-ttu-id="83b9e-153">\\Sottoscrizione radice</span><span class="sxs-lookup"><span data-stu-id="83b9e-153">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="83b9e-154">MOF</span><span class="sxs-lookup"><span data-stu-id="83b9e-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83b9e-155"><dt>Scrcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83b9e-155"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="83b9e-156">DLL</span><span class="sxs-lookup"><span data-stu-id="83b9e-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83b9e-157"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83b9e-157"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83b9e-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83b9e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b9e-159">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="83b9e-159">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[<span data-ttu-id="83b9e-160">Classi consumer standard</span><span class="sxs-lookup"><span data-stu-id="83b9e-160">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="83b9e-161">Esecuzione di uno script basato su un evento</span><span class="sxs-lookup"><span data-stu-id="83b9e-161">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="83b9e-162">Creazione di un consumer logico</span><span class="sxs-lookup"><span data-stu-id="83b9e-162">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="83b9e-163">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="83b9e-163">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="83b9e-164">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="83b9e-164">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

