---
description: Superclasse concreta per le notifiche di avviso CIM.
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: Classe CIM_AlertIndication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1916705ee696c949dba2a557f7077ade8db7ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305677"
---
# <a name="cim_alertindication-class"></a><span data-ttu-id="74885-103">CIM \_ AlertIndication (classe)</span><span class="sxs-lookup"><span data-stu-id="74885-103">CIM\_AlertIndication class</span></span>

<span data-ttu-id="74885-104">Superclasse concreta per le notifiche di avviso CIM.</span><span class="sxs-lookup"><span data-stu-id="74885-104">A concrete superclass for CIM alert notifications.</span></span> <span data-ttu-id="74885-105">**CIM \_ AlertIndication** è un tipo specializzato di classe di **\_ indicazione CIM** che contiene informazioni sulla gravità, la cause, le azioni consigliate e altri dati per un evento reale.</span><span class="sxs-lookup"><span data-stu-id="74885-105">**CIM\_AlertIndication** is a specialized type of **CIM\_Indication** class that contains information about the severity, cause, recommended actions, and other data for a real world event.</span></span> <span data-ttu-id="74885-106">Questo evento e i relativi dati possono essere modellati o meno nella gerarchia di classi CIM.</span><span class="sxs-lookup"><span data-stu-id="74885-106">This event and its data may or may not be modeled in the CIM class hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="74885-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74885-107">Syntax</span></span>

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a><span data-ttu-id="74885-108">Members</span><span class="sxs-lookup"><span data-stu-id="74885-108">Members</span></span>

<span data-ttu-id="74885-109">La classe **CIM \_ AlertIndication** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="74885-109">The **CIM\_AlertIndication** class has these types of members:</span></span>

-   [<span data-ttu-id="74885-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74885-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74885-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74885-111">Properties</span></span>

<span data-ttu-id="74885-112">La classe **CIM \_ AlertIndication** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="74885-112">The **CIM\_AlertIndication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74885-113">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="74885-113">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74885-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74885-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-116">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingManagedElement**","**CIM \_ AlertIndication**.**OtherAlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="74885-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingManagedElement**", "**CIM\_AlertIndication**.**OtherAlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-117">Formato della proprietà **AlertingManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="74885-117">The format of the **AlertingManagedElement** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74885-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="74885-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="74885-119">Il formato è sconosciuto o non interpretabile in maniera significativa da un'applicazione client CIM.</span><span class="sxs-lookup"><span data-stu-id="74885-119">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74885-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="74885-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="74885-121">Il formato è definito dal valore della proprietà OtherAlertingElementFormat.</span><span class="sxs-lookup"><span data-stu-id="74885-121">The format is defined by the value of the OtherAlertingElementFormat property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="74885-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="74885-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74885-123">Il formato è un CIMObjectPath, che specifica un'istanza nello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="74885-123">The format is a CIMObjectPath, specifying an instance in the CIM Schema.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74885-124">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="74885-124">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-127">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="74885-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-128">Informazioni di identificazione dell'entità, ad esempio l'istanza, per la quale viene generata questa indicazione.</span><span class="sxs-lookup"><span data-stu-id="74885-128">The identifying information of the entity (ie, the instance) for which this Indication is generated.</span></span> <span data-ttu-id="74885-129">La proprietà contiene il percorso di un'istanza, codificata come parametro di stringa, se l'istanza è modellata nello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="74885-129">The property contains the path of an instance, encoded as a string parameter - if the instance is modeled in the CIM Schema.</span></span> <span data-ttu-id="74885-130">In caso contrario, la proprietà contiene una stringa di identificazione che assegna un nome all'entità per la quale viene generato l'avviso.</span><span class="sxs-lookup"><span data-stu-id="74885-130">If not a CIM instance, the property contains some identifying string that names the entity for which the Alert is generated.</span></span> <span data-ttu-id="74885-131">Il percorso o la stringa di identificazione viene formattato in base alla proprietà AlertingElementFormat.</span><span class="sxs-lookup"><span data-stu-id="74885-131">The path or identifying string is formatted per the AlertingElementFormat property.</span></span>

</dd> <dt>

<span data-ttu-id="74885-132">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="74885-132">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74885-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74885-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-135">Qualificatori: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Tipo di evento ")</span><span class="sxs-lookup"><span data-stu-id="74885-135">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Event type")</span></span>
</dt> </dl>

