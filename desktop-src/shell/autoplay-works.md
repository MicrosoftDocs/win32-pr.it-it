---
description: La creazione di un'applicazione abilitata per l'esecuzione automatica è una procedura semplice. Questo argomento usa CD-ROM come esempio (è stato il primo supporto a implementare questa tecnologia), ma attualmente sono disponibili molti tipi di supporti diversi che possono usarla.
title: Creazione di unAutoRun-Enabled app
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f3a3c265f71b0bdf66d7825e65eb69ab975bfc6bffa5c9a8674ed5a0fb8feb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224933"
---
# <a name="creating-an-autorun-enabled-application"></a>Creazione di unAutoRun-Enabled app

La creazione di un'applicazione abilitata per l'esecuzione automatica è una procedura semplice. Questo argomento usa CD-ROM come esempio (è stato il primo supporto a implementare questa tecnologia), ma attualmente sono disponibili molti tipi di supporti diversi che possono usarla.

Per abilitare l'esecuzione automatica nell'applicazione, è sufficiente includere due file essenziali:

-   Un file Autorun.inf
-   Un'applicazione di avvio

Quando un utente inserisce un disco in un'unità CD-ROM in un computer compatibile con l'esecuzione automatica, il sistema verifica immediatamente se il disco ha un personal computer file system. In caso contrario, il sistema cerca un file denominato [Autorun.inf](#creating-an-autoruninf-file). Questo file specifica un'applicazione di installazione che verrà eseguita, insieme a un'ampia gamma di impostazioni facoltative. L'applicazione di avvio in genere installa, disinstalla, configura ed esegue l'applicazione.

-   [Creazione di un file Autorun.inf](#creating-an-autoruninf-file)
-   [Sezione \[ \] DeviceInstall](#the-deviceinstall-section)
-   [Argomenti correlati](#related-topics)

## <a name="creating-an-autoruninf-file"></a>Creazione di un file Autorun.inf

Autorun.inf è un file di testo che si trova nella directory radice del CD-ROM che contiene l'applicazione. La funzione principale è fornire al sistema il nome e il percorso del programma di avvio dell'applicazione che verrà eseguito quando viene inserito il disco.

> [!Note]  
> I file Autorun.inf non sono supportati in Windows XP per le unità che restituiscono DRIVE \_ REMOVABLE da [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).

 

Il file Autorun.inf può contenere anche informazioni facoltative, tra cui:

-   Nome di un file contenente un'icona che rappresenta l'unità CD-ROM dell'applicazione. Questa icona verrà visualizzata da Windows Explorer al posto dell'icona dell'unità standard.
-   Comandi aggiuntivi per il menu di scelta rapida visualizzato quando l'utente fa clic con il pulsante destro del mouse sull'icona CD-ROM. È anche possibile specificare il comando predefinito che viene eseguito quando l'utente fa doppio clic sull'icona.

I file Autorun.inf sono simili .ini file. Sono costituite da una o più sezioni, ognuna con un nome racchiuso tra parentesi quadre. Ogni sezione contiene una serie di comandi che verranno eseguiti da Shell quando viene inserito il disco. Esistono due sezioni attualmente definite per i file Autorun.inf.

-   La **\[ sezione \] esecuzione automatica** contiene i comandi di esecuzione automatica predefiniti. Tutti i file Autorun.inf devono avere una **\[ sezione di esecuzione \]** automatica.
-   È possibile **\[ includere \] una sezione facoltativa autorun.alpha** per i sistemi in esecuzione in computer basati su RISC. Quando un disco viene inserito in un'unità CD-ROM in un sistema basato su RISC, Shell eseguirà i comandi in questa sezione anziché quelli nella **\[ sezione esecuzione \]** automatica.

> [!Note]  
> Shell verifica prima di tutto la presenza di una sezione specifica dell'architettura. Se non ne trova una, usa le informazioni nella **\[ sezione esecuzione \]** automatica. Quando Shell trova una sezione, ignora tutte le altre, quindi ogni sezione deve essere autonoma.

 

Ogni sezione contiene una serie di comandi che determinano come viene eseguita l'operazione di esecuzione automatica. Sono disponibili cinque comandi.



| Comando                         | Descrizione                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [defaulticon](autorun-cmds.md) | Specifica l'icona predefinita per l'applicazione.                                        |
| [icona](autorun-cmds.md)        | Specifica il percorso e il nome file di un'icona specifica dell'applicazione per l'unità CD-ROM. |
| [open](autorun-cmds.md)        | Specifica il percorso e il nome file dell'applicazione di avvio.                           |
| [useautorun](autorun-cmds.md)  | Specifica che le funzionalità di Riproduzione automatica V2 devono essere usate, se supportate.                       |
| [Guscio](autorun-cmds.md)       | Definisce il comando predefinito nel menu di scelta rapida del CD-ROM.                             |
| [Verbo \_ shell](autorun-cmds.md) | Aggiunge comandi al menu di scelta rapida del CD-ROM.                                           |



 

Di seguito è riportato un esempio di un semplice file Autorun.inf. Specifica l'Filename.exe come applicazione di avvio. La seconda icona in Filename.exe rappresenta l'unità CD-ROM anziché l'icona dell'unità standard.


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



Questo esempio autorun.inf esegue applicazioni di avvio diverse a seconda del tipo di computer.


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>Sezione \[ \] DeviceInstall

È possibile usare la **\[ sezione DeviceInstall \]** su qualsiasi supporto rimovibile. È supportato solo in Windows XP. Si usa **DriverPath per** specificare un percorso di directory in cui Windows XP cerca i file del driver, impedendo una lunga ricerca nell'intero contenuto.

Usare la sezione **\[ DeviceInstall con \]** un'installazione del driver per specificare le directory in cui Windows XP deve cercare i file del driver nei supporti. In Windows XP, l'intero supporto non viene più cercato per impostazione predefinita, pertanto **\[ deviceInstall \]** deve specificare i percorsi di ricerca. Di seguito sono riportati gli unici supporti rimovibili che Windows XP esegue la ricerca completa senza una sezione **\[ DeviceInstall \]** in un file Autorun.inf.

-   Dischi floppy trovati nelle unità A o B.
-   Supporti CD/DVD di dimensioni inferiori a 1 gigabyte (GB).

Tutti gli altri supporti devono includere **\[ una sezione DeviceInstall \]** per Windows XP per rilevare eventuali driver archiviati in tale supporto.

> [!Note]  
> Come per la **\[ sezione Esecuzione automatica, \]** la sezione **\[ DeviceInstall \]** può essere specifica dell'architettura.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come implementare applicazioni di avvio con esecuzione automatica](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[Scrittura di un'applicazione di installazione del dispositivo](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
