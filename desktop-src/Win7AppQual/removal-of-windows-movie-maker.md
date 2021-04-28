---
description: Rimozione di Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Rimozione di Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116269"
---
# <a name="removal-of-windows-movie-maker"></a>Rimozione di Windows Movie Maker

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Alta  
**Frequenza** - Media  


## <a name="description"></a>Descrizione

Microsoft sta deprecando e rimuovendo l'utilità Movie Maker Windows. ad esempio:

-   Tutti i punti di ingresso a Windows Movie Maker (ad esempio, Menu Start, Avvio > Esegui)
-   Tutti i file binari usati da Windows Movie Maker (tutti gli elementi presenti in %ProgramFiles% \\ Movie Maker)

Tuttavia, i file di progetto Movie Maker utente rimarranno nel sistema e saranno accessibili ad altre applicazioni che supportano questo formato di file.

## <a name="manifestation"></a>Manifestazione

Rimuovere i Movie Maker di Windows nei risultati seguenti:

-   Qualsiasi tentativo di avviare Windows Movie Maker con gli argomenti della riga di comando avrà esito negativo
-   Tutti i plug-in installati per abilitare nuove trasformazioni e animazioni rimarranno installati, ma non verranno esposti all'utente finale

## <a name="solution"></a>Soluzione

Per avere questa funzionalità in futuro, un utente dovrà installare un'applicazione simile da Microsoft o da un altro provider di software.

 

 



