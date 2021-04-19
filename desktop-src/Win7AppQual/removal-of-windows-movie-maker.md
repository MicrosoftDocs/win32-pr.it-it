---
description: .
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Rimozione di Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a3336421ae2bde761aa1d4f238b5cd135ba64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317616"
---
# <a name="removal-of-windows-movie-maker"></a>Rimozione di Windows Movie Maker

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -alta  
**Frequenza** -media  


## <a name="description"></a>Descrizione

Microsoft sta deprecando e rimuovendo l'utilità Windows Movie Maker. ad esempio:

-   Tutti i punti di ingresso di Windows Movie Maker (ad esempio, menu Start, avvio > esecuzione)
-   Tutti i file binari usati da Windows Movie Maker (tutti gli elementi presenti in% ProgramFiles% \\ Movie Maker)

Tuttavia, i file di progetto di un utente Movie Maker rimarranno nel sistema e saranno accessibili ad altre applicazioni che supportano questo formato di file.

## <a name="manifestation"></a>Manifestazione

La rimozione di Windows Movie Maker comporta le seguenti operazioni:

-   Qualsiasi tentativo di avviare Windows Movie Maker con i relativi argomenti della riga di comando avrà esito negativo
-   Tutti i plug-in installati per abilitare nuove trasformazioni e animazioni rimarranno installati ma non verranno esposti all'utente finale

## <a name="solution"></a>Soluzione

Per avere questa funzionalità in futuro, un utente dovrà installare un'applicazione simile da Microsoft o da un altro fornitore di software.

 

 



