---
title: Errori MCI generali
description: Errori MCI generali
ms.assetid: be9c4a2b-44bc-410c-be74-ba55bb4e785b
keywords:
- MCIERR return values,general errors
- riferimento multimediale,errori MCI
- informazioni di riferimento per elementi multimediali, errori MCI
- Media Control Interface (MCI), errori generali
- MCI (Media Control Interface),errori generali
- informazioni di riferimento per MCI, errori generali
- Riferimento MCI, errori generali
- Media Control Interface (MCI), errori
- MCI (Media Control Interface),errori
- informazioni di riferimento per MCI, errori
- riferimento MCI, errori
- MciSendCommand - funzione
- Funzione mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f402e532f1bcf22a9136764647c91b1f4d54479f932c509ec172c1d973f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375158"
---
# <a name="general-mci-errors"></a>Errori MCI generali

I valori di errore seguenti possono essere restituiti dalla [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) o [**mciSendString:**](/previous-versions//dd757161(v=vs.85))



| Valore                            | Significato                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ BAD \_ TIME \_ FORMAT        | Il valore specificato per il formato dell'ora non è valido.                                                                                                         |
| MCIERR \_ NON È IN GRADO DI CARICARE IL \_ \_ DRIVER     | Il driver di dispositivo specificato non verrà caricato correttamente.                                                                                                         |
| MCIERR \_ NON PUÒ USARE \_ \_ ALL         | Il nome del dispositivo "all" non è consentito per questo comando.                                                                                                      |
| MCIERR \_ CREATEWINDOW             | Impossibile creare o usare la finestra.                                                                                                                             |
| LUNGHEZZA DEL DISPOSITIVO \_ \_ MCIERR           | Il nome del dispositivo o del driver è troppo lungo. Specificare un nome di dispositivo o driver di meno di 79 caratteri.                                                     |
| BLOCCO DEL DISPOSITIVO MCIERR \_ \_           | Il dispositivo è in fase di chiusura. Attendere alcuni secondi, quindi riprovare.                                                                                         |
| IL DISPOSITIVO MCIERR \_ \_ NON È \_ INSTALLATO   | Il dispositivo specificato non è installato nel sistema. Usare l'opzione Driver dal Pannello di controllo per installare il dispositivo.                                   |
| DISPOSITIVO MCIERR \_ \_ NON \_ PRONTO       | Il driver di dispositivo non è pronto.                                                                                                                             |
| MCIERR \_ DEVICE \_ OPEN             | Il nome del dispositivo è già usato come alias da questa applicazione. Usare un alias univoco.                                                                        |
| LUNGHEZZA \_ \_ ORD DEL DISPOSITIVO \_ MCIERR      | Il nome del dispositivo o del driver è troppo lungo. Specificare un nome di dispositivo o driver di meno di 79 caratteri.                                                     |
| TIPO DI DISPOSITIVO MCIERR \_ \_ \_ OBBLIGATORIO   | Impossibile trovare il dispositivo specificato nel sistema. Verificare che il dispositivo sia installato e che il nome del dispositivo sia stato digitato correttamente.                            |
| MCIERR \_ DRIVER                   | Il driver di dispositivo presenta un problema. Rivolgersi al produttore del dispositivo per ottenere un nuovo driver.                                                      |
| DRIVER MCIERR \_ \_ INTERNO         | Il driver di dispositivo presenta un problema. Rivolgersi al produttore del dispositivo per ottenere un nuovo driver.                                                      |
| \_ALIAS DUPLICATO DI MCIERR \_         | L'alias specificato è già utilizzato in questa applicazione. Usare un alias univoco.                                                                                |
| ESTENSIONE MCIERR \_ \_ NON \_ TROVATA    | All'estensione specificata non è associato alcun tipo di dispositivo. Specificare un tipo di dispositivo.                                                                       |
| CARATTERI AGGIUNTIVI DI \_ \_ MCIERR        | È necessario racchiudere una stringa tra virgolette. I caratteri dopo le virgolette di chiusura non sono validi.                                              |
| FILE MCIERR \_ \_ NON \_ TROVATO         | Il file richiesto non è stato trovato. Verificare che il percorso e il nome file siano corretti.                                                                             |
| FILE MCIERR \_ \_ NON \_ SALVATO         | Il file non è stato salvato. Verificare che lo spazio su disco del sistema sia sufficiente o che la connessione di rete sia intatta.                                                |
| MCIERR \_ FILE \_ READ               | Lettura dal file non riuscita. Assicurarsi che il file sia presente nel sistema o che il sistema abbia una connessione di rete intatta.                             |
| MCIERR \_ FILE \_ WRITE              | Scrittura nel file non riuscita. Verificare che lo spazio su disco del sistema sia sufficiente o che la connessione di rete sia intatta.                                            |
| NOME FILE MCIERR \_ \_ OBBLIGATORIO       | Il nome file non è valido. Assicurarsi che il nome del file non sia più lungo di otto caratteri, seguiti da un punto e da un'estensione.                                  |
| FLAG MCIERR \_ \_ NON \_ COMPATIBILI   | I parametri specificati non possono essere usati insieme.                                                                                                           |
| MCIERR \_ GET \_ CD                  | Il file richiesto o il dispositivo MCI non è stato trovato. Provare a modificare le directory o a riavviare il sistema.                                                         |
| MCIERR \_ HARDWARE                 | Il dispositivo specificato presenta un problema. Verificare che il dispositivo funzioni correttamente o contattare il produttore del dispositivo.                                     |
| MCIERR \_ ILLEGAL \_ FOR \_ AUTO \_ OPEN | McI non eseguirà il comando specificato in un dispositivo aperto automaticamente. Attendere che il dispositivo sia chiuso, quindi provare a eseguire il comando.             |
| MCIERR \_ INTERNAL                 | Si è verificato un problema durante l'inizializzazione di MCI. Provare a riavviare il Windows operativo.                                                                        |
| ID DISPOSITIVO MCIERR \_ \_ NON \_ VALIDO      | ID dispositivo non valido. Usare l'ID assegnato al dispositivo quando il dispositivo è stato aperto.                                                                               |
| MCIERR \_ INVALID DEVICE NAME (NOME DISPOSITIVO NON VALIDO \_ \_ MCIERR)    | Il dispositivo specificato non è aperto né riconosciuto da MCI.                                                                                                     |
| FILE MCIERR \_ NON \_ VALIDO            | Il file specificato non può essere riprodotto nel dispositivo MCI specificato. Il file potrebbe essere danneggiato o usare un formato di file non corretto.                               |
| PARAMETRO MANCANTE DI \_ MCIERR \_       | Il comando specificato richiede un parametro, che è necessario fornire.                                                                                          |
| MCIERR \_ MULTIPLE                 | Si sono verificati errori in più dispositivi. Specificare separatamente ogni comando e dispositivo per identificare i dispositivi che causano gli errori.                             |
| MCIERR \_ DEVE \_ USARE \_ SHAREABLE     | Il driver di dispositivo è già in uso. È necessario specificare il parametro "sharable" con ogni comando open per condividere il dispositivo.                                  |
| MCIERR \_ NESSUN \_ ELEMENTO \_ CONSENTITO     | Il dispositivo specificato non usa un nome file.                                                                                                               |
| MCIERR \_ NO \_ INTEGER              | Il parametro per questo comando MCI deve essere un valore intero.                                                                                                |
| MCIERR \_ NO \_ WINDOW               | Non è presente alcuna finestra di visualizzazione.                                                                                                                                 |
| FUNZIONE MCIERR \_ \_ NONAPPLICABLE  | La sequenza di comandi MCI specificata non può essere eseguita nell'ordine specificato. Correggere la sequenza di comandi. quindi riprovare.                                   |
| BLOCCO DI PARAMETRI NULL MCIERR \_ \_ \_   | È stato passato un blocco di parametri Null (struttura) a MCI.                                                                                                       |
| MEMORIA INSUFFICIENTE PER \_ MCIERR \_ \_          | La memoria del sistema non è sufficiente per questa attività. Chiudere una o più applicazioni per aumentare la memoria disponibile, quindi provare a eseguire di nuovo l'attività. |
| MCIERR \_ OUTOFRANGE               | Il valore del parametro specificato non è compreso nell'intervallo per il comando MCI specificato.                                                                                |
| MCIERR \_ SET \_ CD                  | Il file o il dispositivo MCI specificato non è accessibile perché l'applicazione non può modificare le directory.                                                         |
| MCIERR \_ SET \_ DRIVE               | Il file o il dispositivo MCI specificato non è accessibile perché l'applicazione non può modificare le unità.                                                              |
| RISORSA MCIERR \_ SENZA \_ NOME        | Non è possibile archiviare un file senza nome. Specificare un nome file.                                                                                                       |
| COMANDO MCIERR \_ NON \_ RICONOSCIUTO    | Il driver non è in grado di riconoscere il comando specificato.                                                                                                          |
| FUNZIONE MCIERR \_ NON \_ SUPPORTATA    | Il driver di dispositivo MCI utilizzato dal sistema non supporta il comando specificato.                                                                           |



 

 

 