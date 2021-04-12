---
description: Il provider Simple Network Management Protocol (SNMP) consente alle applicazioni client di accedere alle informazioni SNMP tramite Strumentazione gestione Windows (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI e SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233993"
---
# <a name="wmi-and-snmp"></a><span data-ttu-id="bb850-103">WMI e SNMP</span><span class="sxs-lookup"><span data-stu-id="bb850-103">WMI and SNMP</span></span>

<span data-ttu-id="bb850-104">Il provider Simple Network Management Protocol (SNMP) consente alle applicazioni client di accedere alle informazioni SNMP tramite Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bb850-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="bb850-105">Il provider SNMP non è installato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bb850-105">The SNMP provider is not installed by default.</span></span> <span data-ttu-id="bb850-106">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="bb850-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

<span data-ttu-id="bb850-107">Simple Network Management Protocol (SNMP) usa uno schema per definire gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="bb850-107">Simple Network Management Protocol (SNMP) uses a schema to define objects.</span></span> <span data-ttu-id="bb850-108">Lo schema è diverso dallo schema utilizzato in WMI.</span><span class="sxs-lookup"><span data-stu-id="bb850-108">The schema is different from the schema used in WMI.</span></span> <span data-ttu-id="bb850-109">Lo schema SNMPv1 e SNMPv2C è denominato struttura delle informazioni di gestione (SMI) ed è incluso in un pacchetto come file MIB (Management Information Base).</span><span class="sxs-lookup"><span data-stu-id="bb850-109">The SNMPv1 and SNMPv2C schema is called the Structure of Management Information (SMI), and is packaged as Management Information Base (MIB) files.</span></span> <span data-ttu-id="bb850-110">I file MIB definiscono gli oggetti utilizzando un linguaggio standard, ovvero Abstract Syntax Notation 1 (ASN. 1), e una serie di definizioni di macro utilizzate come modelli per la descrizione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="bb850-110">MIB files define objects using a standard language—Abstract Syntax Notation 1 (ASN.1)—and a number of macro definitions that serve as templates for describing the objects.</span></span> <span data-ttu-id="bb850-111">Le macro forniscono informazioni quali il nome dell'oggetto, l'identificatore, la sintassi, la descrizione, i diritti di accesso, le operazioni di protocollo e la codifica del protocollo.</span><span class="sxs-lookup"><span data-stu-id="bb850-111">The macros provide information such as the object name, identifier, syntax, description, access rights, protocol operations, and protocol encoding.</span></span> <span data-ttu-id="bb850-112">Nella tabella seguente viene elencato il modo in cui il provider SNMP gestisce diversi aspetti di un oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="bb850-112">The following table lists how the SNMP provider handles different aspects of a MIB object.</span></span>



| <span data-ttu-id="bb850-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="bb850-113">Topic</span></span>                                                    | <span data-ttu-id="bb850-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb850-114">Description</span></span>                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="bb850-115">Macro del tipo di notifica</span><span class="sxs-lookup"><span data-stu-id="bb850-115">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)   | <span data-ttu-id="bb850-116">Modalità di mapping della macro del **tipo di notifica** da SNMP a WMI.</span><span class="sxs-lookup"><span data-stu-id="bb850-116">How the **NOTIFICATION-TYPE** macro maps from SNMP to WMI.</span></span>  |
| [<span data-ttu-id="bb850-117">Macro di tipo oggetto</span><span class="sxs-lookup"><span data-stu-id="bb850-117">OBJECT-TYPE Macro</span></span>](object-type-macro.md)               | <span data-ttu-id="bb850-118">Modalità di mapping della macro di **tipo oggetto** da SNMP a WMI.</span><span class="sxs-lookup"><span data-stu-id="bb850-118">How the **OBJECT-TYPE** macro maps from SNMP to WMI.</span></span>        |
| [<span data-ttu-id="bb850-119">Macro convenzione testuale</span><span class="sxs-lookup"><span data-stu-id="bb850-119">TEXTUAL-CONVENTION Macro</span></span>](textual-convention-macro.md) | <span data-ttu-id="bb850-120">Come viene eseguito il mapping della macro della **convenzione testuale** da SNMP a WMI.</span><span class="sxs-lookup"><span data-stu-id="bb850-120">How the **TEXTUAL-CONVENTION** macro maps from SNMP to WMI.</span></span> |
| [<span data-ttu-id="bb850-121">Macro di tipo TRAP</span><span class="sxs-lookup"><span data-stu-id="bb850-121">TRAP-TYPE Macro</span></span>](trap-type-macro.md)                   | <span data-ttu-id="bb850-122">Come viene eseguito il mapping della macro di **tipo trap** da SNMP a WMI.</span><span class="sxs-lookup"><span data-stu-id="bb850-122">How the **TRAP-TYPE** macro maps from SNMP to WMI.</span></span>          |



 

<span data-ttu-id="bb850-123">Il provider SNMP è dotato di un compilatore che converte gli oggetti MIB in oggetti WMI.</span><span class="sxs-lookup"><span data-stu-id="bb850-123">The SNMP provider comes with a compiler that translates MIB objects into WMI objects.</span></span> <span data-ttu-id="bb850-124">Il compilatore SNMP può inoltre restituire errori o altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="bb850-124">The SNMP compiler can also output error or other messages.</span></span> <span data-ttu-id="bb850-125">Per ulteriori informazioni, vedere [messaggi di errore del compilatore SNMP](snmp-compiler-error-messages.md) e [messaggi informativi generali](general-information-messages.md).</span><span class="sxs-lookup"><span data-stu-id="bb850-125">For more information, see [SNMP compiler Error Messages](snmp-compiler-error-messages.md) and [General Information Messages](general-information-messages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb850-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bb850-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb850-127">Informazioni di riferimento su WMI</span><span class="sxs-lookup"><span data-stu-id="bb850-127">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="bb850-128">Provider WMI</span><span class="sxs-lookup"><span data-stu-id="bb850-128">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



