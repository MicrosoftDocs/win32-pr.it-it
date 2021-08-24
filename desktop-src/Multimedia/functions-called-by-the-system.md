---
title: Funzioni chiamate dal sistema
description: Funzioni chiamate dal sistema
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- audio multimediale, funzioni ACM
- audio, funzioni ACM
- gestione compressione audio(ACM), funzioni
- ACM (gestione compressione audio),funzioni
- Funzioni di ACM
- funzioni callback
- gestione compressione audio,funzioni di callback
- ACM (gestione compressione audio), funzioni di callback
- Procedure hook
- Procedure relative ai driver
- gestione compressione audio,procedure hook
- ACM (gestione compressione audio), procedure hook
- gestione compressione audio,procedure del driver
- ACM (gestione compressione audio),procedure del driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b8a8c3615ae0124d4701f8d37d332e652d8390ef165cec8dc57d881cd328fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678620"
---
# <a name="functions-called-by-the-system"></a>Funzioni chiamate dal sistema

Il sistema chiama tre diversi tipi di funzioni definite dall'applicazione. Le funzioni di callback sono funzioni nell'applicazione chiamate dal sistema in risposta a una richiesta effettuata da un'applicazione. Le procedure hook consentono a un'applicazione di gestire la personalizzazione delle finestre di dialogo. Una procedura del driver è l'implementazione di un'applicazione del proprio codec, convertitore o filtro.

Le funzioni di callback hanno i nomi seguenti:

-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))

La maggior parte delle funzioni di enumerazione in ACM usa funzioni di callback. Ad esempio, quando si chiama una funzione di enumerazione, ACM enumera gli elementi chiamando ripetutamente l'applicazione tramite la funzione di callback.

Alcune funzioni non possono essere chiamate dall'interno di queste funzioni di callback. Le funzioni che non possono essere chiamate modificano le strutture ACM interne usate dalle funzioni di enumerazione. Le funzioni seguenti non devono essere chiamate dall'interno di una funzione di callback:

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

Il sistema chiama le funzioni seguenti per consentire a un'applicazione di gestire la personalizzazione delle finestre di dialogo:

-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

La funzione seguente viene specificata come prototipo che consente a un'applicazione di usare un codec, un convertitore o un filtro personalizzato. Una funzione conforme a questo prototipo può essere passata come argomento alla [**funzione acmDriverAdd.**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)

-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 