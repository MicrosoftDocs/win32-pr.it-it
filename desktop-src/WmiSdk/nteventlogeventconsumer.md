---
description: La classe NTEventLogEventConsumer registra un messaggio specifico nel registro eventi del sistema operativo quando viene recapitato un evento.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: Classe NTEventLogEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879966"
---
# <a name="nteventlogeventconsumer-class"></a><span data-ttu-id="e7c3c-103">Classe NTEventLogEventConsumer</span><span class="sxs-lookup"><span data-stu-id="e7c3c-103">NTEventLogEventConsumer class</span></span>

<span data-ttu-id="e7c3c-104">La classe **NTEventLogEventConsumer** registra un messaggio specifico nel registro eventi del sistema operativo quando viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-104">The **NTEventLogEventConsumer** class logs a specific message to the operating system event log when an event is delivered to it.</span></span> <span data-ttu-id="e7c3c-105">Questa classe è uno dei consumer di eventi standard forniti da WMI.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="e7c3c-106">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="e7c3c-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7c3c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7c3c-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a><span data-ttu-id="e7c3c-108">Members</span><span class="sxs-lookup"><span data-stu-id="e7c3c-108">Members</span></span>

<span data-ttu-id="e7c3c-109">La classe **NTEventLogEventConsumer** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e7c3c-109">The **NTEventLogEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="e7c3c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7c3c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7c3c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7c3c-111">Properties</span></span>

