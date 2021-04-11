---
description: Notifica di rimozione del dispositivo
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notifica di rimozione del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965867"
---
# <a name="device-removal-notification"></a>Notifica di rimozione del dispositivo

Se l'utente rimuove un Plug and Play dispositivo utilizzato dal grafo, il gestore del grafico dei filtri Invia un evento di [**\_ \_ perdita del dispositivo EC**](ec-device-lost.md) . Se il dispositivo torna nuovamente disponibile, il gestore del grafico dei filtri Invia un altro evento di **\_ \_ perdita del dispositivo EC** . Lo stato precedente del filtro di acquisizione, tuttavia, non è più valido. L'applicazione deve ricompilare il grafo per usare il dispositivo.

DirectShow non invia alcun evento quando viene collegato un nuovo dispositivo. Per informazioni sul momento in cui è disponibile un nuovo dispositivo, l'applicazione può monitorare \_ i messaggi della finestra WM DEVICECHANGE. Per ulteriori informazioni, vedere la sezione relativa alla gestione dei dispositivi nella documentazione di Platform SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



