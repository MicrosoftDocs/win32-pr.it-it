---
description: Glossario dei Network Monitor termini che iniziano con la lettera P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de258a4394ae13ca71a62d90fd9ee9218862ab7845c7300fcfe509a3a286f34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555471"
---
# <a name="p-network-monitor"></a>P (Network Monitor)

<dl> <dt>

<span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**Pacchetto**
</dt> <dd>

Vedere [*frame*](f.md).

</dd> <dt>

<span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**Parser**
</dt> <dd>

Componente che rileva un protocollo specifico in un'acquisizione ritardata. Ogni parser può rilevare un protocollo. Tuttavia, una DLL del parser può contenere più parser. Chiamato anche parser di protocollo.

</dd> <dt>

<span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**
</dt> <dd>

Un Network Monitor di inizializzazione che contiene un elenco di tutti i parser installati. Per ogni parser è presente una stringa di commento che descrive il parser, il set seguente del parser e qualsiasi file della Guida associato al parser. Il file INI del parser viene aggiornato quando Network Monitor chiama **ParserAutoInstallInfo** o quando la DLL del parser chiama **CreateHandoffTable.**

</dd> <dt>

<span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**
</dt> <dd>

Strumento software che consente di visualizzare le variabili correlate alle prestazioni di rete che identificano l'attività di un processo.

</dd> <dt>

<span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**modalità promiscua**
</dt> <dd>

Stato in cui una scheda di scheda di rete copia tutti i frame che passano attraverso la rete, indipendentemente dall'indirizzo di destinazione in un buffer locale. Questa modalità consente Network Monitor acquisire e visualizzare tutto il traffico di rete.

</dd> <dt>

<span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**Proprietà**
</dt> <dd>

Elemento protocollo in un parser che descrive un campo dati all'interno di un frame inviato utilizzando tale protocollo.

</dd> <dt>

<span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**database delle proprietà**
</dt> <dd>

Database interno che definisce tutte le proprietà supportate da un protocollo specifico. Il database delle proprietà contiene **una struttura PROPERTYINFO** per ogni proprietà definita dal parser. Network Monitor usa le informazioni nel database quando collega una definizione di proprietà a un'istanza della proprietà e quando formatta i dati delle proprietà visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.

</dd> <dt>

<span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**livello di protocollo**
</dt> <dd>

Raggruppamento logico delle proprietà del protocollo.

</dd> </dl>

 

 