<span data-ttu-id="74885-136">Classificazione primaria dell'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74885-136">The primary classification of the indication.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74885-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="74885-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="74885-138">\- Altri.</span><span class="sxs-lookup"><span data-stu-id="74885-138">\- Other.</span></span> <span data-ttu-id="74885-139">La proprietà OtherAlertType dell'indicatore trasmette la relativa classificazione.</span><span class="sxs-lookup"><span data-stu-id="74885-139">The Indication's OtherAlertType property conveys its classification.</span></span> <span data-ttu-id="74885-140">L'uso di "altro" in un'enumerazione è una convenzione CIM standard.</span><span class="sxs-lookup"><span data-stu-id="74885-140">Use of "Other" in an enumeration is a standard CIM convention.</span></span> <span data-ttu-id="74885-141">Significa che l'indicazione corrente non rientra nelle categorie descritte da questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="74885-141">It means that the current Indication does not fit into the categories described by this enumeration.</span></span>

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span data-ttu-id="74885-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Avviso di comunicazione** (2)</span><span class="sxs-lookup"><span data-stu-id="74885-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Communications Alert** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74885-143">Un'indicazione di questo tipo è associata principalmente alle procedure e/o ai processi necessari per il trasferimento di informazioni da un punto a un altro.</span><span class="sxs-lookup"><span data-stu-id="74885-143">An Indication of this type is principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span data-ttu-id="74885-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Avviso di qualità del servizio** (3)</span><span class="sxs-lookup"><span data-stu-id="74885-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74885-145">Un'indicazione di questo tipo è associata principalmente a una riduzione o a errori nelle prestazioni o nella funzione di un'entità.</span><span class="sxs-lookup"><span data-stu-id="74885-145">An Indication of this type is principally associated with a degradation or errors in the performance or function of an entity.</span></span>

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span data-ttu-id="74885-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Errore di elaborazione** (4)</span><span class="sxs-lookup"><span data-stu-id="74885-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Processing Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74885-147">Un'indicazione di questo tipo è associata principalmente a un errore software o di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="74885-147">An Indication of this type is principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span data-ttu-id="74885-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Avviso del dispositivo** (5)</span><span class="sxs-lookup"><span data-stu-id="74885-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Device Alert** (5)</span></span>


</dt> <dd>

<span data-ttu-id="74885-149">Un'indicazione di questo tipo è associata principalmente a un errore hardware o di strumentazione.</span><span class="sxs-lookup"><span data-stu-id="74885-149">An Indication of this type is principally associated with an equipment or hardware fault.</span></span>

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span data-ttu-id="74885-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Avviso ambientale** (6)</span><span class="sxs-lookup"><span data-stu-id="74885-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Environmental Alert** (6)</span></span>


</dt> <dd>

<span data-ttu-id="74885-151">Avviso ambientale.</span><span class="sxs-lookup"><span data-stu-id="74885-151">Environmental Alert.</span></span> <span data-ttu-id="74885-152">Un'indicazione di questo tipo è associata principalmente a una condizione relativa a un'enclosure in cui si trova l'hardware o ad altre considerazioni sull'ambiente.</span><span class="sxs-lookup"><span data-stu-id="74885-152">An Indication of this type is principally associated with a condition relating to an enclosure in which the hardware resides, or other environmental considerations.</span></span>

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span data-ttu-id="74885-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Modifica modello** (7)</span><span class="sxs-lookup"><span data-stu-id="74885-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Model Change** (7)</span></span>


</dt> <dd>

<span data-ttu-id="74885-154">L'indicazione risolve le modifiche nel modello informativo.</span><span class="sxs-lookup"><span data-stu-id="74885-154">The Indication addresses changes in the Information Model.</span></span> <span data-ttu-id="74885-155">Ad esempio, può incorporare un'indicazione del ciclo di vita per indicare che la modifica del modello specifica viene segnalata.</span><span class="sxs-lookup"><span data-stu-id="74885-155">For example, it may embed a Lifecycle Indication to convey the specific model change being alerted.</span></span>

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span data-ttu-id="74885-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Avviso di sicurezza** (8)</span><span class="sxs-lookup"><span data-stu-id="74885-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Security Alert** (8)</span></span>


</dt> <dd>

<span data-ttu-id="74885-157">.</span><span class="sxs-lookup"><span data-stu-id="74885-157">.</span></span> <span data-ttu-id="74885-158">Viene associata un'indicazione di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="74885-158">An Indication of this type is associated.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74885-159">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="74885-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-162">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Testo aggiuntivo ")</span><span class="sxs-lookup"><span data-stu-id="74885-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Additional text")</span></span>
</dt> </dl>

<span data-ttu-id="74885-163">Breve descrizione dell'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74885-163">A short description of the Indication.</span></span>

</dd> <dt>

