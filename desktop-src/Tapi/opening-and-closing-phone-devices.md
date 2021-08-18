---
description: Dopo aver determinato le funzionalità di un dispositivo telefonico, un'applicazione deve aprire il dispositivo prima di poter accedere alle funzioni in tale telefono.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Apertura e chiusura di Telefono dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dacda3e98e96ed4a11334443a7b99b949e6d1b3823e42e1790c5a346b52dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012521"
---
# <a name="opening-and-closing-phone-devices"></a>Apertura e chiusura di Telefono dispositivi

Dopo aver determinato le funzionalità di un dispositivo telefonico, un'applicazione deve aprire il dispositivo prima di poter accedere alle funzioni in tale telefono. Dopo l'apertura di un dispositivo telefonico, all'applicazione viene restituito un handle che rappresenta il telefono aperto. Un dispositivo telefonico può essere aperto in modalità diverse, offrendo in tal modo un modo strutturato per condividere un dispositivo.

La [**funzione phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) apre il dispositivo telefonico specificato per concedere all'applicazione l'accesso alle funzioni nel telefono. Un dispositivo telefonico viene identificato **per phoneOpen** tramite il relativo identificatore di dispositivo, che viene passato come *parametro dwDeviceID.*

 

 



