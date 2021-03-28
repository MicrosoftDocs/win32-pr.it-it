---
description: La creazione di un'applicazione abilitata per l'AutoRun è una procedura semplice. In questo argomento viene usato il CD-ROM come esempio (il primo supporto per implementare questa tecnologia), ma oggi sono disponibili molti tipi di supporti diversi che possono usarlo.
title: Creazione di un'applicazione AutoRun-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128467"
---
# <a name="creating-an-autorun-enabled-application"></a>Creazione di un'applicazione AutoRun-Enabled

La creazione di un'applicazione abilitata per l'AutoRun è una procedura semplice. In questo argomento viene usato il CD-ROM come esempio (il primo supporto per implementare questa tecnologia), ma oggi sono disponibili molti tipi di supporti diversi che possono usarlo.

Per abilitare l'esecuzione automatica nell'applicazione, è sufficiente includere due file essenziali:

-   Un file Autorun. inf
-   Un'applicazione di avvio

Quando un utente inserisce un disco in un'unità CD-ROM in un computer compatibile con AutoRun, il sistema verifica immediatamente se il disco dispone di un personal computer file system. In caso contrario, il sistema cerca un file denominato [Autorun. inf](#creating-an-autoruninf-file). Questo file specifica un'applicazione di installazione che verrà eseguita insieme a un'ampia gamma di impostazioni facoltative. L'applicazione di avvio in genere installa, Disinstalla, configura ed eventualmente esegue l'applicazione.

-   [Creazione di un file Autorun. inf](#creating-an-autoruninf-file)
-   [\[Sezione DeviceInstall \]](#the-deviceinstall-section)
-   [Argomenti correlati](#related-topics)

## <a name="creating-an-autoruninf-file"></a>Creazione di un file Autorun. inf

Autorun. inf è un file di testo che si trova nella directory radice del CD-ROM che contiene l'applicazione. La funzione principale è fornire al sistema il nome e il percorso del programma di avvio dell'applicazione che verrà eseguito quando viene inserito il disco.

> [!Note]  
> I file Autorun. inf non sono supportati in Windows XP per le unità che restituiscono l'unità \_ rimovibile da [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).

 

Il file Autorun. inf può inoltre contenere informazioni facoltative, tra cui:

-   Nome di un file che contiene un'icona che rappresenterà l'unità CD-ROM dell'applicazione. Questa icona verrà visualizzata da Esplora risorse al posto dell'icona dell'unità standard.
-   Comandi aggiuntivi per il menu di scelta rapida visualizzato quando l'utente fa clic con il pulsante destro del mouse sull'icona del CD-ROM. È anche possibile specificare il comando predefinito che viene eseguito quando l'utente fa doppio clic sull'icona.

I file Autorun. inf sono simili ai file ini. Sono costituiti da una o più sezioni, ciascuna con un nome racchiuso tra parentesi quadre. Ogni sezione contiene una serie di comandi che verranno eseguiti dalla shell quando viene inserito il disco. Sono presenti due sezioni attualmente definite per i file Autorun. inf.

-   La sezione **\[ Autorun \]** contiene i comandi di autorun predefiniti. Tutti i file Autorun. inf devono avere una sezione di **\[ Autorun \]** .
-   È possibile includere una sezione di **\[ Autorun. Alpha \]** facoltativa per i sistemi in esecuzione su computer basati su RISC. Quando un disco viene inserito in un'unità CD-ROM in un sistema basato su RISC, la shell eseguirà i comandi in questa sezione anziché quelli presenti nella sezione **\[ Autorun \]** .

> [!Note]  
> La shell verifica innanzitutto la presenza di una sezione specifica dell'architettura. Se non ne viene trovato uno, USA le informazioni contenute nella sezione **\[ Autorun \]** . Quando la shell trova una sezione, ignora tutte le altre, quindi ogni sezione deve essere indipendente.

 

Ogni sezione contiene una serie di comandi che determinano il modo in cui viene eseguita l'operazione di avvio automatico. Sono disponibili cinque comandi.



| Comando                         | Descrizione                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [DefaultIcon](autorun-cmds.md) | Specifica l'icona predefinita per l'applicazione.                                        |
| [icona](autorun-cmds.md)        | Specifica il percorso e il nome file di un'icona specifica dell'applicazione per l'unità CD-ROM. |
| [open](autorun-cmds.md)        | Specifica il percorso e il nome file dell'applicazione di avvio.                           |
| [useautorun](autorun-cmds.md)  | Specifica che le funzionalità AutoPlay V2 devono essere utilizzate se supportate.                       |
| [Shell](autorun-cmds.md)       | Definisce il comando predefinito nel menu di scelta rapida del CD-ROM.                             |
| [Verbo della shell \_](autorun-cmds.md) | Aggiunge comandi al menu di scelta rapida del CD-ROM.                                           |



 

Di seguito è riportato un esempio di un semplice file Autorun. inf. Specifica Filename.exe come applicazione di avvio. La seconda icona in Filename.exe rappresenterà l'unità CD-ROM anziché l'icona dell'unità standard.


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



Questo esempio di autorun. inf esegue diverse applicazioni di avvio a seconda del tipo di computer.


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>\[Sezione DeviceInstall \]

È possibile usare la sezione **\[ DeviceInstall \]** su qualsiasi supporto rimovibile. È supportato solo in Windows XP. Usare **DriverPath** per specificare un percorso di directory in cui Windows XP cerca i file del driver, impedendo una lunga ricerca nell'intero contenuto.

Utilizzare la sezione **\[ DeviceInstall \]** con l'installazione di un driver per specificare le directory in cui Windows XP deve cercare i file di driver nel supporto. In Windows XP, per impostazione predefinita non viene più eseguita la ricerca di interi supporti, pertanto è necessario che **\[ DeviceInstall \]** specifichi i percorsi di ricerca. Di seguito sono riportati gli unici supporti rimovibili che Windows XP cerca completamente senza una sezione **\[ DeviceInstall \]** in un file Autorun. inf.

-   Dischi floppy presenti nelle unità A o B.
-   Supporti CD/DVD di dimensioni inferiori a 1 gigabyte (GB).

Tutti gli altri supporti devono includere una sezione **\[ DeviceInstall \]** per Windows XP per rilevare tutti i driver archiviati in tale supporto.

> [!Note]  
> Come per la sezione **\[ Autorun \]** , la sezione **\[ DeviceInstall \]** può essere specifica dell'architettura.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come implementare le applicazioni di avvio autorun](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[Scrittura di un'applicazione di installazione del dispositivo](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
