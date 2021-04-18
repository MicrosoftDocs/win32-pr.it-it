---
description: I provider di eventi SNMP supportano i trap SNMPv1 e le notifiche SNMPv2.
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: Ricezione di eventi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f718d2bcea85d0ee942050108f337f8ecb78e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314585"
---
# <a name="receiving-snmp-events"></a>Ricezione di eventi SNMP

I provider di eventi SNMP supportano i trap SNMPv1 e le notifiche SNMPv2.

Sono supportati i tre tipi di trap SNMPv1 e le notifiche SNMPv2 seguenti:

-   Generico

    Le notifiche e i trap generici corrispondono a eventi denominati, ad esempio collegamento e avvio a freddo. Le notifiche e i trap generici sono rappresentati da classi, ad esempio **SnmpLinkUpNotification** e **SnmpWarmStartExtendedNotification**, che contengono il nome della trap nel nome della classe. Queste classi sono sottoclassi di [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md).

-   Specifiche dell'organizzazione

    Le notifiche e i trap specifici dell'organizzazione corrispondono a eventi rappresentati da una classe WMI che non è una sottoclasse di [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md). Per supportare trap e notifiche specifiche dell'organizzazione, un consumer deve definire le classi compilando le definizioni MIB usando il compilatore MIB SNMP.

-   Aziendale-non specifico

    Le notifiche e i trap non specifici dell'organizzazione non corrispondono ad alcun tipo di evento generico o a tipi di evento specifici dell'organizzazione. Per le notifiche e i trap non specifici dell'organizzazione non sono state compilate le definizioni MIB in archivio SMIR. Sono rappresentate dalle classi [SnmpNotification](snmpnotification.md), **SnmpV2Notification**, **SnmpV1ExtendedNotification** e **SnmpV2ExtendedNotification** derivate da SnmpNotification e [SnmpExtendedNotification](snmpextendednotification.md).

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Le sezioni seguenti sono illustrate in questo argomento:

