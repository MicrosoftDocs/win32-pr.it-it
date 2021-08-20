---
title: Pulizia della directory virtuale
description: BITS estende le directory virtuali IIS per supportare i caricamenti.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce883bbd9f1af31bc7cafb10a2484f3a56ecbcffa7917a5a0e491a38da4701b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118422192"
---
# <a name="virtual-directory-cleanup"></a>Pulizia della directory virtuale

BITS estende le directory virtuali IIS per supportare i caricamenti. Ogni directory virtuale ha una proprietà di timeout della sessione (la proprietà della metabase [BITSSessionTimeout](bits-iis-extension-properties.md) di IIS) che specifica il periodo di tempo durante il quale il client BITS deve eseguire lo stato di avanzamento del caricamento del file. Se durante tale periodo non viene effettuato alcun avanzamento (il timer viene reimpostato quando viene effettuato lo stato di avanzamento), BITS chiude la sessione. Il timeout predefinito della sessione è di 14 giorni.

BITS aggiunge un elemento di lavoro [al Utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page) per ogni directory virtuale creata e abilitata. L'elemento di lavoro elimina le risorse associate alle sessioni chiuse. Per impostazione predefinita, la pulizia viene eseguita ogni 12 ore. Se due directory virtuali puntano alla stessa directory fisica, il processo di pulizia avviato da una delle directory elimina le risorse associate a tutte le sessioni chiuse nella directory fisica.

Usare la scheda Estensione BITS o le [Utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page) per modificare la pianificazione della pulizia in base alle esigenze dell'applicazione. È anche possibile chiamare il [**metodo IBITSExtensionSetup::GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) per recuperare un puntatore di interfaccia all'attività di pulizia associata alla directory virtuale.

> [!Note]  
> Se la Utilità di pianificazione è disabilitata dopo l'avirtualizzazione della directory virtuale, il processo di pulizia della directory virtuale non funzionerà.

 

 

 