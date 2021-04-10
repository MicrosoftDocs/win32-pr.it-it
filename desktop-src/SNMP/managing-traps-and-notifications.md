---
title: Gestione di trap e notifiche
description: L'applicazione WinSNMP deve registrarsi per ricevere trap e notifiche chiamando la funzione SnmpRegister con SNMPAPI \_ on. L'applicazione può annullare la registrazione e disabilitare i trap e le notifiche chiamando la funzione con SNMPAPI \_ off.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856633"
---
# <a name="managing-traps-and-notifications"></a><span data-ttu-id="00669-104">Gestione di trap e notifiche</span><span class="sxs-lookup"><span data-stu-id="00669-104">Managing Traps and Notifications</span></span>

<span data-ttu-id="00669-105">L'applicazione WinSNMP deve registrarsi per ricevere trap e notifiche chiamando la funzione [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) con snmpapi \_ on.</span><span class="sxs-lookup"><span data-stu-id="00669-105">The WinSNMP application must register to receive traps and notifications by calling the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) function with SNMPAPI\_ON.</span></span> <span data-ttu-id="00669-106">L'applicazione può annullare la registrazione e disabilitare i trap e le notifiche chiamando la funzione con SNMPAPI \_ off.</span><span class="sxs-lookup"><span data-stu-id="00669-106">The application can unregister and disable traps and notifications by calling the function with SNMPAPI\_OFF.</span></span>

<span data-ttu-id="00669-107">Quando l'applicazione chiama **SnmpRegister**, sono disponibili diverse opzioni.</span><span class="sxs-lookup"><span data-stu-id="00669-107">Several options are available when the application calls **SnmpRegister**.</span></span> <span data-ttu-id="00669-108">È possibile registrare o annullare la registrazione dell'applicazione per le seguenti trap e notifiche:</span><span class="sxs-lookup"><span data-stu-id="00669-108">The application can register or unregister for the following traps and notifications:</span></span>

-   <span data-ttu-id="00669-109">Un tipo di trap o notifica</span><span class="sxs-lookup"><span data-stu-id="00669-109">One type of trap or notification</span></span>
-   <span data-ttu-id="00669-110">Tutti i trap e le notifiche</span><span class="sxs-lookup"><span data-stu-id="00669-110">All traps and notifications</span></span>
-   <span data-ttu-id="00669-111">Tutte le origini di trap e richieste di notifica</span><span class="sxs-lookup"><span data-stu-id="00669-111">All sources of trap and notification requests</span></span>
-   <span data-ttu-id="00669-112">Trap e notifiche da tutte le entità di gestione</span><span class="sxs-lookup"><span data-stu-id="00669-112">Traps and notifications from all management entities</span></span>
-   <span data-ttu-id="00669-113">Trap e notifiche per ogni contesto</span><span class="sxs-lookup"><span data-stu-id="00669-113">Traps and notifications for every context</span></span>

<span data-ttu-id="00669-114">Per registrare e ricevere un trap o un tipo di notifica predefinito, è necessario che l'applicazione definisca un identificatore di oggetto (struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ) per ogni tipo predefinito.</span><span class="sxs-lookup"><span data-stu-id="00669-114">To register and receive a predefined trap or notification type, the application must define an object identifier (an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure) for each predefined type.</span></span> <span data-ttu-id="00669-115">La struttura deve contenere una sequenza di corrispondenza dei modelli per il tipo di trap o di notifica.</span><span class="sxs-lookup"><span data-stu-id="00669-115">The structure must contain a pattern-matching sequence for the type of trap or notification.</span></span> <span data-ttu-id="00669-116">RFC 1907, "Information Management base per la versione 2 del Simple Network Management Protocol (SNMPv2)", definisce gli identificatori degli oggetti trap e Notification.</span><span class="sxs-lookup"><span data-stu-id="00669-116">RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)," defines trap and notification object identifiers.</span></span>

<span data-ttu-id="00669-117">Per recuperare le notifiche e i dati trap in attesa per una sessione WinSNMP, è necessario che un'applicazione WinSNMP chiami la funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) con l'handle di sessione restituito dalla funzione [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="00669-117">To retrieve outstanding trap data and notifications for a WinSNMP session, a WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function with the session handle returned by the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span>

<span data-ttu-id="00669-118">Per ulteriori informazioni, vedere [invio di messaggi SNMP](sending-snmp-messages.md) e [ricezione di messaggi SNMP](receiving-snmp-messages.md).</span><span class="sxs-lookup"><span data-stu-id="00669-118">For more information, see [Sending SNMP Messages](sending-snmp-messages.md) and [Receiving SNMP Messages](receiving-snmp-messages.md).</span></span> <span data-ttu-id="00669-119">Per ulteriori informazioni sull'allocazione e la deallocazione di risorse per trap e notifiche, vedere [allocazione di oggetti memoria WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="00669-119">For additional information about allocation and deallocation of resources for traps and notifications, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




