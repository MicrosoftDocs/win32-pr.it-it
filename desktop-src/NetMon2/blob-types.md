---
description: Network Monitor usa tre tipi di oggetti binari di grandi dimensioni (BLOB) per selezionare e connettere schede di interfaccia di rete (NIC), acquisire dati e modificare i dati di NPP.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: Tipi di BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233838"
---
# <a name="blob-types"></a>Tipi di BLOB

Network Monitor usa tre tipi di oggetti binari di grandi dimensioni (BLOB) per selezionare e connettere schede di interfaccia di rete (NIC), acquisire dati e modificare i dati di NPP.

## <a name="npp-blob"></a>BLOB NPP

Le applicazioni usano i BLOB NPP per connettersi a una scheda di interfaccia di rete specifica tramite un oggetto NPP. (L'applicazione effettua la connessione con una chiamata a **CreateNPPInterface** e ai dati relativi alla posizione nel BLOB di NPP). Un'applicazione può inoltre archiviare i dati di configurazione nel BLOB NPP per configurare l'oggetto NPP. Inoltre, un'applicazione che salva il BLOB di NPP non deve passare attraverso il Finder per riutilizzare tale BLOB.

## <a name="filter-blob"></a>Filtra BLOB

Un BLOB di filtri contiene criteri definiti dall'applicazione che è possibile usare per selezionare un oggetto NPP e una scheda di interfaccia di rete. Ad esempio, un'applicazione può richiedere una scheda di interfaccia di rete specifica, solo schede Ethernet o schede che supportano una frequenza di acquisizione dei frame specifica.

## <a name="special-blob"></a>BLOB speciale

Quando un NPP richiede dati aggiuntivi prima di poter restituire un BLOB NPP a un'applicazione, l'oggetto NPP usa un BLOB speciale. In genere, l'applicazione non necessita né USA BLOB speciali, quindi non viene restituita a un'applicazione a meno che non sia impostato un flag specifico in una chiamata di funzione. Ad esempio, un NPP remoto usa un BLOB speciale perché è necessario un nome di percorso per effettuare una connessione. Un'applicazione che riceve un BLOB speciale NPP remoto può aggiungere la stringa e richiamarla nel Finder per ottenere una tabella BLOB NPP. Per altre informazioni, vedere [voci speciali](special-blob-entries.md)per i BLOB.

 

 



