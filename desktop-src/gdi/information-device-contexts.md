---
description: Il controller di dominio di informazioni viene usato per recuperare i dati predefiniti del dispositivo.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Contesti di dispositivi informativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002e9d5ebb6831f9e2251e76049e586ac3e84056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528326"
---
# <a name="information-device-contexts"></a>Contesti di dispositivi informativi

Il controller di dominio di informazioni viene usato per recuperare i dati predefiniti del dispositivo. Ad esempio, un'applicazione può chiamare la funzione [**create**](/windows/desktop/api/Wingdi/nf-wingdi-createica) per creare un controller di dominio di informazioni per un particolare modello di stampante e quindi chiamare le funzioni [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) per recuperare gli attributi predefiniti della penna o del pennello. Poiché il sistema è in grado di recuperare informazioni sul dispositivo senza creare le strutture normalmente associate ad altri tipi di contesti di dispositivo, un controller di dominio di informazioni comporta un sovraccarico molto inferiore e viene creato notevolmente più velocemente rispetto a qualsiasi altro tipo. Al termine del recupero dei dati da parte di un'applicazione tramite un controller di dominio di informazioni, deve chiamare la funzione [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .

 

 



