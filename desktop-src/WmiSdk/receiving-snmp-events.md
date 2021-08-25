---
description: I provider di eventi SNMP supportano trap SNMPv1 e notifiche SNMPv2.
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: Ricezione di eventi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf09e32ec05d42adcc60891cd369cde1f3f078541416ce1a492484de024744bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996021"
---
# <a name="receiving-snmp-events"></a>Ricezione di eventi SNMP

I provider di eventi SNMP supportano trap SNMPv1 e notifiche SNMPv2.

Sono supportati i tre tipi di trap SNMPv1 e le notifiche SNMPv2 seguenti:

-   Generico

    Trap e notifiche generiche corrispondono a eventi denominati, ad esempio collegamento e avvio a freddo. Le trap e le notifiche generiche sono rappresentate da classi, ad esempio **SnmpLinkUpNotification** e **SnmpWarmStartExtendedNotification**, che contengono il nome del trap nel nome della classe. Queste classi sono sottoclassi [di SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md).

-   Enterprise specifico

    Enterprise trap e notifiche specifiche corrispondono a eventi rappresentati da una classe WMI che non è una sottoclasse di [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md). Per supportare trap e notifiche specifiche dell'organizzazione, un consumer deve definire le classi compilando le definizioni MIB usando il compilatore MIB SNMP.

-   Enterprise non specifico

    Le trap e le notifiche non specifiche dell'organizzazione non corrispondono ai tipi di evento generici o ai tipi di evento specifici dell'organizzazione. Le definizioni MIB non specifiche di trap e notifiche non sono state compilate in SMIR. Sono rappresentate dalle classi [SnmpNotification](snmpnotification.md), **SnmpV2Notification**, **SnmpV1ExtendedNotification** e **SnmpV2ExtendedNotification** derivate da SnmpNotification e [SnmpExtendedNotification](snmpextendednotification.md).

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Configurazione dell'ambiente SNMP WMI.](setting-up-the-wmi-snmp-environment.md)

 

In questo argomento vengono illustrate le sezioni seguenti:

