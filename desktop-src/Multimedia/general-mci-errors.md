---
title: Errori generali di MCI
description: Errori generali di MCI
ms.assetid: be9c4a2b-44bc-410c-be74-ba55bb4e785b
keywords:
- MCIERR valori restituiti, errori generali
- riferimenti multimediali, errori di MCI
- informazioni di riferimento per gli errori di MCI
- Interfaccia di controllo multimediale (MCI), errori generali
- MCI (interfaccia di controllo multimediale), errori generali
- riferimento per MCI, errori generali
- Riferimento a MCI, errori generali
- Interfaccia di controllo multimediale (MCI), errori
- MCI (interfaccia di controllo multimediale), errori
- informazioni di riferimento per MCI, errori
- Riferimento a MCI, errori
- mciSendCommand (funzione)
- mciSendString (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44538937be73c2ccfb1d30de1f1a1c729cc05095
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337014"
---
# <a name="general-mci-errors"></a>Errori generali di MCI

I valori di errore seguenti possono essere restituiti dalla funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) o [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :



| Valore                            | Significato                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_formato MCIERR \_ tempo non valido \_        | Il valore specificato per il formato dell'ora non è valido.                                                                                                         |
| MCIERR \_ non è in grado di \_ caricare il \_ driver     | Il driver di dispositivo specificato non viene caricato correttamente.                                                                                                         |
| MCIERR \_ non può \_ utilizzare \_ All         | Il nome del dispositivo "All" non è consentito per questo comando.                                                                                                      |
| \_CREATEWINDOW MCIERR             | Impossibile creare o utilizzare la finestra.                                                                                                                             |
| \_lunghezza del dispositivo MCIERR \_           | Il nome del dispositivo o del driver è troppo lungo. Specificare un nome di dispositivo o di driver inferiore a 79 caratteri.                                                     |
| \_dispositivo MCIERR \_ bloccato           | Il dispositivo è in fase di chiusura. Attendere alcuni secondi, quindi riprovare.                                                                                         |
| il \_ dispositivo MCIERR \_ non è \_ installato   | Il dispositivo specificato non è installato nel sistema. Usare l'opzione drivers nel pannello di controllo per installare il dispositivo.                                   |
| \_dispositivo MCIERR \_ non \_ pronto       | Il driver di dispositivo non è pronto.                                                                                                                             |
| \_dispositivo MCIERR \_ aperto             | Il nome del dispositivo è già usato come alias da questa applicazione. Usare un alias univoco.                                                                        |
| \_ \_ lunghezza ORD dispositivo \_ MCIERR      | Il nome del dispositivo o del driver è troppo lungo. Specificare un nome di dispositivo o di driver inferiore a 79 caratteri.                                                     |
| il \_ tipo di dispositivo MCIERR è \_ \_ obbligatorio   | Il dispositivo specificato non è stato trovato nel sistema. Verificare che il dispositivo sia installato e che il nome del dispositivo sia stato digitato correttamente.                            |
| \_driver MCIERR                   | Il driver di dispositivo presenta un problema. Rivolgersi al produttore del dispositivo per ottenere un nuovo driver.                                                      |
| \_driver MCIERR \_ interno         | Il driver di dispositivo presenta un problema. Rivolgersi al produttore del dispositivo per ottenere un nuovo driver.                                                      |
| \_alias duplicato MCIERR \_         | L'alias specificato è già utilizzato nell'applicazione. Usare un alias univoco.                                                                                |
| \_estensione MCIERR \_ non \_ trovata    | All'estensione specificata non è associato alcun tipo di dispositivo. Specificare un tipo di dispositivo.                                                                       |
| MCIERR \_ \_ caratteri aggiuntivi        | È necessario racchiudere una stringa tra virgolette; i caratteri che seguono le virgolette di chiusura non sono validi.                                              |
| il \_ file MCIERR non è stato \_ \_ trovato         | Il file richiesto non è stato trovato. Verificare che il percorso e il nome del file siano corretti.                                                                             |
| il \_ file MCIERR non è stato \_ \_ salvato         | Il file non è stato salvato. Verificare che il sistema disponga di spazio su disco sufficiente o che la connessione di rete sia intatta.                                                |
| \_lettura file \_ MCIERR               | Lettura dal file non riuscita. Verificare che il file sia presente nel sistema o che il sistema disponga di una connessione di rete intatta.                             |
| \_scrittura file \_ MCIERR              | Impossibile scrivere nel file. Verificare che il sistema disponga di spazio su disco sufficiente o che la connessione di rete sia intatta.                                            |
| MCIERR \_ nomefile \_ obbligatorio       | Il nome file non è valido. Verificare che il nome del file non sia più lungo di otto caratteri, seguito da un punto e da un'estensione.                                  |
| \_flag MCIERR \_ non \_ compatibili   | I parametri specificati non possono essere utilizzati insieme.                                                                                                           |
| MCIERR \_ ottenere \_ CD                  | Il file richiesto o il dispositivo MCI non è stato trovato. Provare a modificare le directory o a riavviare il sistema.                                                         |
| \_hardware MCIERR                 | Il dispositivo specificato presenta un problema. Verificare che il dispositivo funzioni correttamente o contattare il produttore del dispositivo.                                     |
| MCIERR non \_ valido \_ per l' \_ \_ apertura automatica | MCI non eseguirà il comando specificato su un dispositivo aperto automaticamente. Attendere fino alla chiusura del dispositivo, quindi provare a eseguire il comando.             |
| MCIERR \_ interno                 | Si è verificato un problema durante l'inizializzazione di MCI. Provare a riavviare il sistema operativo Windows.                                                                        |
| \_ID dispositivo non valido MCIERR \_ \_      | ID dispositivo non valido. Usare l'ID assegnato al dispositivo quando il dispositivo è stato aperto.                                                                               |
| MCIERR \_ \_ nome dispositivo non valido \_    | Il dispositivo specificato non è aperto né riconosciuto da MCI.                                                                                                     |
| \_file MCIERR non valido \_            | Impossibile riprodurre il file specificato sul dispositivo MCI specificato. Il file potrebbe essere danneggiato o potrebbe utilizzare un formato di file non corretto.                               |
| \_parametro MCIERR mancante \_       | Il comando specificato richiede un parametro, che è necessario fornire.                                                                                          |
| MCIERR \_ multiplo                 | Si sono verificati errori in più di un dispositivo. Specificare separatamente ogni comando e dispositivo per identificare i dispositivi che causano gli errori.                             |
| MCIERR \_ deve \_ usare \_ condivisibile     | Il driver di dispositivo è già in uso. È necessario specificare il parametro "condivisibile" con ogni comando aperto per condividere il dispositivo.                                  |
| MCIERR \_ nessun \_ elemento \_ consentito     | Il dispositivo specificato non usa un nome file.                                                                                                               |
| MCIERR \_ senza \_ Integer              | Il parametro per questo comando MCI deve essere un valore integer.                                                                                                |
| MCIERR \_ Nessuna \_ finestra               | Nessuna finestra di visualizzazione.                                                                                                                                 |
| MCIERR \_ funzione non applicabile \_  | La sequenza di comandi MCI specificata non può essere eseguita nell'ordine specificato. Correggere la sequenza di comandi. quindi, riprovare.                                   |
| \_blocco di \_ parametri \_ null MCIERR   | Un blocco di parametri null (struttura) è stato passato a MCI.                                                                                                       |
| \_ \_ \_ memoria insufficiente MCIERR          | Memoria del sistema insufficiente per questa attività. Uscire da una o più applicazioni per aumentare la memoria disponibile, quindi provare di nuovo a eseguire l'attività. |
| \_OUTOFRANGE MCIERR               | Il valore del parametro specificato non è compreso nell'intervallo per il comando MCI specificato.                                                                                |
| CD di MCIERR \_ set \_                  | Il file o il dispositivo MCI specificato non è accessibile perché l'applicazione non può modificare le directory.                                                         |
| \_unità set \_ MCIERR               | Il file o il dispositivo MCI specificato non è accessibile perché l'applicazione non può modificare le unità.                                                              |
| MCIERR \_ risorsa senza nome \_        | Non è possibile archiviare un file senza nome. Specificare un nome file.                                                                                                       |
| comando MCIERR non \_ riconosciuto \_    | Il driver non è in grado di riconoscere il comando specificato.                                                                                                          |
| funzione MCIERR non \_ supportata \_    | Il driver di dispositivo MCI utilizzato dal sistema non supporta il comando specificato.                                                                           |



 

 

 