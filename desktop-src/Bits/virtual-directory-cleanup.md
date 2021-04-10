---
title: Pulizia directory virtuale
description: BITS estende le directory virtuali IIS per supportare i caricamenti.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963251"
---
# <a name="virtual-directory-cleanup"></a>Pulizia directory virtuale

BITS estende le directory virtuali IIS per supportare i caricamenti. Ogni directory virtuale dispone di una proprietà di timeout della sessione (la proprietà della metabase IIS [BITSSessionTimeout](bits-iis-extension-properties.md) ) che specifica il periodo di tempo in cui il client BITS deve eseguire lo stato di avanzamento del caricamento del file. Se durante tale periodo non viene eseguito alcun avanzamento (il timer viene reimpostato quando viene eseguito lo stato di avanzamento), BITS chiude la sessione. Il timeout della sessione predefinito è di 14 giorni.

BITS aggiunge un elemento di lavoro al [utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page) per ogni directory virtuale creata e abilitata. L'elemento di lavoro elimina le risorse associate alle sessioni chiuse. Per impostazione predefinita, la pulizia viene eseguita ogni 12 ore. Se due directory virtuali puntano alla stessa directory fisica, il processo di pulizia avviato da una delle directory Elimina le risorse associate a tutte le sessioni chiuse nella directory fisica.

Utilizzare la scheda estensione BITS o le interfacce [utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page) per modificare la pianificazione della pulizia nel modo appropriato per l'applicazione. È anche possibile chiamare il metodo [**IBITSExtensionSetup:: GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) per recuperare un puntatore di interfaccia all'attività di pulizia associata alla directory virtuale.

> [!Note]  
> Se il Utilità di pianificazione viene disabilitato dopo l'abilitazione della directory virtuale, il processo di pulizia della directory virtuale non funzionerà.

 

 

 