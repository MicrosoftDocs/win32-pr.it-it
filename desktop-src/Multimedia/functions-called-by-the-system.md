---
title: Funzioni chiamate dal sistema
description: Funzioni chiamate dal sistema
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- audio multimediale, funzioni ACM
- audio, funzioni ACM
- Gestione compressione audio (ACM), funzioni
- ACM (Gestione compressione audio), funzioni
- Funzioni ACM
- funzioni callback
- Gestione compressione audio (ACM), funzioni di callback
- ACM (Gestione compressione audio), funzioni di callback
- procedure Hook
- procedure per i driver
- Gestione compressione audio (ACM), procedure Hook
- ACM (Gestione compressione audio), procedure Hook
- Gestione compressione audio (ACM), procedure per i driver
- ACM (Gestione compressione audio), procedure per i driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299677"
---
# <a name="functions-called-by-the-system"></a>Funzioni chiamate dal sistema

Il sistema chiama tre tipi diversi di funzioni definite dall'applicazione. Le funzioni di callback sono funzioni nell'applicazione chiamate dal sistema in risposta a una richiesta effettuata da un'applicazione. Le procedure Hook consentono a un'applicazione di gestire la personalizzazione delle finestre di dialogo. Una procedura di driver è l'implementazione del proprio codec, convertitore o filtro di un'applicazione.

Le funzioni di callback hanno i nomi seguenti:

-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))

La maggior parte delle funzioni di enumerazione in ACM utilizza funzioni di callback. Ad esempio, quando si chiama una funzione di enumerazione, l'ACM enumera gli elementi chiamando ripetutamente l'applicazione tramite la funzione di callback.

Alcune funzioni non possono essere chiamate dall'interno di queste funzioni di callback. Le funzioni che non possono essere chiamate modificano le strutture ACM interne utilizzate dalle funzioni di enumerazione. Le funzioni seguenti non devono essere chiamate dall'interno di una funzione di callback:

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

Il sistema chiama le funzioni seguenti per consentire a un'applicazione di gestire la personalizzazione delle finestre di dialogo:

-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

La funzione seguente viene specificata come prototipo che consente a un'applicazione di utilizzare un codec, un convertitore o un filtro personalizzato. Una funzione conforme a questo prototipo può essere passata come argomento alla funzione [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .

-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 