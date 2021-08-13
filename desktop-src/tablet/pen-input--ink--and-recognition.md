---
description: Una nuova funzionalità interessante del Tablet PC è il sistema di input penna.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Input penna, input penna e riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8645a1a68499975ad3ef5cdafb8c07685e9ed9e600cdc9ca2129babaa8b953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716265"
---
# <a name="pen-input-ink-and-recognition"></a>Input penna, input penna e riconoscimento

Una nuova funzionalità interessante del Tablet PC è il sistema di input penna. Tutti i computer Tablet PC hanno un digitalizzatore sotto lo schermo che accetta l'input penna. Questo nuovo meccanismo di input richiede di pensare a come compilare applicazioni in modo specifico per Tablet PC. L'API (Application Programming Interface) della piattaforma Tablet PC consente di eseguire questa operazione.

## <a name="collection-data-management-and-recognition"></a>Raccolta, Gestione dati e riconoscimento

La piattaforma Tablet PC può essere suddivisa in tre aree distinte:

-   Raccolta input penna (oggetti utilizzati per raccogliere input penna dal digitalizzatore).
-   Gestione dei dati dell'input penna (oggetti usati per gestire l'input penna raccolto).
-   Riconoscimento input penna (oggetti usati per convertire l'input penna raccolto in altri tipi di dati, ad esempio testo).

L'immagine seguente illustra, a livello di alto livello, il funzionamento dell'API Raccolta input penna (API Penna), dell'API Ink Gestione dati (API Input penna) e dell'API Riconoscimento input penna (API Riconoscimento input penna) nella piattaforma Tablet PC.

![Illustraton che illustra il funzionamento dell'API penna, dell'API input penna e dell'API di riconoscimento](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

L'API della piattaforma Tablet PC è disponibile nelle API gestite e in una libreria COM. Gli argomenti seguenti descrivono gli oggetti nell'API e illustrano come le applicazioni usano questi oggetti:

-   [Raccolta input penna](ink-collection.md)
-   [Dati input penna](ink-data.md)
-   [Riconoscimento input penna](ink-recognition.md)
-   [Analisi input penna](ink-analysis.md)
-   [Riconoscimento della grafia in Windows Server 2008 R2](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



