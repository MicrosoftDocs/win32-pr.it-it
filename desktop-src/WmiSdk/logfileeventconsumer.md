---
description: La classe LogFileEventConsumer scrive stringhe personalizzate in un file di log di testo quando gli eventi vengono recapitati.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: Classe LogFileEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310342"
---
# <a name="logfileeventconsumer-class"></a><span data-ttu-id="1ce33-103">Classe LogFileEventConsumer</span><span class="sxs-lookup"><span data-stu-id="1ce33-103">LogFileEventConsumer class</span></span>

<span data-ttu-id="1ce33-104">La classe **LogFileEventConsumer** scrive stringhe personalizzate in un file di log di testo quando gli eventi vengono recapitati.</span><span class="sxs-lookup"><span data-stu-id="1ce33-104">The **LogFileEventConsumer** class writes customized strings to a text log file when events are delivered to it.</span></span> <span data-ttu-id="1ce33-105">Le stringhe sono separate dalle sequenze di fine riga.</span><span class="sxs-lookup"><span data-stu-id="1ce33-105">The strings are separated by end-of-line sequences.</span></span> <span data-ttu-id="1ce33-106">Questa classe è uno dei consumer di eventi standard forniti da WMI.</span><span class="sxs-lookup"><span data-stu-id="1ce33-106">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="1ce33-107">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="1ce33-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce33-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ce33-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a><span data-ttu-id="1ce33-109">Members</span><span class="sxs-lookup"><span data-stu-id="1ce33-109">Members</span></span>

<span data-ttu-id="1ce33-110">La classe **LogFileEventConsumer** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1ce33-110">The **LogFileEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="1ce33-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1ce33-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ce33-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1ce33-112">Properties</span></span>

<span data-ttu-id="1ce33-113">La classe **LogFileEventConsumer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1ce33-113">The **LogFileEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ce33-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="1ce33-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce33-115">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1ce33-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1ce33-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ce33-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ce33-117">ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="1ce33-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="1ce33-118">WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o il SID Administrator, a seconda del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1ce33-118">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="1ce33-119">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.</span><span class="sxs-lookup"><span data-stu-id="1ce33-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="1ce33-120">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="1ce33-120">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ce33-121">**Filename**</span><span class="sxs-lookup"><span data-stu-id="1ce33-121">**Filename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce33-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ce33-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ce33-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ce33-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ce33-124">Nome di un file che include il percorso a cui vengono accodate le voci di log.</span><span class="sxs-lookup"><span data-stu-id="1ce33-124">Name of a file that includes the path to which the log entries are appended.</span></span> <span data-ttu-id="1ce33-125">Se il file non esiste, **LogFileEventConsumer** tenta di crearlo.</span><span class="sxs-lookup"><span data-stu-id="1ce33-125">If the file does not exist, **LogFileEventConsumer** attempts to create it.</span></span> <span data-ttu-id="1ce33-126">Il consumer ha esito negativo quando il percorso non esiste o quando l'utente che crea il consumer non dispone delle autorizzazioni di scrittura per il file o il percorso.</span><span class="sxs-lookup"><span data-stu-id="1ce33-126">The consumer fails when the path does not exist, or when the user who creates the consumer does not have write permissions for the file or path.</span></span>

</dd> <dt>