<span data-ttu-id="74885-164">**EventID**</span><span class="sxs-lookup"><span data-stu-id="74885-164">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-167">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="74885-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-168">Valore specifico di strumentazione o provider che descrive l'evento reale sottostante rappresentato dall'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74885-168">An instrumentation or provider specific value that describes the underlying real-world event represented by the indication.</span></span> <span data-ttu-id="74885-169">Le indicazioni con lo stesso valore **eventId** non null vengono considerate dall'entità di creazione per rappresentare lo stesso evento.</span><span class="sxs-lookup"><span data-stu-id="74885-169">Indications with the same non-NULL **EventID** value are considered, by the creating entity, to represent the same event.</span></span> <span data-ttu-id="74885-170">Il confronto di due valori **eventId** viene definito solo per le indicazioni di avviso con valori identici, non null, delle proprietà **SystemCreateClassName**, **SystemName** e **providerName** .</span><span class="sxs-lookup"><span data-stu-id="74885-170">The comparison of two **EventID** values is only defined for alert indications with identical, non-NULL values of **SystemCreateClassName**, **SystemName** and **ProviderName** properties.</span></span>

</dd> <dt>

<span data-ttu-id="74885-171">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="74885-171">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-172">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74885-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74885-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-174">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="74885-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-175">Data e ora che indica quando l'evento sottostante è stato rilevato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="74885-175">The time and date that indicates when the underlying event was first detected.</span></span> <span data-ttu-id="74885-176">Se questi valori vengono specificati e l'entità di creazione non è in grado di fornire queste informazioni, questa proprietà deve essere impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="74885-176">If this values is specified and the creating entity is not capable of providing this information, this property must be set to **NULL**.</span></span> <span data-ttu-id="74885-177">Questo valore è basato sulla nozione della data e dell'ora locali dell'oggetto **\_ ManageSystemElement CIM** che ha generato l'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74885-177">This value is based on the notion of the local date and time of the **CIM\_ManageSystemElement** object that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="74885-178">**Messaggio**</span><span class="sxs-lookup"><span data-stu-id="74885-178">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-181">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**MessageID**","**CIM \_ AlertIndication**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="74885-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**MessageID**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-182">Messaggio formattato per l'indicazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="74885-182">The formatted message for the alert indication.</span></span> <span data-ttu-id="74885-183">Questo messaggio viene formattato combinando uno o più elementi dinamici specificati nella proprietà **MessageArguments** e con gli elementi statici identificati in modo univoco dalla proprietà **MessageID** .</span><span class="sxs-lookup"><span data-stu-id="74885-183">This message is formatted by combining one or more of the dynamic elements specified in the **MessageArguments** property, and with the static elements uniquely identified by the **MessageID** property.</span></span>

</dd> <dt>

<span data-ttu-id="74885-184">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="74885-184">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-185">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="74885-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74885-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-187">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Messaggio**","**CIM \_ AlertIndication**.**MessageID**")</span><span class="sxs-lookup"><span data-stu-id="74885-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageID**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-188">Matrice che contiene il contenuto dinamico del messaggio per l'indicazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="74885-188">An array that contains the dynamic content of the message for the alert indication.</span></span>

</dd> <dt>

<span data-ttu-id="74885-189">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="74885-189">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-192">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Messaggio**","**CIM \_ AlertIndication**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="74885-192">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-193">ID univoco del formato del messaggio, con l'ambito dell'organizzazione specificato in **OwningEntity**.</span><span class="sxs-lookup"><span data-stu-id="74885-193">The unique ID of the message format, withing the scope of the organization specified in **OwningEntity**.</span></span>

</dd> <dt>

<span data-ttu-id="74885-194">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="74885-194">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-197">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="74885-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-198">Definisce il formato della proprietà **AlertingManagedElement** quando la proprietà **AlertingElementFormat** è impostata su "1" (other); in caso contrario, questo valore deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="74885-198">Defines the format of the **AlertingManagedElement** property when the **AlertingElementFormat** property is set to "1" (other); otherwise, this value must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="74885-199">**OtherAlertType**</span><span class="sxs-lookup"><span data-stu-id="74885-199">**OtherAlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-202">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertType**")</span><span class="sxs-lookup"><span data-stu-id="74885-202">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertType**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-203">Stringa che descrive il valore **AlertType** quando la proprietà **AlertType** è impostata su "1" (altra modifica dello stato).</span><span class="sxs-lookup"><span data-stu-id="74885-203">A string that describes the **AlertType** value when the **AlertType** property is set to "1" (Other State Change).</span></span>

</dd> <dt>

<span data-ttu-id="74885-204">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="74885-204">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74885-207">ID univoco dell'organizzazione a cui appartiene la definizione del formato della proprietà del **messaggio** .</span><span class="sxs-lookup"><span data-stu-id="74885-207">The unique ID of the organization that owns the definition of the format of the **Message** property.</span></span> <span data-ttu-id="74885-208">**OwningEntity** deve includere un nome con copyright, marchio o univoco di proprietà dell'entità di business o del corpo degli standard che ha definito il formato del messaggio.</span><span class="sxs-lookup"><span data-stu-id="74885-208">**OwningEntity** must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

