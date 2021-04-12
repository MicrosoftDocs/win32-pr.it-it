---
description: La classe SMTPEventConsumer Invia un messaggio di posta elettronica utilizzando Simple Mail Transfer Protocol (SMTP) ogni volta che viene recapitato un evento.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: Classe SMTPEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233810"
---
# <a name="smtpeventconsumer-class"></a><span data-ttu-id="73a37-103">Classe SMTPEventConsumer</span><span class="sxs-lookup"><span data-stu-id="73a37-103">SMTPEventConsumer class</span></span>

<span data-ttu-id="73a37-104">La classe **SMTPEventConsumer** Invia un messaggio di posta elettronica utilizzando Simple Mail Transfer Protocol (SMTP) ogni volta che viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="73a37-104">The **SMTPEventConsumer** class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="73a37-105">Un server SMTP deve esistere sulla rete.</span><span class="sxs-lookup"><span data-stu-id="73a37-105">An SMTP server must exist on the network.</span></span> <span data-ttu-id="73a37-106">La classe SMTPEventConsumer non supporta gli allegati.</span><span class="sxs-lookup"><span data-stu-id="73a37-106">The SMTPEventConsumer class does not support attachments.</span></span> <span data-ttu-id="73a37-107">La codifica del messaggio di posta elettronica deve essere US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="73a37-107">The encoding of the email message must be US-ASCII.</span></span>

<span data-ttu-id="73a37-108">Questa classe è uno dei consumer di eventi standard forniti da WMI.</span><span class="sxs-lookup"><span data-stu-id="73a37-108">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="73a37-109">Per un esempio dell'uso di **SMTPEventConsumer** per creare un consumer, vedere [invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="73a37-109">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="73a37-110">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="73a37-110">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="73a37-111">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="73a37-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="73a37-112">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="73a37-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a37-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73a37-113">Syntax</span></span>

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a><span data-ttu-id="73a37-114">Members</span><span class="sxs-lookup"><span data-stu-id="73a37-114">Members</span></span>

<span data-ttu-id="73a37-115">La classe **SMTPEventConsumer** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="73a37-115">The **SMTPEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="73a37-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73a37-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73a37-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="73a37-117">Properties</span></span>

<span data-ttu-id="73a37-118">La classe **SMTPEventConsumer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="73a37-118">The **SMTPEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73a37-119">**BccLine**</span><span class="sxs-lookup"><span data-stu-id="73a37-119">**BccLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-122">Elenco di indirizzi, separati da virgola o punto e virgola, nel formato di un modello di stringa standard a cui il messaggio viene inviato come copia nascosta.</span><span class="sxs-lookup"><span data-stu-id="73a37-122">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a blind carbon copy.</span></span> <span data-ttu-id="73a37-123">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="73a37-123">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="73a37-124">**CcLine**</span><span class="sxs-lookup"><span data-stu-id="73a37-124">**CcLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-127">Elenco di indirizzi, separati da una virgola o un punto e virgola, nel formato di un modello di stringa standard a cui il messaggio viene inviato come copia carbone.</span><span class="sxs-lookup"><span data-stu-id="73a37-127">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a carbon copy.</span></span> <span data-ttu-id="73a37-128">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="73a37-128">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="73a37-129">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="73a37-129">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-130">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="73a37-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="73a37-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-132">ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="73a37-132">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="73a37-133">WMI archivia il SID dell'utente che crea un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) o il SID Administrator, a seconda del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="73a37-133">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="73a37-134">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.</span><span class="sxs-lookup"><span data-stu-id="73a37-134">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="73a37-135">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="73a37-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="73a37-136">**FromLine**</span><span class="sxs-lookup"><span data-stu-id="73a37-136">**FromLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-139">Dalla riga di un messaggio di posta elettronica nel formato di un modello di stringa standard.</span><span class="sxs-lookup"><span data-stu-id="73a37-139">From line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="73a37-140">Se è **null**, una riga da viene costruita nel formato "WinMgmt@*machineName*".</span><span class="sxs-lookup"><span data-stu-id="73a37-140">If **NULL**, a From line is constructed in the form of "WinMgmt@*MachineName*".</span></span>

</dd> <dt>

