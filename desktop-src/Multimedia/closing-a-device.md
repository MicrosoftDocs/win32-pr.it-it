---
title: Chiusura di un dispositivo
description: Chiusura di un dispositivo
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- Comando MCI_CLOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395383"
---
# <a name="closing-a-device"></a>Chiusura di un dispositivo

Il comando [**Chiudi**](close.md) ([**MCI \_ Close**](mci-close.md)) rilascia l'accesso a un dispositivo o a un file. MCI libera un dispositivo quando tutte le attività che usano un dispositivo lo hanno chiuso. Per consentire a MCI di gestire i dispositivi, l'applicazione deve chiudere ogni dispositivo o file al termine dell'utilizzo.

Quando si chiude un dispositivo MCI esterno che usa i propri supporti anziché i file (ad esempio audio CD), il driver lascia il dispositivo alla modalità operativa corrente. Se quindi si chiude un dispositivo audio CD che esegue, anche se il driver di dispositivo viene rilasciato dalla memoria, il dispositivo audio CD continuerà a funzionare fino a quando non raggiunge la fine del contenuto.

> [!Note]  
> La chiusura di un'applicazione con i dispositivi Open MCI può impedire ad altre applicazioni di utilizzare tali dispositivi fino al riavvio di Windows.

 

 

 




