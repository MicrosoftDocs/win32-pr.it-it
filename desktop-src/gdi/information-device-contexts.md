---
description: Le informazioni sul controller di dominio vengono usate per recuperare i dati predefiniti del dispositivo.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Informazioni sui contesti di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974b861f47ffbd19566a5224d0c2705e9797e86abbe46005c6eb1687a9573378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779131"
---
# <a name="information-device-contexts"></a>Informazioni sui contesti di dispositivo

Le informazioni sul controller di dominio vengono usate per recuperare i dati predefiniti del dispositivo. Ad esempio, un'applicazione può chiamare la funzione [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) per creare un controller di dominio di informazioni per un particolare modello di stampante e quindi chiamare le funzioni [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) per recuperare gli attributi predefiniti della penna o del pennello. Poiché il sistema può recuperare le informazioni sul dispositivo senza creare le strutture normalmente associate agli altri tipi di contesti di dispositivo, un controller di dominio di informazioni comporta un sovraccarico molto inferiore e viene creato molto più velocemente rispetto a qualsiasi altro tipo. Al termine del recupero dei dati da parte di un'applicazione tramite un controller di dominio di informazioni, è necessario chiamare la [**funzione DeleteDC.**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)

 

 



