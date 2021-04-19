---
title: Registrazione
description: Registrazione
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- Comando MCI_RECORD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4248b2d4bbdd984ad23a772f0adca04581afca1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297783"
---
# <a name="recording"></a>Registrazione

La specifica MCI generale supporta la registrazione con video digitali, sequencer MIDI, videoregistratore (VCR) e dispositivi Waveform-Audio; Tuttavia, solo i dispositivi audio e VCR attualmente implementano le funzionalità di registrazione. È possibile inserire o sovrascrivere le informazioni registrate in un file o un record esistente in un nuovo file. Per registrare un file esistente, aprire un dispositivo audio e un file di forma d'onda come in genere. Per registrare in un nuovo file, quando si apre il dispositivo specificare "nuovo" come nome del dispositivo se si usa l'interfaccia della stringa di comando. Se si usa l'interfaccia del messaggio di comando, specificare un nome file di lunghezza zero.

Quando MCI crea un nuovo file per la registrazione, il formato dei dati viene impostato su un formato predefinito specificato dal driver di dispositivo. Per usare un formato diverso dal formato predefinito, è possibile usare il comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)).

Per avviare la registrazione, utilizzare il comando [**record**](record.md) (o il record [**MCI \_**](mci-record.md) e la struttura [**\_ \_ parametri record MCI**](mci-record-parms.md) ).

Se si registra in modalità di inserimento in un file esistente, è possibile usare i flag "from" (MCI \_ from) e "to" (MCI \_ to) del comando **record** per specificare le posizioni di inizio e fine per la registrazione. Se, ad esempio, si registra in un file di 20 secondi e si inizia la registrazione a 5 secondi e si termina la registrazione in 10 secondi, il file risultante sarà di 25 secondi di lunghezza. Il file avrà un segmento di 5 secondi inserito 5 secondi nella registrazione originale.

Se si registra con la modalità di sovrascrittura in un file esistente, è possibile usare i flag "from" e "to" per specificare i percorsi iniziale e finale della sezione sovrascritta. Se, ad esempio, si registra in un file di 20 secondi e si inizia la registrazione a 5 secondi e si termina la registrazione in 10 secondi, è ancora presente una registrazione di 20 secondi, ma la sezione che inizia a 5 secondi e termina con 10 secondi verrà sostituita.

Se non si specifica un percorso finale, la registrazione continua fino a quando non si invia un comando [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) o finché il driver non esaurisce lo spazio libero su disco. Se si registra in un nuovo file, è possibile omettere il flag "from" o impostarlo su zero per avviare la registrazione all'inizio di un nuovo file. È possibile specificare una posizione finale per terminare la registrazione durante la registrazione in un nuovo file.

Il comando [**record**](record.md) è a volte accurato all'interno di un solo secondo della posizione iniziale, ad esempio con i dispositivi VCR. Per registrare in modo più accurato, è consigliabile usare il comando [**cue**](cue.md) ([**MCI \_ cue**](mci-cue.md)). Questo comando è riconosciuto da Digital-video, VCR e Waveform-Audio Devices. Per altre informazioni sulla registrazione con i dispositivi VCR, vedere [Servizi VCR](vcr-services.md).

## <a name="saving-a-recorded-file"></a>Salvataggio di un file registrato

Al termine della registrazione, utilizzare il comando [**Salva**](save.md) (oppure il comando [**MCI \_ Save**](mci-save.md) e la struttura di [**\_ salvataggio \_ parametri MCI**](mci-save-parms.md) ) per salvare la registrazione prima di chiudere il dispositivo.

> [!Note]  
> Se si chiude il dispositivo senza salvare, i dati registrati andranno perduti.

 

## <a name="checking-input-levels-pcm-only"></a>Verifica dei livelli di input (solo PCM)

Per ottenere il livello del segnale di input prima della registrazione in un dispositivo di input audio (PCM, Modulation Code Modulation), usare il comando [**status**](status.md) ([**\_ stato MCI**](mci-status.md)). Specificare il flag "Level" (o il \_ \_ flag elemento stato MCI e impostare il membro **dwItem** della struttura [**\_ \_ parametri stato MCI**](mci-status-parms.md) su MCI \_ Wave \_ status \_ Level). Viene restituito il livello medio del segnale di input. Il valore del canale sinistro si trova nella parola più significativa e il valore a destra o mono canale si trova nella parola di ordine inferiore.

Il livello di input è rappresentato come un valore senza segno. Per gli esempi a 8 bit, questo valore è compreso tra 0 e 127 (0x7F). Per gli esempi a 16 bit, si trova nell'intervallo compreso tra 0 e 32.767 (0x7FFF).

 

 




