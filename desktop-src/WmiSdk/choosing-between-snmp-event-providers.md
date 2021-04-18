---
description: I provider di eventi SNMP ricevono pacchetti di eventi SNMP dallo stack WINSNMP e convertono le informazioni incluse nei pacchetti in eventi WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Scelta tra i provider di eventi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315738"
---
# <a name="choosing-between-snmp-event-providers"></a><span data-ttu-id="0ebb2-103">Scelta tra i provider di eventi SNMP</span><span class="sxs-lookup"><span data-stu-id="0ebb2-103">Choosing Between SNMP Event Providers</span></span>

<span data-ttu-id="0ebb2-104">I provider di eventi SNMP ricevono pacchetti di eventi SNMP dallo stack WINSNMP e convertono le informazioni incluse nei pacchetti in eventi WMI.</span><span class="sxs-lookup"><span data-stu-id="0ebb2-104">SNMP event providers receive SNMP event packets from the WINSNMP stack and translate the information included in the packets into WMI events.</span></span>

<span data-ttu-id="0ebb2-105">WMI include i due provider di eventi SNMP seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ebb2-105">WMI includes the following two SNMP event providers:</span></span>

-   <span data-ttu-id="0ebb2-106">Provider di eventi incapsulato SNMP (Filtra)</span><span class="sxs-lookup"><span data-stu-id="0ebb2-106">SNMP Encapsulated Event provider (SEEP)</span></span>

    <span data-ttu-id="0ebb2-107">Il provisioning incapsulato indica che l'istanza dell'evento dispone di proprietà semplici che descrivono le informazioni mappate direttamente dal trap SNMP.</span><span class="sxs-lookup"><span data-stu-id="0ebb2-107">Encapsulated provision means that the event instance has simple properties describing the information mapped directly from the SNMP trap.</span></span>

-   <span data-ttu-id="0ebb2-108">Provider di eventi SNMP referente (SREP)</span><span class="sxs-lookup"><span data-stu-id="0ebb2-108">SNMP Referent Event provider (SREP)</span></span>

    <span data-ttu-id="0ebb2-109">Il provisioning referente astrae le informazioni presenti all'interno del trap SNMP in modo che le proprietà che condividono la stessa classe e l'istanza vengano presentate come oggetti incorporati.</span><span class="sxs-lookup"><span data-stu-id="0ebb2-109">Referent provision abstracts the information present within the SNMP trap so that properties which share the same class and instance are presented as embedded objects.</span></span> <span data-ttu-id="0ebb2-110">Questo consente di recuperare l'istanza univoca, a cui è associata la trap, dopo la ricezione dell'evento usando il \_ \_ RelPath SNMP.</span><span class="sxs-lookup"><span data-stu-id="0ebb2-110">This allows for the unique instance, with which the trap is associated, to be retrieved after the receipt of the event, using the SNMP \_\_RELPATH.</span></span>

> [!Note]  
> <span data-ttu-id="0ebb2-111">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="0ebb2-111">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="0ebb2-112">Indipendentemente dal fatto che l'evento SNMP sia un trap SNMPv1 o una notifica SNMPv2C, lo stack lo segnala come notifica SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="0ebb2-112">Regardless of whether the SNMP event is an SNMPv1 trap or an SNMPv2C notification, the stack reports it as an SNMPv2 notification.</span></span> <span data-ttu-id="0ebb2-113">Pertanto, i provider di eventi elaborano tutti gli eventi SNMP come notifiche di SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="0ebb2-113">Therefore, the event providers process all SNMP events as SNMPv2 notifications.</span></span>

<span data-ttu-id="0ebb2-114">Per descrivere gli eventi SNMP ai consumer WMI, ogni provider di eventi supporta una gerarchia di classi che deriva dalla classe di sistema [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="0ebb2-114">To describe the SNMP events to WMI consumers, each event provider supports a hierarchy of classes that derives from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) system class.</span></span> <span data-ttu-id="0ebb2-115">La classe [SNMPNotification](snmpnotification.md) è la classe padre per la gerarchia di infiltrazione. la classe [SNMPExtendedNotification](snmpextendednotification.md) è la classe padre per la gerarchia di SREP.</span><span class="sxs-lookup"><span data-stu-id="0ebb2-115">The [SNMPNotification](snmpnotification.md) class is the parent class for the SEEP hierarchy; the [SNMPExtendedNotification](snmpextendednotification.md) class is the parent class for the SREP hierarchy.</span></span>

 

 



