---
title: Utilizzo di una funzione di callback per elaborare i messaggi del driver
description: Utilizzo di una funzione di callback per elaborare i messaggi del driver
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- audio Waveform, funzioni di callback
- blocchi di dati audio, funzioni di callback
- audio Waveform, elaborazione dei messaggi del driver
- blocchi di dati audio, elaborazione dei messaggi del driver
- elaborazione dei messaggi del driver
- waveInOpen (funzione)
- waveOutOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299730"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a>Utilizzo di una funzione di callback per elaborare i messaggi del driver

È possibile scrivere una funzione di callback personalizzata per elaborare i messaggi inviati dal driver di dispositivo. Per usare una funzione di callback, specificare il \_ flag della funzione di callback nel parametro *fdwOpen* e l'indirizzo del callback nel parametro *dwCallback* della funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .

I messaggi inviati a una funzione di callback sono simili ai messaggi inviati a una finestra, con la differenza che hanno due parametri **DWORD** anziché **uint** e un parametro **DWORD** . Per informazioni dettagliate su questi messaggi, vedere la pagina relativa alla [riproduzione di file di Waveform-Audio](playing-waveform-audio-files.md).

Per passare i dati dell'istanza da un'applicazione a una funzione di callback, usare una delle tecniche seguenti:

-   Passare i dati dell'istanza utilizzando il parametro *dwInstance* della funzione che apre il driver di dispositivo.
-   Passare i dati dell'istanza usando il membro **dwUser** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica un blocco di dati audio da inviare a un driver di dispositivo.

Se sono necessari più di 32 bit di dati dell'istanza, passare un puntatore a una struttura contenente le informazioni aggiuntive.

 

 