-   [Ricezione di eventi SNMP generici](#receiving-generic-snmp-events)
-   [Ricezione di eventi Enterprise-Specific](#receiving-enterprise-specific-events)
-   [Ricezione di eventi Enterprise-Nonspecific](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>Ricezione di eventi SNMP generici

Il FILTRAggio e il SREP supportano tutti i tipi di trap SNMPv1 generici e le notifiche SNMPv2. Gli eventi SNMP generici sono rappresentati da sottoclassi delle classi [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md) .

Ogni tipo di evento è rappresentato da una classe infiltrata e una classe SREP. Le classi di infiltrazione derivano da [SnmpNotification](snmpnotification.md); le classi SREP derivano da [SnmpExtendedNotification](snmpextendednotification.md). I provider di eventi richiedono classi diverse perché usano meccanismi diversi nella presentazione dei dati dell'evento SNMP.

Il FILTRAggio converte i dati dell'evento SNMP direttamente nelle proprietà della classe WMI, mentre SREP non lo esegue. SREP aggiunge un livello di riferimento indiretto all'interpretazione necessaria per utilizzare le proprietà WMI. Le proprietà delle sottoclassi SREP [SnmpExtendedNotification](snmpextendednotification.md) sono istanze di classi SNMP; le proprietà delle sottoclassi [SnmpNotification](snmpnotification.md) di filtraggio sono numeri interi e stringhe.

Nella tabella seguente sono elencati i tipi di eventi SNMP generici e le classi di evento associate.



| Evento SNMP                                    | Filtra classe                                | Classe SREP                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| Errore di autenticazione                        | **SnmpAuthenticationFailureNotification** | **SnmpAuthenticationFailureExtendedNotification** |
| Perdita Neighbor del protocollo gateway esterno (EGP) | **SnmpEGPNeighborLossNotification**       | **SnmpEGPNeighborLossExtendedNotification**       |
| Avvio a freddo                                    | **SnmpColdStartNotification**             | **SnmpColdStartExtendedNotification**             |
| Avvio a caldo                                    | **SnmpWarmStartNotification**             | **SnmpWarmStartExtendedNotification**             |
| Collegamento                                       | **SnmpLinkUpNotification**                | **SnmpLinkUpExtendedNotification**                |
| Collegamento in basso                                     | **SnmpLinkDownNotification**              | **SnmpLinkDownExtendedNotification**              |



 

Ad esempio, le classi **SnmpLinkUpNotification** e **SnmpLinkUpExtendedNotification** descrivono l'evento di collegamento. Entrambe le classi includono le proprietà **ifindex**, **ifadminstatus** e **ifOperStatus** , ma hanno tipi molto diversi. Le proprietà della classe **SnmpLinkUpNotification** sono di tipo SINT32 e String. Le proprietà della classe **SnmpLinkUpExtendedNotification** sono il tipo di oggetto incorporato IETF \_ SNMP \_ RFC1213 \_ MIB \_ ifTable.

## <a name="receiving-enterprise-specific-events"></a>Ricezione di eventi Enterprise-Specific

Il FILTRAggio e il SREP supportano eventuali trap e notifiche specifiche dell'organizzazione compilate in archivio SMIR.

Nella procedura riportata di seguito viene descritto come ricevere eventi specifici dell'organizzazione.

**Per ricevere eventi specifici dell'organizzazione**

1.  Compilare le definizioni MIB dal dispositivo responsabile della generazione dell'evento.

    È possibile compilare le definizioni MIB utilizzando il compilatore MIB SNMP. Per ulteriori informazioni, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

2.  Determinare i tipi di classi di cui si desidera eseguire il mapping agli eventi.

    Quando si compila la definizione MIB per un evento specifico dell'organizzazione, è possibile determinare il tipo di classe generato dal compilatore. In particolare, è possibile indicare al compilatore di creare una delle opzioni seguenti:

    -   [SnmpNotification](snmpnotification.md) le sottoclassi dalle definizioni.
    -   [SnmpExtendedNotification](snmpextendednotification.md) le sottoclassi dalle definizioni.
    -   Sottoclassi [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md) dalle definizioni.

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

Se i provider di eventi SNMP ricevono una trap o una notifica specifica per cui non esiste alcuna classe, i provider generano un evento non specifico dell'organizzazione. Per ulteriori informazioni, vedere [ricezione di eventi non specifici dell'organizzazione](#receiving-enterprise-nonspecific-events).

## <a name="receiving-enterprise-nonspecific-events"></a>Ricezione di eventi Enterprise-Nonspecific

Un evento non specifico dell'organizzazione è un evento che non esegue il mapping da un trap SNMPv1 o da una notifica SNMPv2 a una delle sottoclassi di [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) o qualsiasi classe che rappresenta un evento Enterprise.

Filtra usa le classi **SNMPV1Notification** o **SNMPV2Notification** per gli eventi non specifici, mentre SREP usa le classi **SNMPv1ExtendedNotification** e **SNMPV2ExtendedNotification** .

Tutte e quattro le classi non specifiche dell'organizzazione derivano dalle classi [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) e hanno lo stesso formato. Entrambe le classi hanno la singola proprietà **VarBindList**. **VarBindList** è una matrice di istanze della classe **SnmpVarBind** . **SnmpVarBind** è una classe di base supportata dai provider di eventi SNMP per rappresentare un'istanza di un'associazione di variabili SNMP. Nella tabella seguente sono elencate le proprietà di **SnmpVarBind**.



| Proprietà         | Descrizione                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| Codifica         | Stringa che indica il tipo Abstract Syntax Notation One (ASN. 1) della variabile nella proprietà **value** . |
| ObjectIdentifier | Stringa che identifica la variabile nella proprietà **value** .                                                 |
| Valore            | Dati non elaborati in ottetti.                                                                                            |



 

Nelle classi **SnmpV1Notification** e **SnmpV2Notification** , l'ordine di associazione delle variabili dall'evento SNMP è stato mantenuto, ad eccezione dei primi due binding variabili, timestamp e SnmpTrapOID. Queste associazioni sono state rimosse e vengono archiviate nelle proprietà **timestamp** e **Identification** della classe padre [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) .

 

 



