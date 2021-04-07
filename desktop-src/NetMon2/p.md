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
# <a name="p-network-monitor"></a>P (Network Monitor)

<dl> <dt>

<span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**pacchetto**
</dt> <dd>

Vedere [*frame*](f.md).

</dd> <dt>

<span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**parser**
</dt> <dd>

Componente che rileva un protocollo specifico in un'acquisizione ritardata. Ogni parser può rilevare un protocollo. Una DLL del parser può tuttavia contenere più parser. Detto anche parser di protocollo.

</dd> <dt>

<span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**
</dt> <dd>

Un Network Monitor file di inizializzazione contenente un elenco di tutti i parser installati. Per ogni parser è presente una stringa di commento che descrive il parser, il set seguente del parser e qualsiasi file della Guida associato al parser. Il file INI del parser viene aggiornato quando Network Monitor chiama **ParserAutoInstallInfo** o quando la dll del parser chiama **CreateHandoffTable**.

</dd> <dt>

<span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**PerfMon**
</dt> <dd>

Uno strumento software che consente di visualizzare le variabili correlate alle prestazioni di rete che identificano l'attività di un processo.

</dd> <dt>

<span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**modalità promiscua**
</dt> <dd>

Stato in cui una scheda di rete copia tutti i frame che passano sulla rete, indipendentemente dall'indirizzo di destinazione in un buffer locale. Questa modalità consente Network Monitor di acquisire e visualizzare tutto il traffico di rete.

</dd> <dt>

<span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**Proprietà**
</dt> <dd>

Un elemento del protocollo in un parser che descrive un campo dati all'interno di un frame inviato usando tale protocollo.

</dd> <dt>

<span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**database proprietà**
</dt> <dd>

Un database interno che definisce tutte le proprietà supportate da un protocollo specifico. Il database delle proprietà contiene una struttura **PROPERTYINFO** per ogni proprietà definita dal parser. Network Monitor utilizza le informazioni nel database quando collega una definizione di proprietà a un'istanza della proprietà e quando formatta i dati della proprietà visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.

</dd> <dt>

<span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**livello di protocollo**
</dt> <dd>

Raggruppamento logico di proprietà del protocollo.

</dd> </dl>

 

 



