---
description: Dopo aver determinato le funzionalità di un dispositivo telefonico, un'applicazione deve aprire il dispositivo prima di poter accedere alle funzioni sul telefono.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Apertura e chiusura di dispositivi telefonici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308288"
---
# <a name="opening-and-closing-phone-devices"></a>Apertura e chiusura di dispositivi telefonici

Dopo aver determinato le funzionalità di un dispositivo telefonico, un'applicazione deve aprire il dispositivo prima di poter accedere alle funzioni sul telefono. Dopo che un dispositivo telefonico è stato aperto correttamente, l'applicazione viene restituita un handle che rappresenta il telefono aperto. Un dispositivo telefonico può essere aperto in modalità diverse, offrendo così un modo strutturato per condividere un dispositivo telefonico.

La funzione [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) apre il dispositivo telefonico specificato per consentire all'applicazione di accedere alle funzioni sul telefono. Un dispositivo telefonico viene identificato per **phoneOpen** per mezzo del relativo identificatore del dispositivo, che viene passato come parametro *dwDeviceID* .

 

 



