---
description: Un dispositivo di imaging viene rappresentato in Windows Image Acquisition (WIA) come albero gerarchico di oggetti elemento WIA (interfacce IWiaItem).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Utilizzo di oggetti dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129387"
---
# <a name="using-wia-device-objects"></a>Utilizzo di oggetti dispositivo WIA

Un dispositivo di imaging viene rappresentato in Windows Image Acquisition (WIA) come albero gerarchico di oggetti elemento WIA (interfacce [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ). In genere, la radice di questo albero di elementi rappresenta il dispositivo stesso, mentre gli altri elementi nell'albero rappresentano le immagini, per una fotocamera o per le aree di analisi, per uno scanner.

Le applicazioni utilizzano Gestione dispositivi WIA per creare ed enumerare i dispositivi WIA. Le sezioni seguenti illustrano come creare e usare i dispositivi WIA:

-   [Selezione di un dispositivo](-wia-selecting-a-device.md)
-   [Dispositivi della fotocamera WIA](-wia-wia-camera-devices.md)
-   [Dispositivi scanner WIA](-wia-wia-scanner-devices.md)

 

 