-   [Ricezione di eventi SNMP generici](#receiving-generic-snmp-events)
-   [Ricezione Enterprise-Specific eventi](#receiving-enterprise-specific-events)
-   [Ricezione Enterprise-Nonspecific eventi](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>Ricezione di eventi SNMP generici

SEEP e SREP supportano tutti i tipi di trap SNMPv1 generici e notifiche SNMPv2. Gli eventi SNMP generici sono rappresentati da sottoclassi delle [classi SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification.](snmpextendednotification.md)

Ogni tipo di evento è rappresentato da una classe SEEP e da una classe SREP. Le classi SEEP derivano da [SnmpNotification](snmpnotification.md); le classi SREP derivano da [SnmpExtendedNotification](snmpextendednotification.md). I provider di eventi richiedono classi diverse perché usano meccanismi diversi nella presentazione dei dati degli eventi SNMP.

SeeP converte i dati degli eventi SNMP direttamente nelle proprietà della classe WMI, mentre SREP non lo fa. SREP aggiunge un livello di riferimento indiretto all'interpretazione necessaria per usare le proprietà WMI. Le proprietà delle sottoclassi [SREP SnmpExtendedNotification](snmpextendednotification.md) sono istanze di classi SNMP. Le proprietà delle sottoclassi SEEP [SnmpNotification](snmpnotification.md) sono numeri interi e stringhe.

Nella tabella seguente sono elencati i tipi di eventi SNMP generici e le classi di evento associate.



| Evento SNMP                                    | Classe SEEP                                | Classe SREP                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| Errore di autenticazione                        | **SnmpAuthenticationFailureNotification** | **SnmpAuthenticationFailureExtendedNotification** |
| Perdita del router adiacente EGP (Exterior Gateway Protocol) | **SnmpEGPNeighborLossNotification**       | **SnmpEGPNeighborLossExtendedNotification**       |
| Avvio a freddo                                    | **SnmpColdStartNotification**             | **SnmpColdStartExtendedNotification**             |
| Avvio a caldo                                    | **SnmpWarmStartNotification**             | **SnmpWarmStartExtendedNotification**             |
| Collegamento                                       | **SnmpLinkUpNotification**                | **SnmpLinkUpExtendedNotification**                |
| Collegamento verso il basso                                     | **SnmpLinkDownNotification**              | **SnmpLinkDownExtendedNotification**              |



 

Ad esempio, le **classi SnmpLinkUpNotification** e **SnmpLinkUpExtendedNotification** descrivono l'evento di collegamento. Entrambe le classi includono le proprietà **ifIndex**, **ifAdminStatus** e **ifOperStatus,** ma hanno tipi molto diversi. Le proprietà nella **classe SnmpLinkUpNotification** sono di tipo SINT32 e STRING. Le proprietà nella **classe SnmpLinkUpExtendedNotification** sono il tipo di oggetto incorporato IETF \_ SNMP \_ RFC1213 \_ MIB \_ ifTable.

## <a name="receiving-enterprise-specific-events"></a>Ricezione Enterprise-Specific eventi

SEEP e SREP supportano tutte le trap e le notifiche specifiche dell'organizzazione compilate in SMIR.

La procedura seguente descrive come ricevere eventi specifici dell'organizzazione.

**Per ricevere eventi specifici dell'organizzazione**

1.  Compilare le definizioni MIB dal dispositivo responsabile della generazione dell'evento.

    È possibile compilare le definizioni MIB usando il compilatore MIB SNMP. Per altre informazioni, vedere [Configurazione dell'ambiente SNMP WMI.](setting-up-the-wmi-snmp-environment.md)

2.  Determinare i tipi di classi di cui si vuole eseguire il mapping agli eventi.

    Quando si compila la definizione MIB per un evento specifico dell'organizzazione, è possibile determinare il tipo di classe generato dal compilatore. In particolare, è possibile indicare al compilatore di creare una delle opzioni seguenti:

    -   [Sottoclassi SnmpNotification](snmpnotification.md) dalle definizioni.
    -   [Sottoclassi SnmpExtendedNotification](snmpextendednotification.md) dalle definizioni.
    -   [Sottoclassi SnmpNotification](snmpnotification.md) [e SnmpExtendedNotification](snmpextendednotification.md) dalle definizioni.

    Per altre informazioni, vedere [Compilazione di file MOF](compiling-mof-files.md).

Se i provider di eventi SNMP ricevono un trap o una notifica specifica per cui non è presente alcuna classe, i provider generano un evento non specifico di . Per altre informazioni, vedere [Ricezione Enterprise eventi non specifici](#receiving-enterprise-nonspecific-events).

## <a name="receiving-enterprise-nonspecific-events"></a>Ricezione Enterprise-Nonspecific eventi

Un evento aziendale non specifico è un evento che non esegue il mapping da una notifica trap SNMPv1 o SNMPv2 a una delle sottoclassi di [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) o a qualsiasi classe che rappresenta un evento aziendale.

SEEP usa le classi **SNMPV1Notification** o **SNMPV2Notification** per eventi non specifici, mentre SREP usa le classi **SNMPv1ExtendedNotification** e **SNMPV2ExtendedNotification.**

Tutte e quattro le classi aziendali non specifiche derivano dalle classi [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification](snmpextendednotification.md) e hanno lo stesso formato. Entrambe le classi hanno la singola **proprietà VarBindList**. **VarBindList** è una matrice di istanze della **classe SnmpVarBind.** **SnmpVarBind** è una classe di base supportata dai provider di eventi SNMP per rappresentare un'istanza di un'associazione di variabili SNMP. Nella tabella seguente sono elencate le proprietà **di SnmpVarBind**.



| Proprietà         | Descrizione                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| Codifica         | Stringa che indica il tipo ASN.1 (Abstract Syntax Notation One) della variabile nella **proprietà** Value. |
| ObjectIdentifier | Stringa che identifica la variabile nella **proprietà** Value.                                                 |
| Valore            | Dati non elaborati in ottetti.                                                                                            |



 

Nelle classi **SnmpV1Notification** e **SnmpV2Notification** l'ordine di associazione delle variabili dall'evento SNMP è stato mantenuto ad eccezione delle prime due associazioni di variabili, TimeStamp e SnmpTrapOID. Queste associazioni sono state rimosse e vengono archiviate nelle proprietà **TimeStamp** e **Identification** della classe padre [SnmpNotification](snmpnotification.md) o [SnmpExtendedNotification.](snmpextendednotification.md)

 

 



