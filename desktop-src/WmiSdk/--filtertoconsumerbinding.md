---
description: Viene utilizzato nella registrazione di consumer di eventi permanenti per correlare un'istanza di \_ \_ EventConsumer a un'istanza di \_ \_ eventfilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: Classe __FilterToConsumerBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317596"
---
# <a name="__filtertoconsumerbinding-class"></a>\_\_Classe FilterToConsumerBinding

La classe di sistema **\_ \_ FilterToConsumerBinding** viene utilizzata per la registrazione di consumer di eventi permanenti per correlare un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) a un'istanza di [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ FilterToConsumerBinding** è una classe di associazione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a>Members

La classe **\_ \_ FilterToConsumerBinding** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ FilterToConsumerBinding** dispone di queste proprietà.

<dl> <dt>

**Consumer**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ EventConsumer**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Riferimento a un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) che rappresenta il percorso dell'oggetto a un consumer logico, il destinatario di un evento. Un consumer logico è un'istanza di una classe derivata da **\_ \_ EventConsumer**.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

ID di sicurezza (SID) che identifica in modo univoco l'utente che ha creato l'associazione. A seconda del sistema operativo, WMI archivia il SID amministratore o il SID dell'utente che crea un'istanza di **\_ \_ FilterToConsumerBinding**. Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.

</dd> <dt>

**DeliverSynchronously**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Obsoleta. Usare invece la proprietà **DeliveryQoS** al posto di questa proprietà, perché se **DeliverSynchronously** è impostato su **true** , viene eseguito l'override dell'impostazione della proprietà **DeliveryQoS** .

</dd> <dt>

**DeliveryQoS**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Qualità del servizio per una sottoscrizione. Se la proprietà **DeliverSynchronously** è impostata su **true**, esegue l'override dell'impostazione della proprietà **DeliveryQoS** .

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_ FLAG \_ QoS \_ sincrono** (0)


</dt> <dd>

Recapito sincrono

**False**. L'evento viene recapitato in modo sincrono al consumer logico.

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_ FLAG \_ QoS \_ Express** (1)


</dt> <dd>

Recapito rapido

**True**. L'evento viene recapitato al consumer logico in modo asincrono.

</dd> </dl>

</dd> <dt>

**Filter**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ EventFilter**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Riferimento a un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) che rappresenta il percorso dell'oggetto a un filtro eventi che è una query che specifica il tipo di evento da ricevere.

</dd> <dt>

**MaintainSecurityContext**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, gli eventi vengono recapitati nello stesso contesto di sicurezza in cui si trovava il provider al momento della loro fornitura.

> [!Note]  
> Solo un consumer implementato come DLL (un consumer in-process) può ricevere eventi nel contesto di sicurezza del provider. Per ulteriori informazioni sulla sicurezza e sui provider in-process, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md). Per ulteriori informazioni ed esempi, vedere Replace:[ricezione di eventi](receiving-events-securely.md)in modo sicuro.

 

</dd> <dt>

**SlowDownProviders**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, i provider vengono rallentati se il consumer non è in grado di rimanere attivi.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ FilterToConsumerBinding** deriva da [**\_ \_ IndicationRelated**](--indicationrelated.md), che non dispone di proprietà.

I consumer di eventi permanenti usano la classe di sistema **\_ \_ FilterToConsumerBinding** per associare i filtri eventi ai consumer finali. Dopo aver associato il filtro e il consumer, WMI può inviare gli eventi che corrispondono al filtro al consumer corrispondente.

## <a name="examples"></a>Esempio

Nell'esempio di PowerShell [per la creazione di una registrazione di eventi WMI permanenti per il monitoraggio dei file](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) nella raccolta TechNet viene usato **\_ \_ FilterToConsumerBinding** come parte di uno script complesso per configurare la registrazione di un evento WMI permanente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_IndicationRelated**](--indicationrelated.md)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Monitoraggio degli eventi](monitoring-events.md)
</dt> <dt>

[Creazione di un filtro eventi](creating-an-event-filter.md)
</dt> <dt>

[Protezione degli eventi WMI](securing-wmi-events.md)
</dt> </dl>

 

 




