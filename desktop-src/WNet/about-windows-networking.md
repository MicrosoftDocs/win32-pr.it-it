---
title: Informazioni sulla rete di Windows
description: Le applicazioni possono utilizzare le funzioni WNet per aggiungere e annullare le connessioni di rete e recuperare informazioni sulla configurazione corrente della rete.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Windows Networking WNet, descritto
- WNet WNet, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045320"
---
# <a name="about-windows-networking"></a>Informazioni sulla rete di Windows

Le applicazioni possono utilizzare le funzioni WNet per aggiungere e annullare le connessioni di rete e recuperare informazioni sulla configurazione corrente della rete.

Nella figura seguente viene illustrata la struttura di una rete tipica.

![struttura di rete tipica](images/csnet-01.png)

Nella figura precedente, la gerarchia per le risorse di Windows NT Server/Windows 2000 Server è fornita in dettaglio come provider di rete \# 1. Le risorse di rete di altri provider hanno sistemi gerarchici diversi. Un'applicazione non necessita di informazioni sulla gerarchia prima che inizi a funzionare con una rete. Può procedere dalla radice di rete (ovvero la risorsa del contenitore più in alto) e recuperare le informazioni sulle risorse della rete in base alle esigenze.

Le risorse di rete che contengono altre risorse sono denominate *contenitori*. Le risorse del contenitore sono incluse nelle caselle della figura precedente.

Le risorse che non contengono altre risorse sono denominate *oggetti*. Nella figura precedente, SharePoint \# 1 e SharePoint \# 2 sono oggetti. *SharePoint* è un oggetto accessibile attraverso la rete. Esempi di SharePoint includono stampanti e directory condivise.

 

 