<span data-ttu-id="73a37-141">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="73a37-141">**HeaderFields**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-142">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="73a37-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73a37-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-144">Matrice di campi di intestazione che vengono inseriti in un messaggio di posta elettronica senza interpretazione.</span><span class="sxs-lookup"><span data-stu-id="73a37-144">Array of header fields that are inserted into an email message without interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="73a37-145">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="73a37-145">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-148">Nome del computer a cui Strumentazione gestione Windows (WMI) Invia gli eventi.</span><span class="sxs-lookup"><span data-stu-id="73a37-148">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="73a37-149">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="73a37-149">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="73a37-150">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="73a37-150">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73a37-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-153">Numero massimo di code per un consumer specifico, in byte.</span><span class="sxs-lookup"><span data-stu-id="73a37-153">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="73a37-154">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="73a37-154">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="73a37-155">**Messaggio**</span><span class="sxs-lookup"><span data-stu-id="73a37-155">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-158">Modello di stringa standard che contiene il corpo di un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="73a37-158">Standard string template that contains the body of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="73a37-159">**Nome**</span><span class="sxs-lookup"><span data-stu-id="73a37-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73a37-162">Qualificatori: [ **chiave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="73a37-162">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="73a37-163">Identificatore univoco del consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="73a37-163">Unique identifier for the event consumer.</span></span>

</dd> <dt>

<span data-ttu-id="73a37-164">**ReplyToLine**</span><span class="sxs-lookup"><span data-stu-id="73a37-164">**ReplyToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-167">Risposta alla riga di un messaggio di posta elettronica nel formato di un modello di stringa standard.</span><span class="sxs-lookup"><span data-stu-id="73a37-167">Reply-to line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="73a37-168">Se è **null**, non viene utilizzata alcuna riga di risposta.</span><span class="sxs-lookup"><span data-stu-id="73a37-168">If **NULL**, no Reply-to line is used.</span></span>

</dd> <dt>

<span data-ttu-id="73a37-169">**SMTPServer**</span><span class="sxs-lookup"><span data-stu-id="73a37-169">**SMTPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-172">Nome del server SMTP tramite il quale viene inviato un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="73a37-172">Name of the SMTP server through which an email is sent.</span></span> <span data-ttu-id="73a37-173">I nomi consentiti sono un indirizzo IP o un nome DNS o NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="73a37-173">Permissible names are an IP address, or a DNS or NetBIOS name.</span></span> <span data-ttu-id="73a37-174">Questa proprietà non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="73a37-174">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="73a37-175">**Oggetto**</span><span class="sxs-lookup"><span data-stu-id="73a37-175">**Subject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-178">Modello di stringa standard che contiene l'oggetto di un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="73a37-178">Standard string template that contains the subject of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="73a37-179">**ToLine**</span><span class="sxs-lookup"><span data-stu-id="73a37-179">**ToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73a37-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="73a37-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73a37-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="73a37-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73a37-182">Elenco di indirizzi, separati da virgola o punto e virgola, nel formato di un modello di stringa standard che identifica la posizione in cui deve essere inviato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="73a37-182">A list of addresses, separated by a comma or semicolon, in the format of a standard string template that identifies where the message is to be sent.</span></span> <span data-ttu-id="73a37-183">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="73a37-183">For more information, see the Remarks section of this topic.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73a37-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="73a37-184">Remarks</span></span>

<span data-ttu-id="73a37-185">La classe SMTPEventConsumer è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="73a37-185">The SMTPEventConsumer class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="73a37-186">Alcune delle proprietà **ToLine**, **CcLine** o **BccLine** possono essere **null**, ma non tutte possono essere **null**.</span><span class="sxs-lookup"><span data-stu-id="73a37-186">Some of the **ToLine**, **CcLine**, or **BccLine** properties can be **NULL**, but they cannot all be **NULL**.</span></span>

<span data-ttu-id="73a37-187">La ricezione di un codice di errore restituito dal servizio SMTP viene considerata un errore.</span><span class="sxs-lookup"><span data-stu-id="73a37-187">Receiving an error return code from the SMTP service is considered a failure.</span></span>

## <a name="examples"></a><span data-ttu-id="73a37-188">Esempio</span><span class="sxs-lookup"><span data-stu-id="73a37-188">Examples</span></span>

<span data-ttu-id="73a37-189">Per un esempio dell'uso di **SMTPEventConsumer** per creare un consumer, vedere [invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="73a37-189">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="73a37-190">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="73a37-190">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73a37-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73a37-191">Requirements</span></span>



| <span data-ttu-id="73a37-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="73a37-192">Requirement</span></span> | <span data-ttu-id="73a37-193">Valore</span><span class="sxs-lookup"><span data-stu-id="73a37-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73a37-194">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73a37-194">Minimum supported client</span></span><br/> | <span data-ttu-id="73a37-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73a37-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73a37-196">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73a37-196">Minimum supported server</span></span><br/> | <span data-ttu-id="73a37-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73a37-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73a37-198">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="73a37-198">Namespace</span></span><br/>                | <span data-ttu-id="73a37-199">\\Sottoscrizione radice</span><span class="sxs-lookup"><span data-stu-id="73a37-199">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="73a37-200">MOF</span><span class="sxs-lookup"><span data-stu-id="73a37-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73a37-201"><dt>Smtpcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73a37-201"><dt>Smtpcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="73a37-202">DLL</span><span class="sxs-lookup"><span data-stu-id="73a37-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73a37-203"><dt>Smtpcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73a37-203"><dt>Smtpcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a37-204">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73a37-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a37-205">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="73a37-205">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="73a37-206">Classi consumer standard</span><span class="sxs-lookup"><span data-stu-id="73a37-206">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="73a37-207">Invio di messaggi di posta elettronica in base a un evento</span><span class="sxs-lookup"><span data-stu-id="73a37-207">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="73a37-208">Creazione di un consumer logico</span><span class="sxs-lookup"><span data-stu-id="73a37-208">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="73a37-209">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="73a37-209">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 




