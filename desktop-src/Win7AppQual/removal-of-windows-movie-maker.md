---
description: Rimozione di Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Rimozione di Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538032d589439ccc0966bc151568813eed3d1946cd2cb8ea7d9314246edb19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098521"
---
# <a name="removal-of-windows-movie-maker"></a>Rimozione di Windows Movie Maker

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Alta  
**Frequenza** - Media  


## <a name="description"></a>Descrizione

Microsoft sta deprecando e rimuovendo l'Windows Movie Maker di installazione. ad esempio:

-   Tutti i punti di ingresso Windows Movie Maker (ad esempio, Menu Start, Avvia > Esegui)
-   Tutti i file binari usati da Windows Movie Maker (tutti gli elementi presenti in %ProgramFiles% \\ Movie Maker)

Tuttavia, i file di progetto Movie Maker utente rimarranno nel sistema e saranno accessibili ad altre applicazioni che supportano questo formato di file.

## <a name="manifestation"></a>Manifestazione

Rimuovere i Windows Movie Maker risultati seguenti:

-   Qualsiasi tentativo di avviare Windows Movie Maker con gli argomenti della riga di comando avrà esito negativo
-   Tutti i plug-in installati per abilitare nuove trasformazioni e animazioni rimarranno installati, ma non verranno esposti all'utente finale

## <a name="solution"></a>Soluzione

Per avere questa funzionalità in futuro, un utente dovrà installare un'applicazione simile da Microsoft o da un altro provider di software.

 

 