</dd> <dt>

<span data-ttu-id="74885-209">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="74885-209">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-210">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74885-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74885-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-212">Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Gravità percepita ")</span><span class="sxs-lookup"><span data-stu-id="74885-212">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="74885-213">Gravità dell'indicazione di avviso dal punto di vista dell'elemento che ha generato l'avviso.</span><span class="sxs-lookup"><span data-stu-id="74885-213">The severity of the alert indication from the point of view of the element that raised the alert.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74885-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="74885-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="74885-215">Segue l'utilizzo comune.</span><span class="sxs-lookup"><span data-stu-id="74885-215">Follows common usage.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74885-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="74885-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="74885-217">Indica che il valore della gravità è reperibile nella proprietà OtherSeverity.</span><span class="sxs-lookup"><span data-stu-id="74885-217">Indicates that the Severity's value can be found in the OtherSeverity property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="74885-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informazioni** (2)</span><span class="sxs-lookup"><span data-stu-id="74885-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74885-219">Segue l'utilizzo comune.</span><span class="sxs-lookup"><span data-stu-id="74885-219">Follows common usage.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="74885-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Danneggiato/avviso** (3)</span><span class="sxs-lookup"><span data-stu-id="74885-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74885-221">Deve essere usato quando è appropriato per consentire all'utente di decidere se è necessaria un'azione.</span><span class="sxs-lookup"><span data-stu-id="74885-221">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="74885-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secondario** (4)</span><span class="sxs-lookup"><span data-stu-id="74885-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74885-223">Indica che l'azione è necessaria, ma in questo momento la situazione non è grave.</span><span class="sxs-lookup"><span data-stu-id="74885-223">Indicates action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="74885-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principale** (5)</span><span class="sxs-lookup"><span data-stu-id="74885-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="74885-225">Indica che l'azione è ora necessaria.</span><span class="sxs-lookup"><span data-stu-id="74885-225">Indicates action is needed now.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="74885-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (6)</span><span class="sxs-lookup"><span data-stu-id="74885-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="74885-227">L'azione è ora necessaria e l'ambito è ampio (probabilmente verrà generata un'interruzione imminente a una risorsa critica).</span><span class="sxs-lookup"><span data-stu-id="74885-227">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="74885-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irreversibile/irreversibile** (7)</span><span class="sxs-lookup"><span data-stu-id="74885-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="74885-229">Indica che si è verificato un errore, ma è troppo tardi per eseguire un'azione correttiva.</span><span class="sxs-lookup"><span data-stu-id="74885-229">Indicates an error occurred, but it's too late to take remedial action.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74885-230">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="74885-230">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-231">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74885-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74885-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-233">Qualificatori: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Probabili cause "," Recommendation. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCauseDescription**","**CIM \_ AlertIndication**.**ID** evento ","**CIM \_ AlertIndication**.**EventTime**")</span><span class="sxs-lookup"><span data-stu-id="74885-233">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCauseDescription**", "**CIM\_AlertIndication**.**EventID**", "**CIM\_AlertIndication**.**EventTime**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-234">Causa probabile della situazione che ha generato l'indicazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="74885-234">The probable cause of the situation which resulted in the alert indication.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74885-235">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="74885-235">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74885-236">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="74885-236">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="74885-237">**Errore scheda/scheda** (2)</span><span class="sxs-lookup"><span data-stu-id="74885-237">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="74885-238">**Errore del sottosistema dell'applicazione** (3)</span><span class="sxs-lookup"><span data-stu-id="74885-238">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="74885-239">**Larghezza di banda ridotta** (4)</span><span class="sxs-lookup"><span data-stu-id="74885-239">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="74885-240">**Errore di creazione connessione** (5)</span><span class="sxs-lookup"><span data-stu-id="74885-240">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="74885-241">**Errore del protocollo di comunicazione** (6)</span><span class="sxs-lookup"><span data-stu-id="74885-241">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="74885-242">**Errore del sottosistema di comunicazione** (7)</span><span class="sxs-lookup"><span data-stu-id="74885-242">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="74885-243">**Errore di configurazione/personalizzazione** (8)</span><span class="sxs-lookup"><span data-stu-id="74885-243">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="74885-244">**Congestione** (9)</span><span class="sxs-lookup"><span data-stu-id="74885-244">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="74885-245">**Dati danneggiati** (10)</span><span class="sxs-lookup"><span data-stu-id="74885-245">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="74885-246">**Limite cicli CPU superato** (11)</span><span class="sxs-lookup"><span data-stu-id="74885-246">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="74885-247">**Errore del set di dati/modem** (12)</span><span class="sxs-lookup"><span data-stu-id="74885-247">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="74885-248">**Segnale danneggiato** (13)</span><span class="sxs-lookup"><span data-stu-id="74885-248">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="74885-249">**Errore di interfaccia DTE-DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="74885-249">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="74885-250">**Sportello enclosure aperto** (15)</span><span class="sxs-lookup"><span data-stu-id="74885-250">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="74885-251">**Malfunzionamento delle apparecchiature** (16)</span><span class="sxs-lookup"><span data-stu-id="74885-251">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="74885-252">**Vibrazione eccessiva** (17)</span><span class="sxs-lookup"><span data-stu-id="74885-252">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="74885-253">**Errore di formato del file** (18)</span><span class="sxs-lookup"><span data-stu-id="74885-253">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="74885-254">**Fire detected** (19)</span><span class="sxs-lookup"><span data-stu-id="74885-254">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="74885-255">**Flood rilevato** (20)</span><span class="sxs-lookup"><span data-stu-id="74885-255">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="74885-256">**Errore di framing** (21)</span><span class="sxs-lookup"><span data-stu-id="74885-256">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="74885-257">**Problema HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="74885-257">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="74885-258">**Umidità inaccettabile** (23)</span><span class="sxs-lookup"><span data-stu-id="74885-258">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="74885-259">**Errore del dispositivo di I/O** (24)</span><span class="sxs-lookup"><span data-stu-id="74885-259">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="74885-260">**Errore dispositivo di input** (25)</span><span class="sxs-lookup"><span data-stu-id="74885-260">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="74885-261">**Errore LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="74885-261">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="74885-262">È stata **rilevata una perdita non tossica** (27)</span><span class="sxs-lookup"><span data-stu-id="74885-262">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="74885-263">**Errore di trasmissione del nodo locale** (28)</span><span class="sxs-lookup"><span data-stu-id="74885-263">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="74885-264">**Perdita di frame** (29)</span><span class="sxs-lookup"><span data-stu-id="74885-264">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="74885-265">**Perdita del segnale** (30)</span><span class="sxs-lookup"><span data-stu-id="74885-265">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="74885-266">**Approvvigionamento materiale esaurito** (31)</span><span class="sxs-lookup"><span data-stu-id="74885-266">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="74885-267">**Problema del multiplexer** (32)</span><span class="sxs-lookup"><span data-stu-id="74885-267">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="74885-268">**Memoria insufficiente** (33)</span><span class="sxs-lookup"><span data-stu-id="74885-268">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="74885-269">**Errore dispositivo di output** (34)</span><span class="sxs-lookup"><span data-stu-id="74885-269">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="74885-270">**Prestazioni** ridotte (35)</span><span class="sxs-lookup"><span data-stu-id="74885-270">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="74885-271">**Problema di alimentazione** (36)</span><span class="sxs-lookup"><span data-stu-id="74885-271">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="74885-272">**Pressione inaccettabile** (37)</span><span class="sxs-lookup"><span data-stu-id="74885-272">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="74885-273">**Problema del processore (errore interno del computer)** (38)</span><span class="sxs-lookup"><span data-stu-id="74885-273">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="74885-274">**Errore della pompa** (39)</span><span class="sxs-lookup"><span data-stu-id="74885-274">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="74885-275">**Dimensione coda superata** (40)</span><span class="sxs-lookup"><span data-stu-id="74885-275">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="74885-276">**Errore di ricezione** (41)</span><span class="sxs-lookup"><span data-stu-id="74885-276">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="74885-277">**Errore del ricevitore** (42)</span><span class="sxs-lookup"><span data-stu-id="74885-277">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="74885-278">**Errore di trasmissione del nodo remoto** (43)</span><span class="sxs-lookup"><span data-stu-id="74885-278">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="74885-279">**Risorsa alla capacità o al prossimo livello** (44)</span><span class="sxs-lookup"><span data-stu-id="74885-279">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="74885-280">**Tempo di risposta eccessivo** (45)</span><span class="sxs-lookup"><span data-stu-id="74885-280">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="74885-281">**Frequenza di ritrasmissione eccessiva** (46)</span><span class="sxs-lookup"><span data-stu-id="74885-281">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="74885-282">**Errore software** (47)</span><span class="sxs-lookup"><span data-stu-id="74885-282">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="74885-283">**Programma software terminato in modo anomalo** (48)</span><span class="sxs-lookup"><span data-stu-id="74885-283">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="74885-284">**Errore del programma software (risultati non corretti)** (49)</span><span class="sxs-lookup"><span data-stu-id="74885-284">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="74885-285">**Problema di capacità di archiviazione** (50)</span><span class="sxs-lookup"><span data-stu-id="74885-285">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="74885-286">**Temperatura inaccettabile** (51)</span><span class="sxs-lookup"><span data-stu-id="74885-286">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="74885-287">**Soglia superata** (52)</span><span class="sxs-lookup"><span data-stu-id="74885-287">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="74885-288">**Problema di temporizzazione** (53)</span><span class="sxs-lookup"><span data-stu-id="74885-288">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="74885-289">È stata **rilevata una perdita tossica** (54)</span><span class="sxs-lookup"><span data-stu-id="74885-289">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="74885-290">**Errore di trasmissione** (55)</span><span class="sxs-lookup"><span data-stu-id="74885-290">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="74885-291">**Errore della trasmittente** (56)</span><span class="sxs-lookup"><span data-stu-id="74885-291">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="74885-292">**Risorsa sottostante non disponibile** (57)</span><span class="sxs-lookup"><span data-stu-id="74885-292">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="74885-293">**Versione non corrispondente** (58)</span><span class="sxs-lookup"><span data-stu-id="74885-293">**Version MisMatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="74885-294">**Avviso precedente cancellato** (59)</span><span class="sxs-lookup"><span data-stu-id="74885-294">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="74885-295">**Tentativi di accesso non riusciti** (60)</span><span class="sxs-lookup"><span data-stu-id="74885-295">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="74885-296">**Rilevato virus software** (61)</span><span class="sxs-lookup"><span data-stu-id="74885-296">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="74885-297">**Protezione hardware violata** (62)</span><span class="sxs-lookup"><span data-stu-id="74885-297">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="74885-298">**Rilevato un attacco Denial of Service** (63)</span><span class="sxs-lookup"><span data-stu-id="74885-298">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="74885-299">**Mancata corrispondenza delle credenziali di sicurezza** (64)</span><span class="sxs-lookup"><span data-stu-id="74885-299">**Security Credential MisMatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="74885-300">**Accesso non autorizzato** (65)</span><span class="sxs-lookup"><span data-stu-id="74885-300">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="74885-301">**Allarme ricevuto** (66)</span><span class="sxs-lookup"><span data-stu-id="74885-301">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="74885-302">**Perdita di puntatore** (67)</span><span class="sxs-lookup"><span data-stu-id="74885-302">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="74885-303">**Mancata corrispondenza del payload** (68)</span><span class="sxs-lookup"><span data-stu-id="74885-303">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="74885-304">**Errore di trasmissione** (69)</span><span class="sxs-lookup"><span data-stu-id="74885-304">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="74885-305">**Frequenza degli errori eccessiva** (70)</span><span class="sxs-lookup"><span data-stu-id="74885-305">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="74885-306">**Problema di traccia** (71)</span><span class="sxs-lookup"><span data-stu-id="74885-306">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="74885-307">**Elemento non disponibile** (72)</span><span class="sxs-lookup"><span data-stu-id="74885-307">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="74885-308">**Elemento mancante** (73)</span><span class="sxs-lookup"><span data-stu-id="74885-308">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="74885-309">**Perdita di più frame** (74)</span><span class="sxs-lookup"><span data-stu-id="74885-309">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="74885-310">**Errore canale broadcast** (75)</span><span class="sxs-lookup"><span data-stu-id="74885-310">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="74885-311">**Ricevuto messaggio non valido** (76)</span><span class="sxs-lookup"><span data-stu-id="74885-311">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="74885-312">**Errore di routing** (77)</span><span class="sxs-lookup"><span data-stu-id="74885-312">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="74885-313">**Errore backplane** (78)</span><span class="sxs-lookup"><span data-stu-id="74885-313">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="74885-314">**Duplicazione degli identificatori** (79)</span><span class="sxs-lookup"><span data-stu-id="74885-314">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="74885-315">**Errore nel percorso di protezione** (80)</span><span class="sxs-lookup"><span data-stu-id="74885-315">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="74885-316">**Perdita di sincronizzazione o mancata corrispondenza** (81)</span><span class="sxs-lookup"><span data-stu-id="74885-316">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="74885-317">**Problema terminale** (82)</span><span class="sxs-lookup"><span data-stu-id="74885-317">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="74885-318">**Errore di clock in tempo reale** (83)</span><span class="sxs-lookup"><span data-stu-id="74885-318">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="74885-319">**Errore antenna** (84)</span><span class="sxs-lookup"><span data-stu-id="74885-319">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="74885-320">**Errore di ricarica della batteria** (85)</span><span class="sxs-lookup"><span data-stu-id="74885-320">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="74885-321">**Errore del disco** (86)</span><span class="sxs-lookup"><span data-stu-id="74885-321">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="74885-322">**Errore di salto della frequenza** (87)</span><span class="sxs-lookup"><span data-stu-id="74885-322">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="74885-323">**Perdita di ridondanza** (88)</span><span class="sxs-lookup"><span data-stu-id="74885-323">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="74885-324">**Errore alimentatore** (89)</span><span class="sxs-lookup"><span data-stu-id="74885-324">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="74885-325">**Problema relativo alla qualità del segnale** (90)</span><span class="sxs-lookup"><span data-stu-id="74885-325">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="74885-326">Scaricamento **della batteria** (91)</span><span class="sxs-lookup"><span data-stu-id="74885-326">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="74885-327">**Errore batteria** (92)</span><span class="sxs-lookup"><span data-stu-id="74885-327">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="74885-328">**Problema di alimentazione commerciale** (93)</span><span class="sxs-lookup"><span data-stu-id="74885-328">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="74885-329">**Errore ventola** (94)</span><span class="sxs-lookup"><span data-stu-id="74885-329">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="74885-330">**Errore del motore** (95)</span><span class="sxs-lookup"><span data-stu-id="74885-330">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="74885-331">**Errore del sensore** (96)</span><span class="sxs-lookup"><span data-stu-id="74885-331">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="74885-332">**Errore fusibile** (97)</span><span class="sxs-lookup"><span data-stu-id="74885-332">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="74885-333">**Errore del generatore** (98)</span><span class="sxs-lookup"><span data-stu-id="74885-333">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="74885-334">**Batteria insufficiente** (99)</span><span class="sxs-lookup"><span data-stu-id="74885-334">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="74885-335">**Carburante basso** (100)</span><span class="sxs-lookup"><span data-stu-id="74885-335">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="74885-336">**Acqua bassa** (101)</span><span class="sxs-lookup"><span data-stu-id="74885-336">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="74885-337">**Gas esplosivo** (102)</span><span class="sxs-lookup"><span data-stu-id="74885-337">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="74885-338">**Venti elevati** (103)</span><span class="sxs-lookup"><span data-stu-id="74885-338">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="74885-339">**Accumulo di ghiaccio** (104)</span><span class="sxs-lookup"><span data-stu-id="74885-339">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="74885-340">**Fumo** (105)</span><span class="sxs-lookup"><span data-stu-id="74885-340">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="74885-341">**Memoria non corrispondente** (106)</span><span class="sxs-lookup"><span data-stu-id="74885-341">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="74885-342">**Cicli esauriti CPU** (107)</span><span class="sxs-lookup"><span data-stu-id="74885-342">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="74885-343">**Problema relativo all'ambiente software** (108)</span><span class="sxs-lookup"><span data-stu-id="74885-343">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="74885-344">**Errore di download del software** (109)</span><span class="sxs-lookup"><span data-stu-id="74885-344">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="74885-345">**Elemento reinizializzato** (110)</span><span class="sxs-lookup"><span data-stu-id="74885-345">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="74885-346">**Timeout** (111)</span><span class="sxs-lookup"><span data-stu-id="74885-346">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="74885-347">**Problemi di registrazione** (112)</span><span class="sxs-lookup"><span data-stu-id="74885-347">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="74885-348">**Perdita rilevata** (113)</span><span class="sxs-lookup"><span data-stu-id="74885-348">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="74885-349">**Errore del meccanismo di protezione** (114)</span><span class="sxs-lookup"><span data-stu-id="74885-349">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="74885-350">**Protezione** di un errore di risorse (115)</span><span class="sxs-lookup"><span data-stu-id="74885-350">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="74885-351">**Incoerenza del database** (116)</span><span class="sxs-lookup"><span data-stu-id="74885-351">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="74885-352">**Errore di autenticazione** (117)</span><span class="sxs-lookup"><span data-stu-id="74885-352">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="74885-353">**Violazione della riservatezza** (118)</span><span class="sxs-lookup"><span data-stu-id="74885-353">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="74885-354">**Manomissione cavo** (119)</span><span class="sxs-lookup"><span data-stu-id="74885-354">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="74885-355">**Informazioni ritardate** (120)</span><span class="sxs-lookup"><span data-stu-id="74885-355">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="74885-356">**Informazioni duplicate** (121)</span><span class="sxs-lookup"><span data-stu-id="74885-356">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="74885-357">**Informazioni mancanti** (122)</span><span class="sxs-lookup"><span data-stu-id="74885-357">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="74885-358">**Modifica delle informazioni** (123)</span><span class="sxs-lookup"><span data-stu-id="74885-358">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="74885-359">**Informazioni fuori sequenza** (124)</span><span class="sxs-lookup"><span data-stu-id="74885-359">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="74885-360">**Chiave scaduta** (125)</span><span class="sxs-lookup"><span data-stu-id="74885-360">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="74885-361">**Errore di non ripudio** (126)</span><span class="sxs-lookup"><span data-stu-id="74885-361">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="74885-362">**Attività fuori orario** (127)</span><span class="sxs-lookup"><span data-stu-id="74885-362">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="74885-363">**Fuori servizio** (128)</span><span class="sxs-lookup"><span data-stu-id="74885-363">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="74885-364">**Errore procedurale** (129)</span><span class="sxs-lookup"><span data-stu-id="74885-364">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="74885-365">**Informazioni impreviste** (130)</span><span class="sxs-lookup"><span data-stu-id="74885-365">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74885-366">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="74885-366">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-367">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-369">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="74885-369">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="74885-370">Informazioni aggiuntive correlate alla proprietà **ProbableCause** .</span><span class="sxs-lookup"><span data-stu-id="74885-370">Additional information related to the **ProbableCause** property.</span></span>

