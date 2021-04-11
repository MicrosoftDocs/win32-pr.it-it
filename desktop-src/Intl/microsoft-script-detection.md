---
description: Il servizio di rilevamento script ELS è denominato rilevamento script Microsoft.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Rilevamento script Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130311"
---
# <a name="microsoft-script-detection"></a>Rilevamento script Microsoft

Il servizio di rilevamento script ELS è denominato rilevamento script Microsoft. Questo servizio consente alle applicazioni di rilevare gli script in cui viene scritto il testo. La controparte NLS (National Language Support) di un servizio di rilevamento script è la funzione [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) . Il servizio ELS, tuttavia, recupera inoltre gli intervalli di testo che appartengono a ogni sistema di scrittura.

## <a name="input-to-microsoft-script-detection"></a>Input per il rilevamento di script Microsoft

L'input per il servizio rilevamento script Microsoft è un testo UTF-16 per il quale il servizio determina gli intervalli di script.

## <a name="output-of-microsoft-script-detection"></a>Output del rilevamento di script Microsoft

L'output del servizio Microsoft Script Detection è una matrice di intervalli, ognuno dei quali contiene una stringa UTF-16 con terminazione null con il nome Unicode specificato del sistema di scrittura associato. Il servizio segnala i caratteri comuni (Rachele) e ereditato (Qaai) normali come appartenenti all'intervallo di script precedente. L'inizio dei caratteri comuni e ereditati viene segnalato come appartenente al successivo intervallo di script. Se tutti i caratteri nel testo di input sono comuni o ereditati, l'output del servizio è un singolo intervallo con la stringa vuota come dati.

## <a name="microsoft-script-detection-operation"></a>Operazione di rilevamento script Microsoft

Il servizio Microsoft Script Detection esegue il mapping dei punti di codice appartenenti all'intervallo comune al sistema di scrittura precedente. In alternativa, il servizio può eseguire il mapping dei punti di codice al sistema di scrittura successivo se i punti di codice si trovano all'inizio della stringa di input. Non è necessario che l'applicazione gestisca l'intervallo comune.

## <a name="microsoft-script-detection-guid"></a>GUID rilevamento script Microsoft

Il GUID per il servizio Microsoft Rilevamento lingua viene dichiarato in Elssrvc. h, come illustrato nel codice seguente.


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui servizi linguistici estesi](about-extended-linguistic-services.md)
</dt> </dl>

 

 



