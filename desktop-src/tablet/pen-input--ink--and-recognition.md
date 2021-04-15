---
description: Una nuova funzionalità interessante di Tablet PC è il sistema di input penna.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Input penna, input penna e riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568192"
---
# <a name="pen-input-ink-and-recognition"></a>Input penna, input penna e riconoscimento

Una nuova funzionalità interessante di Tablet PC è il sistema di input penna. Tutti i computer Tablet PC hanno un digitalizzatore sotto la schermata che accetta input penna. Questo nuovo meccanismo di input richiede di considerare come compilare applicazioni specifiche per Tablet PC. La piattaforma Tablet PC Application Programming Interface (API) consente di eseguire questa operazione.

## <a name="collection-data-management-and-recognition"></a>Raccolta, Gestione dati e riconoscimento

La piattaforma Tablet PC può essere divisa in tre aree distinte:

-   Raccolta di input penna (oggetti utilizzati per raccogliere input penna dal digitalizzatore).
-   Gestione dati Ink (oggetti utilizzati per gestire l'input penna).
-   Riconoscimento dell'input penna (oggetti utilizzati per convertire l'input penna raccolto in altri tipi di dati, ad esempio testo).

La figura seguente illustra, a livello generale, il modo in cui l'API della raccolta di input penna (API penna), l'API Gestione dati input penna e l'API di riconoscimento input penna (API di riconoscimento) funzionano insieme nella piattaforma Tablet PC.

![Illustraton che illustra in che modo l'API Pen, l'API Ink e l'API di riconoscimento collaborano](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

L'API della piattaforma Tablet PC è disponibile nelle API gestite e in una libreria COM. Negli argomenti seguenti vengono descritti gli oggetti nell'API e viene illustrato il modo in cui le applicazioni utilizzano questi oggetti:

-   [Raccolta di input penna](ink-collection.md)
-   [Dati Ink](ink-data.md)
-   [Riconoscimento input penna](ink-recognition.md)
-   [Analisi dell'input penna](ink-analysis.md)
-   [Riconoscimento della grafia in Windows Server 2008 R2](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