</dd> <dt>

<span data-ttu-id="74885-371">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="74885-371">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-372">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-374">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="74885-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="74885-375">Nome del provider che ha generato l'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74885-375">The name of the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="74885-376">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="74885-376">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-377">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="74885-377">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74885-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-379">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Azioni di ripristino proposte ")</span><span class="sxs-lookup"><span data-stu-id="74885-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Proposed repair actions")</span></span>
</dt> </dl>

<span data-ttu-id="74885-380">Descrizioni del formato gratuite delle azioni consigliate da intraprendere per risolvere la cause della notifica.</span><span class="sxs-lookup"><span data-stu-id="74885-380">Free form descriptions of the recommended actions to take to resolve the cause of the notification.</span></span>

</dd> <dt>

<span data-ttu-id="74885-381">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="74885-381">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-382">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-384">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="74885-384">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="74885-385">Valore **CreationClassName** del sistema di ambito per il provider che ha generato l'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74885-385">The **CreationClassName** value of the scoping system for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="74885-386">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="74885-386">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-387">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74885-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74885-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-389">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="74885-389">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="74885-390">Nome del sistema di ambito per il provider che ha generato l'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74885-390">The scoping system name for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="74885-391">**Di tendenza**</span><span class="sxs-lookup"><span data-stu-id="74885-391">**Trending**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74885-392">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74885-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74885-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74885-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74885-394">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. TrendIndication")</span><span class="sxs-lookup"><span data-stu-id="74885-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.TrendIndication")</span></span>
</dt> </dl>