<span data-ttu-id="e7c3c-112">La classe **NTEventLogEventConsumer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-112">The **NTEventLogEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7c3c-113">**Categoria**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-116">Categoria di eventi.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-116">Event category.</span></span> <span data-ttu-id="e7c3c-117">Si tratta di informazioni specifiche dell'origine e possono avere qualsiasi valore.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-117">This is source-specific information and can have any value.</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-118">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-118">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-119">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-121">ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-121">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="e7c3c-122">WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o il SID Administrator, a seconda del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-122">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="e7c3c-123">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-123">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="e7c3c-124">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="e7c3c-124">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-125">**EventID**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-125">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-126">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-128">Messaggio di evento nella DLL del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-128">Event message in the message DLL.</span></span> <span data-ttu-id="e7c3c-129">Questa proprietà non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-129">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-130">**EventType**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-130">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-133">Tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-133">Type of event.</span></span> <span data-ttu-id="e7c3c-134">Questo parametro può avere uno dei valori elencati nell'elenco seguente, definiti in Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-134">This parameter can have one of the values listed in the following list, which are defined in Winnt.h.</span></span>

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span data-ttu-id="e7c3c-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Registro eventi \_ Operazione riuscita** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="e7c3c-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG\_SUCCESS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="e7c3c-136">Evento riuscito</span><span class="sxs-lookup"><span data-stu-id="e7c3c-136">Successful event</span></span>

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span data-ttu-id="e7c3c-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Registro eventi \_ ERRORE \_ Tpye** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="e7c3c-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG\_ERROR\_TPYE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="e7c3c-138">Evento di errore</span><span class="sxs-lookup"><span data-stu-id="e7c3c-138">Error event</span></span>

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span data-ttu-id="e7c3c-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Registro eventi \_ \_Tipo di avviso** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="e7c3c-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG\_WARNING\_TYPE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="e7c3c-140">Evento di avviso</span><span class="sxs-lookup"><span data-stu-id="e7c3c-140">Warning event</span></span>

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span data-ttu-id="e7c3c-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Registro eventi \_ \_Tipo di informazioni** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="e7c3c-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG\_INFORMATION\_TYPE** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="e7c3c-142">Evento informativo</span><span class="sxs-lookup"><span data-stu-id="e7c3c-142">Information event</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span data-ttu-id="e7c3c-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Registro eventi \_ CONTROLLO \_ riuscito** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="e7c3c-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG\_AUDIT\_SUCCESS** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="e7c3c-144">Tipo di controllo con esito positivo</span><span class="sxs-lookup"><span data-stu-id="e7c3c-144">Success audit type</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span data-ttu-id="e7c3c-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Registro eventi \_ \_Errore di controllo** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="e7c3c-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG\_AUDIT\_FAILURE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="e7c3c-146">Tipo di controllo errore</span><span class="sxs-lookup"><span data-stu-id="e7c3c-146">Failure audit type</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e7c3c-147">**InsertionStringTemplates**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-147">**InsertionStringTemplates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-148">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-148">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-150">Matrice di modelli di stringa standard utilizzata come stringa di inserimento per un record del log eventi.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-150">Array of standard string templates that is used as the insertion string for an event log record.</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-151">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-151">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-154">Nome del computer a cui Strumentazione gestione Windows (WMI) Invia gli eventi.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-154">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="e7c3c-155">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="e7c3c-155">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-156">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-156">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-159">Numero massimo di code per un consumer specifico, in byte.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-159">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="e7c3c-160">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="e7c3c-160">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-161">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-164">Qualificatori: [ **chiave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="e7c3c-164">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-165">Nome univoco di un consumer.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-165">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-166">**NameOfRawDataProperty**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-166">**NameOfRawDataProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-169">Nome della proprietà dell'evento che contiene i dati da passare al parametro *lpRawData* della funzione [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="e7c3c-169">Name of the event property that contains data to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpRawData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-170">**NameOfUserSidProperty**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-170">**NameOfUserSidProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-173">Nome della proprietà dell'evento che contiene un ID di sicurezza (SID) da passare al parametro *lpUserSid* della funzione [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="e7c3c-173">Name of the event property that contains a security identifier (SID) to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpUserSid* parameter.</span></span> <span data-ttu-id="e7c3c-174">La proprietà deve essere una matrice di byte (**Uint8**) o una stringa.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-174">The property must be either an array of bytes (**uint8**) or a string.</span></span> <span data-ttu-id="e7c3c-175">Se si tratta di una matrice di byte, si presuppone che sia un SID.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-175">If it is an array of bytes, it is assumed to be a SID.</span></span> <span data-ttu-id="e7c3c-176">Se è una stringa, si tratta di un SID di stringa convertito in un SID.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-176">If it is a string, it is a string SID that is converted into a SID.</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-177">**NumberOfInsertionStrings**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-177">**NumberOfInsertionStrings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-178">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-180">Numero di elementi nella matrice **InsertionStringTemplates** .</span><span class="sxs-lookup"><span data-stu-id="e7c3c-180">Number of elements in the **InsertionStringTemplates** array.</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-181">**SourceName**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-181">**SourceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-184">Nome dell'origine in cui si trova un messaggio.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-184">Source name where a message is located.</span></span> <span data-ttu-id="e7c3c-185">Si presuppone che il cliente abbia registrato una DLL con i messaggi necessari.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-185">The customer is assumed to have registered a DLL with the necessary messages.</span></span>

> [!Note]  
> <span data-ttu-id="e7c3c-186">Il valore di questo parametro non deve includere i due punti (:) carattere.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-186">The value of this parameter must not include a colon (:) character.</span></span>

 

</dd> <dt>

<span data-ttu-id="e7c3c-187">**UNCServerName**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-187">**UNCServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c3c-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c3c-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7c3c-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7c3c-190">Nome del computer in cui registrare un evento o **null** se l'evento deve essere registrato in un server locale.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-190">Name of the computer on which to log an event, or **NULL** if the event is to be logged on a local server.</span></span>

<span data-ttu-id="e7c3c-191">Per impostazione predefinita, gli utenti autenticati non possono registrare gli eventi nel registro applicazioni in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-191">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="e7c3c-192">Di conseguenza, l'utilizzo di questa proprietà per specificare un computer remoto non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="e7c3c-192">As a result, using this property to specify a remote computer will not work.</span></span> <span data-ttu-id="e7c3c-193">Per informazioni su come modificare la sicurezza del registro eventi, vedere l' [articolo della Knowledge Knowledge](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="e7c3c-193">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7c3c-194">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7c3c-194">Remarks</span></span>

<span data-ttu-id="e7c3c-195">La classe **NTEventLogEventConsumer** è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="e7c3c-195">The **NTEventLogEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="e7c3c-196">Esempio</span><span class="sxs-lookup"><span data-stu-id="e7c3c-196">Examples</span></span>

<span data-ttu-id="e7c3c-197">Per un esempio dell'uso di **NTEventLogEventConsumer** per creare un consumer, vedere [registrazione nel registro eventi NT in base a un evento](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="e7c3c-197">For an example of using **NTEventLogEventConsumer** to create a consumer, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c3c-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7c3c-198">Requirements</span></span>



| <span data-ttu-id="e7c3c-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7c3c-199">Requirement</span></span> | <span data-ttu-id="e7c3c-200">Valore</span><span class="sxs-lookup"><span data-stu-id="e7c3c-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c3c-201">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7c3c-201">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c3c-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7c3c-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7c3c-203">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7c3c-203">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c3c-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7c3c-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7c3c-205">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e7c3c-205">Namespace</span></span><br/>                | <span data-ttu-id="e7c3c-206">\\Sottoscrizione radice</span><span class="sxs-lookup"><span data-stu-id="e7c3c-206">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="e7c3c-207">MOF</span><span class="sxs-lookup"><span data-stu-id="e7c3c-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7c3c-208"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7c3c-208"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7c3c-209">DLL</span><span class="sxs-lookup"><span data-stu-id="e7c3c-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7c3c-210"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7c3c-210"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7c3c-211">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7c3c-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c3c-212">Classi consumer standard</span><span class="sxs-lookup"><span data-stu-id="e7c3c-212">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="e7c3c-213">Creazione di un consumer logico</span><span class="sxs-lookup"><span data-stu-id="e7c3c-213">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="e7c3c-214">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="e7c3c-214">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="e7c3c-215">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="e7c3c-215">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