<span data-ttu-id="1ce33-127">**Unicode**</span><span class="sxs-lookup"><span data-stu-id="1ce33-127">**IsUnicode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce33-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1ce33-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ce33-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ce33-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ce33-130">Se **true**, il file di log è un file di testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ce33-130">If **TRUE**, the log file is a Unicode text file.</span></span> <span data-ttu-id="1ce33-131">Se **false**, il file di log è un file di testo di codice multibyte.</span><span class="sxs-lookup"><span data-stu-id="1ce33-131">If **FALSE**, the log file is a multibyte code text file.</span></span> <span data-ttu-id="1ce33-132">Se il file esiste, questa proprietà viene ignorata e viene utilizzata l'impostazione del file corrente.</span><span class="sxs-lookup"><span data-stu-id="1ce33-132">If the file exists, this property is ignored and the current file setting is used.</span></span> <span data-ttu-id="1ce33-133">Se, ad esempio, il valore **di Unicode è** **false**, ma il file esistente è un file Unicode, viene utilizzato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ce33-133">For example, if **IsUnicode** is **FALSE**, but the existing file is a Unicode file, then Unicode is used.</span></span> <span data-ttu-id="1ce33-134">Se la codifica è **true**, ma il file è di tipo multibyte **, viene utilizzato** il codice multibyte.</span><span class="sxs-lookup"><span data-stu-id="1ce33-134">If **IsUnicode** is **TRUE**, but the file is multibyte code, then multibyte code is used.</span></span>

</dd> <dt>

<span data-ttu-id="1ce33-135">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="1ce33-135">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce33-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ce33-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ce33-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ce33-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ce33-138">Nome del computer a cui Strumentazione gestione Windows (WMI) Invia gli eventi.</span><span class="sxs-lookup"><span data-stu-id="1ce33-138">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="1ce33-139">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="1ce33-139">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ce33-140">**MaximumFileSize**</span><span class="sxs-lookup"><span data-stu-id="1ce33-140">**MaximumFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce33-141">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ce33-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ce33-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ce33-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ce33-143">Dimensioni massime di un file di log in byte.</span><span class="sxs-lookup"><span data-stu-id="1ce33-143">Maximum size of a log file in bytes.</span></span> <span data-ttu-id="1ce33-144">Se il file primario supera la dimensione massima, il contenuto viene spostato in un altro file e il file primario viene svuotato.</span><span class="sxs-lookup"><span data-stu-id="1ce33-144">If the primary file exceeds its maximum size, the contents are moved to a different file and the primary file is emptied.</span></span> <span data-ttu-id="1ce33-145">Il valore 0 (zero) indica che non è previsto alcun limite per le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1ce33-145">A value of 0 (zero) means there is no size limit.</span></span> <span data-ttu-id="1ce33-146">Il valore predefinito è 65.535 byte.</span><span class="sxs-lookup"><span data-stu-id="1ce33-146">The default value is 65,535 bytes.</span></span> <span data-ttu-id="1ce33-147">Le dimensioni del file vengono verificate prima di un'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="1ce33-147">The size of the file is checked before a write operation.</span></span> <span data-ttu-id="1ce33-148">Pertanto, è possibile avere un file leggermente più grande del limite di dimensioni specificato.</span><span class="sxs-lookup"><span data-stu-id="1ce33-148">Therefore, you can have a file that is slightly larger than the specified size limit.</span></span> <span data-ttu-id="1ce33-149">L'operazione di scrittura successiva la intercetta e avvia un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="1ce33-149">The next write operation catches it and starts a new file.</span></span>

<span data-ttu-id="1ce33-150">L'elenco seguente identifica la struttura di denominazione per il file di backup:</span><span class="sxs-lookup"><span data-stu-id="1ce33-150">The following list identifies the naming structure for the backup file:</span></span>

-   <span data-ttu-id="1ce33-151">Se il nome file originale è 8,3, l'estensione viene sostituita da una stringa nel formato "001", "002" e così via con il numero più piccolo maggiore di tutti i numeri scelti e usati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="1ce33-151">If the original filename is 8.3, the extension is replaced by a string in the format of "001", "002", and so on with the smallest number larger than all the previously used and chosen numbers.</span></span> <span data-ttu-id="1ce33-152">Se si usa "999", il numero scelto è il numero inutilizzato più piccolo.</span><span class="sxs-lookup"><span data-stu-id="1ce33-152">If "999" is used, then the number chosen is the smallest unused number.</span></span>
-   <span data-ttu-id="1ce33-153">Se il nome file originale non è 8,3, viene aggiunta una stringa nel formato "001", "002" e così via al nome del file.</span><span class="sxs-lookup"><span data-stu-id="1ce33-153">If the original filename is not 8.3, a string in the format of "001", "002", and so on is appended to the file name.</span></span>