<span data-ttu-id="74885-395">Fornisce informazioni sulla tendenza, ovvero sulle tendenze, su inattivo o nessuna modifica.</span><span class="sxs-lookup"><span data-stu-id="74885-395">Provides information on trending - trending up, down or no change.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74885-396">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="74885-396">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="74885-397">**Non applicabile** (1)</span><span class="sxs-lookup"><span data-stu-id="74885-397">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

<span data-ttu-id="74885-398">**Tendenza verso l'alto** (2)</span><span class="sxs-lookup"><span data-stu-id="74885-398">**Trending Up** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

<span data-ttu-id="74885-399">**Tendenza verso il basso** (3)</span><span class="sxs-lookup"><span data-stu-id="74885-399">**Trending Down** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="74885-400">**Nessuna modifica** (4)</span><span class="sxs-lookup"><span data-stu-id="74885-400">**No Change** (4)</span></span>


<span data-ttu-id="74885-401"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="74885-401"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="74885-402">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74885-402">Requirements</span></span>



| <span data-ttu-id="74885-403">Requisito</span><span class="sxs-lookup"><span data-stu-id="74885-403">Requirement</span></span> | <span data-ttu-id="74885-404">Valore</span><span class="sxs-lookup"><span data-stu-id="74885-404">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74885-405">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74885-405">Minimum supported client</span></span><br/> | <span data-ttu-id="74885-406">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="74885-406">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="74885-407">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74885-407">Minimum supported server</span></span><br/> | <span data-ttu-id="74885-408">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="74885-408">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="74885-409">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="74885-409">Namespace</span></span><br/>                | <span data-ttu-id="74885-410">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="74885-410">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="74885-411">MOF</span><span class="sxs-lookup"><span data-stu-id="74885-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74885-412"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74885-412"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74885-413">DLL</span><span class="sxs-lookup"><span data-stu-id="74885-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74885-414"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74885-414"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74885-415">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74885-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74885-416">**\_PROCESSINDICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="74885-416">**CIM\_ProcessIndication**</span></span>](cim-processindication.md)
</dt> </dl>

 

