---
description: Notifica di rimozione del dispositivo
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notifica di rimozione del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3cc73aba6ad02eb1dfba095b6f45b9fa6c067c51dbe165f4ded86141dae1c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052021"
---
# <a name="device-removal-notification"></a>Notifica di rimozione del dispositivo

Se l'utente rimuove Plug and Play dispositivo utilizzato dal grafo, il gestore del grafico dei filtri invia un [**evento EC \_ DEVICE \_ LOST.**](ec-device-lost.md) Se il dispositivo diventa nuovamente disponibile, il gestore del grafico dei filtri invia un altro **evento EC \_ DEVICE \_ LOST.** Tuttavia, lo stato precedente del filtro di acquisizione non è più valido. L'applicazione deve ricompilare il grafo per usare il dispositivo.

DirectShow invia alcun evento quando un nuovo dispositivo è collegato. Per informazioni sulla disponibilità di un nuovo dispositivo, l'applicazione può monitorare i messaggi della finestra \_ DEVICECHANGE WM. Per altre informazioni, vedere "Gestione dei dispositivi" nella documentazione di Platform SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