<span data-ttu-id="1ce33-154">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1ce33-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1ce33-155">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="1ce33-155">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce33-156">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ce33-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ce33-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ce33-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ce33-158">Numero massimo di code per un consumer specifico, in byte.</span><span class="sxs-lookup"><span data-stu-id="1ce33-158">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="1ce33-159">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="1ce33-159">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ce33-160">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1ce33-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce33-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ce33-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ce33-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ce33-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ce33-163">Qualificatori: [ **chiave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="1ce33-163">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="1ce33-164">Nome univoco del consumer.</span><span class="sxs-lookup"><span data-stu-id="1ce33-164">Unique name for this consumer.</span></span>

</dd> <dt>

<span data-ttu-id="1ce33-165">**Text**</span><span class="sxs-lookup"><span data-stu-id="1ce33-165">**Text**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce33-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1ce33-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ce33-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1ce33-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ce33-168">[Modello](using-standard-string-templates.md) di stringa standard per il testo di una voce di log.</span><span class="sxs-lookup"><span data-stu-id="1ce33-168">Standard string [template](using-standard-string-templates.md) for the text of a log entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ce33-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ce33-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1ce33-170">Il **LogFileEventConsumer** non protegge il file di log.</span><span class="sxs-lookup"><span data-stu-id="1ce33-170">The **LogFileEventConsumer** does not secure the log file.</span></span> <span data-ttu-id="1ce33-171">Pertanto, quando si configura **LogFileEventConsumer**, è importante specificare una directory protetta per il livello richiesto.</span><span class="sxs-lookup"><span data-stu-id="1ce33-171">Therefore, when you configure the **LogFileEventConsumer**, it is important to specify a directory that is secured to the level that you require.</span></span>

 

<span data-ttu-id="1ce33-172">La classe **LogFileEventConsumer** è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="1ce33-172">The **LogFileEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="1ce33-173">Esempio</span><span class="sxs-lookup"><span data-stu-id="1ce33-173">Examples</span></span>

<span data-ttu-id="1ce33-174">Per un esempio dell'uso di **LogFileEventConsumer** per creare un consumer, vedere [scrittura in un file di log in base a un evento](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="1ce33-174">For an example of using **LogFileEventConsumer** to create a consumer, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce33-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ce33-175">Requirements</span></span>



| <span data-ttu-id="1ce33-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ce33-176">Requirement</span></span> | <span data-ttu-id="1ce33-177">Valore</span><span class="sxs-lookup"><span data-stu-id="1ce33-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce33-178">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ce33-178">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce33-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ce33-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1ce33-180">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ce33-180">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce33-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ce33-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1ce33-182">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1ce33-182">Namespace</span></span><br/>                | <span data-ttu-id="1ce33-183">\\Sottoscrizione radice</span><span class="sxs-lookup"><span data-stu-id="1ce33-183">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="1ce33-184">MOF</span><span class="sxs-lookup"><span data-stu-id="1ce33-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ce33-185"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ce33-185"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ce33-186">DLL</span><span class="sxs-lookup"><span data-stu-id="1ce33-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ce33-187"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ce33-187"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce33-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ce33-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce33-189">Classi consumer standard</span><span class="sxs-lookup"><span data-stu-id="1ce33-189">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="1ce33-190">Scrittura in un file di log in base a un evento</span><span class="sxs-lookup"><span data-stu-id="1ce33-190">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="1ce33-191">Creazione di un consumer logico</span><span class="sxs-lookup"><span data-stu-id="1ce33-191">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="1ce33-192">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="1ce33-192">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="1ce33-193">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="1ce33-193">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

