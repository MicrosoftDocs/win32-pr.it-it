---
title: Registrazione
description: Registrazione
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- MCI_RECORD comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27033dde148a6f99a1168eea4d6c0a97aea82881638ccb6d6f5535632e897148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805511"
---
# <a name="recording"></a>Registrazione

La specifica MCI generale supporta la registrazione con dispositivi digital-video, MIDI Sequencer, videocassetta (VCR) e waveform-audio; Tuttavia, solo i dispositivi waveform-audio e VCR implementano attualmente le funzionalità di registrazione. È possibile inserire o sovrascrivere le informazioni registrate in un file o in un record esistente in un nuovo file. Per registrare in un file esistente, aprire un dispositivo waveform-audio e un file come di consueto. Per registrare in un nuovo file, quando si apre il dispositivo specificare "new" come nome del dispositivo se si usa l'interfaccia della stringa di comando. Se si usa l'interfaccia del messaggio di comando, specificare un nome file di lunghezza zero.

Quando MCI crea un nuovo file per la registrazione, il formato dei dati viene impostato su un formato predefinito specificato dal driver di dispositivo. Per usare un formato diverso da quello predefinito, è possibile usare il [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)).

Per iniziare la registrazione, usare il [**comando record**](record.md) [**(o MCI \_ RECORD**](mci-record.md) e la [**struttura MCI RECORD \_ \_ PARMS).**](mci-record-parms.md)

Se si registra in modalità inserimento in un file esistente, è possibile usare i flag "from" (MCI FROM) e \_ "to" (MCI TO) del comando di record per specificare le posizioni iniziale e finale per la \_  registrazione. Ad esempio, se si registra in un file di 20 secondi e si inizia la registrazione a 5 secondi e si termina la registrazione a 10 secondi, il file risultante avrà una lunghezza di 25 secondi. Il file avrà un segmento di 5 secondi inserito 5 secondi nella registrazione originale.

Se si registra con la modalità di sovrascrittura in un file esistente, è possibile usare i flag "from" e "to" per specificare i percorsi iniziale e finale della sezione sovrascritta. Ad esempio, se si registra in un file di 20 secondi e si inizia la registrazione a 5 secondi e si termina la registrazione a 10 secondi, la registrazione è ancora lunga 20 secondi, ma la sezione che inizia da 5 secondi e termina a 10 secondi verrà sostituita.

Se non si specifica un percorso finale, la registrazione continua fino a quando non si invia un comando [**stop**](stop.md) ([**MCI \_ STOP**](mci-stop.md)) o fino a quando il driver non esaurirà lo spazio libero su disco. Se si registra in un nuovo file, è possibile omettere il flag "da" o impostarlo su zero per avviare la registrazione all'inizio di un nuovo file. È possibile specificare un percorso finale per terminare la registrazione durante la registrazione in un nuovo file.

Il [**comando di**](record.md) registrazione è talvolta accurato a meno di 1 secondo dalla posizione iniziale, ad esempio con i dispositivi vcr. Per registrare in modo più accurato, è necessario usare il [**comando cue**](cue.md) ([**MCI \_ CUE**](mci-cue.md)). Questo comando è riconosciuto dai dispositivi digital-video, VCR e waveform-audio. Per altre informazioni sulla registrazione con i dispositivi VCR, vedere [Servizi VCR](vcr-services.md).

## <a name="saving-a-recorded-file"></a>Salvataggio di un file registrato

Al termine della registrazione, usare il comando [**save**](save.md) (o [**MCI \_ SAVE**](mci-save.md) e la struttura [**MCI \_ SAVE \_ PARMS)**](mci-save-parms.md) per salvare la registrazione prima di chiudere il dispositivo.

> [!Note]  
> Se si chiude il dispositivo senza salvarlo, i dati registrati vengono persi.

 

## <a name="checking-input-levels-pcm-only"></a>Controllo dei livelli di input (solo PCM)

Per ottenere il livello del segnale di input prima della registrazione in un dispositivo di input audio-forma d'onda PCM (Pulse Code Modulation), usare il comando [**status**](status.md) ([**MCI \_ STATUS).**](mci-status.md) Specificare il flag "level" (o il flag MCI STATUS ITEM) e impostare il membro dwItem della struttura \_ \_ [**MCI \_ STATUS \_ PARMS**](mci-status-parms.md) su MCI WAVE STATUS  \_ \_ \_ LEVEL. Viene restituito il livello medio del segnale di input. Il valore del canale sinistro è nella parola più alta e il valore a destra o monocanale è nella parola meno importante.

Il livello di input è rappresentato come valore senza segno. Per gli esempi a 8 bit, questo valore è compreso nell'intervallo da 0 a 127 (0x7F). Per gli esempi a 16 bit, è compreso nell'intervallo da 0 a 32.767 (0x7FFF).

 

 




