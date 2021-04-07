---
description: Glossario dei termini Network Monitor che iniziano con la lettera P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a95ed739acb6f4a59cf8c7a7edb760547f6469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049589"
---
# <a name="p-network-monitor"></a><span data-ttu-id="00cd9-103">P (Network Monitor)</span><span class="sxs-lookup"><span data-stu-id="00cd9-103">P (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="00cd9-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**pacchetto**</span><span class="sxs-lookup"><span data-stu-id="00cd9-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**packet**</span></span>
</dt> <dd>

<span data-ttu-id="00cd9-105">Vedere [*frame*](f.md).</span><span class="sxs-lookup"><span data-stu-id="00cd9-105">See [*frame*](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="00cd9-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**parser**</span><span class="sxs-lookup"><span data-stu-id="00cd9-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**parser**</span></span>
</dt> <dd>

<span data-ttu-id="00cd9-107">Componente che rileva un protocollo specifico in un'acquisizione ritardata.</span><span class="sxs-lookup"><span data-stu-id="00cd9-107">A component that detects a specific protocol in a delayed capture.</span></span> <span data-ttu-id="00cd9-108">Ogni parser può rilevare un protocollo.</span><span class="sxs-lookup"><span data-stu-id="00cd9-108">Each parser can detect one protocol.</span></span> <span data-ttu-id="00cd9-109">Una DLL del parser può tuttavia contenere più parser.</span><span class="sxs-lookup"><span data-stu-id="00cd9-109">However, one parser DLL may contain multiple parsers.</span></span> <span data-ttu-id="00cd9-110">Detto anche parser di protocollo.</span><span class="sxs-lookup"><span data-stu-id="00cd9-110">Also called a protocol parser.</span></span>

</dd> <dt>

<span data-ttu-id="00cd9-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span><span class="sxs-lookup"><span data-stu-id="00cd9-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span></span>
</dt> <dd>

<span data-ttu-id="00cd9-112">Un Network Monitor file di inizializzazione contenente un elenco di tutti i parser installati.</span><span class="sxs-lookup"><span data-stu-id="00cd9-112">A Network Monitor initialization file that contains a list of all the installed parsers.</span></span> <span data-ttu-id="00cd9-113">Per ogni parser è presente una stringa di commento che descrive il parser, il set seguente del parser e qualsiasi file della Guida associato al parser.</span><span class="sxs-lookup"><span data-stu-id="00cd9-113">For each parser there is a comment string that describes the parser, the follow set of the parser, and any Help file associated with the parser.</span></span> <span data-ttu-id="00cd9-114">Il file INI del parser viene aggiornato quando Network Monitor chiama **ParserAutoInstallInfo** o quando la dll del parser chiama **CreateHandoffTable**.</span><span class="sxs-lookup"><span data-stu-id="00cd9-114">The parser INI file is updated when Network Monitor calls **ParserAutoInstallInfo**, or when the parser DLL calls **CreateHandoffTable**.</span></span>

</dd> <dt>

<span data-ttu-id="00cd9-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**PerfMon**</span><span class="sxs-lookup"><span data-stu-id="00cd9-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**</span></span>
</dt> <dd>

<span data-ttu-id="00cd9-116">Uno strumento software che consente di visualizzare le variabili correlate alle prestazioni di rete che identificano l'attività di un processo.</span><span class="sxs-lookup"><span data-stu-id="00cd9-116">A software tool that allows you to view network performance-related variables that identify the activity of a process.</span></span>

</dd> <dt>

<span data-ttu-id="00cd9-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**modalità promiscua**</span><span class="sxs-lookup"><span data-stu-id="00cd9-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**promiscuous mode**</span></span>
</dt> <dd>

<span data-ttu-id="00cd9-118">Stato in cui una scheda di rete copia tutti i frame che passano sulla rete, indipendentemente dall'indirizzo di destinazione in un buffer locale.</span><span class="sxs-lookup"><span data-stu-id="00cd9-118">A state in which a network adapter card copies all the frames that pass over the network, regardless of the destination address to a local buffer.</span></span> <span data-ttu-id="00cd9-119">Questa modalità consente Network Monitor di acquisire e visualizzare tutto il traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="00cd9-119">This mode enables Network Monitor to capture and display all network traffic.</span></span>

</dd> <dt>

<span data-ttu-id="00cd9-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="00cd9-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="00cd9-121">Un elemento del protocollo in un parser che descrive un campo dati all'interno di un frame inviato usando tale protocollo.</span><span class="sxs-lookup"><span data-stu-id="00cd9-121">A protocol element in a parser that describes a data field within a frame that is sent by using that protocol.</span></span>

</dd> <dt>

<span data-ttu-id="00cd9-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**database proprietà**</span><span class="sxs-lookup"><span data-stu-id="00cd9-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**property database**</span></span>
</dt> <dd>

<span data-ttu-id="00cd9-123">Un database interno che definisce tutte le proprietà supportate da un protocollo specifico.</span><span class="sxs-lookup"><span data-stu-id="00cd9-123">An internal database that defines all the properties that a specific protocol supports.</span></span> <span data-ttu-id="00cd9-124">Il database delle proprietà contiene una struttura **PROPERTYINFO** per ogni proprietà definita dal parser.</span><span class="sxs-lookup"><span data-stu-id="00cd9-124">The property database contains a **PROPERTYINFO** structure for each property that the parser defines.</span></span> <span data-ttu-id="00cd9-125">Network Monitor utilizza le informazioni nel database quando collega una definizione di proprietà a un'istanza della proprietà e quando formatta i dati della proprietà visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="00cd9-125">Network Monitor uses the information in the database when it attaches a property definition to an instance of the property, and when it formats the property data that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="00cd9-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**livello di protocollo**</span><span class="sxs-lookup"><span data-stu-id="00cd9-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**protocol level**</span></span>
</dt> <dd>

<span data-ttu-id="00cd9-127">Raggruppamento logico di proprietà del protocollo.</span><span class="sxs-lookup"><span data-stu-id="00cd9-127">A logical grouping of protocol properties.</span></span>

</dd> </dl>

 

 



