---
title: Informazioni sull'input non elaborato
description: Questo argomento illustra l'input dell'utente da dispositivi come i joystick, i touch screen e i microfoni.
ms.assetid: 013ed309-f667-47ed-ade0-5e7ca5a0997a
keywords:
- input utente, input non elaborato
- acquisizione di input utente, input non elaborato
- input non elaborato
- registrazione di input non elaborato
- lettura di input non elaborato
- input non elaborato del joystick
- input non elaborato del touch screen
- input non elaborato del microfono
- Human Interface Device (HID)
- HID (dispositivo human interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fed3772406cc85df57b95c4b11dbcfeaf60804e94da5602059ec790e87e0439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884328"
---
# <a name="about-raw-input"></a>Informazioni sull'input non elaborato

Accanto alla tastiera e al mouse tradizionali sono presenti molti dispositivi di input utente. Ad esempio, l'input dell'utente può derivare da un joystick, un touch screen, un microfono o altri dispositivi che consentono una grande flessibilità nell'input dell'utente. Questi dispositivi sono noti collettivamente come HID (Human Interface Devices). L'API di input non elaborato offre un modo stabile e affidabile per le applicazioni di accettare input non elaborato da qualsiasi HID, inclusi tastiera e mouse.

Questa sezione contiene gli argomenti seguenti:

-   [Modello di input non elaborato](#raw-input-model)
-   [Registrazione per l'input non elaborato](#registration-for-raw-input)
-   [Lettura dell'input non elaborato](#reading-raw-input)

## <a name="raw-input-model"></a>Modello di input non elaborato

In precedenza, la tastiera e il mouse in genere hanno generato dati di input. Il sistema ha interpretato i dati provenienti da questi dispositivi in modo da eliminare i dettagli specifici del dispositivo delle informazioni non elaborate. Ad esempio, la tastiera genera il codice di analisi specifico del dispositivo, ma il sistema fornisce un'applicazione con il codice del tasto virtuale. Oltre a nascondere i dettagli dell'input non elaborato, gestione finestre non supporta tutti i nuovi HID. Per ottenere l'input dagli HID non supportati, un'applicazione doveva eseguire molte operazioni: aprire il dispositivo, gestire la modalità condivisa, leggere periodicamente il dispositivo o configurare la porta di completamento I/O e così via. Il modello di input non elaborato e le API associate sono stati sviluppati per consentire l'accesso semplice all'input non elaborato da tutti i dispositivi di input, inclusi tastiera e mouse.

Il modello di input non elaborato è diverso dal modello di input Windows originale per la tastiera e il mouse. Nel modello di input originale un'applicazione riceve input indipendente dal dispositivo sotto forma di messaggi inviati o inviati alle finestre, ad esempio [**WM \_ CHAR,**](wm-char.md) [**WM \_ MOUSEMOVE**](wm-mousemove.md)e [**WM \_ APPCOMMAND.**](wm-appcommand.md) Al contrario, per l'input non elaborato un'applicazione deve registrare i dispositivi da cui vuole ottenere i dati. Inoltre, l'applicazione ottiene l'input non elaborato tramite il [**messaggio WM \_ INPUT.**](wm-input.md)

Il modello di input non elaborato presenta diversi vantaggi:

-   Un'applicazione non deve rilevare o aprire il dispositivo di input.
-   Un'applicazione ottiene i dati direttamente dal dispositivo ed elabora i dati in base alle proprie esigenze.
-   Un'applicazione può distinguere l'origine dell'input anche se è dello stesso tipo di dispositivo. Ad esempio, due dispositivi mouse.
-   Un'applicazione gestisce il traffico dati specificando i dati da una raccolta di dispositivi o solo da tipi di dispositivo specifici.
-   I dispositivi HID possono essere usati non appena diventano disponibili nel marketplace, senza attendere che nuovi tipi di messaggio o un sistema operativo aggiornato abbia nuovi comandi in [**WM \_ APPCOMMAND.**](wm-appcommand.md)

Si noti [**che WM \_ APPCOMMAND**](wm-appcommand.md) fornisce per alcuni dispositivi HID. **TUTTAVIA, WM \_ APPCOMMAND è** un evento di input indipendente dal dispositivo di livello superiore, mentre [**WM \_ INPUT**](wm-input.md) invia dati non elaborati di basso livello specifici di un dispositivo.

## <a name="registration-for-raw-input"></a>Registrazione per l'input non elaborato

Per impostazione predefinita, nessuna applicazione riceve input non elaborato. Per ricevere input non elaborato da un dispositivo, un'applicazione deve registrare il dispositivo.

Per registrare i dispositivi, un'applicazione crea innanzitutto una matrice di strutture [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice) che specificano la raccolta di primo livello [per](/windows-hardware/drivers/hid/top-level-collections) i dispositivi che desidera. Il TLC è definito da una [pagina di](/windows-hardware/drivers/hid/hid-usages#usage-page) utilizzo (la classe del dispositivo) e da un [ID](/windows-hardware/drivers/hid/hid-usages#usage-id) di utilizzo (il dispositivo all'interno della classe). Ad esempio, per ottenere il TLC della tastiera, impostare UsagePage = 0x01 e UsageID = 0x06. L'applicazione [**chiama RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) per registrare i dispositivi.

Si noti che un'applicazione può registrare un dispositivo che non è attualmente collegato al sistema. Quando questo dispositivo è collegato, il Windows Manager invierà automaticamente l'input non elaborato all'applicazione. Per ottenere l'elenco dei dispositivi di input non elaborati nel sistema, un'applicazione chiama [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist). Usando *hDevice da* questa chiamata, un'applicazione chiama [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) per ottenere le informazioni sul dispositivo.

Tramite il **membro dwFlags** di [**RAWINPUTDEVICE,**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)un'applicazione può selezionare i dispositivi da ascoltare e anche quelli che vuole ignorare. Ad esempio, un'applicazione può richiedere l'input da tutti i dispositivi di telefonia, ad eccezione dei computer di risposta. Per il codice di esempio, [vedere Registrazione per l'input non elaborato.](using-raw-input.md)

Si noti che anche il mouse e la tastiera sono HID, in modo che i dati provenienti da essi possano passare sia dal messaggio [**HID WM \_ INPUT**](wm-input.md) che dai messaggi tradizionali. Un'applicazione può selezionare uno dei metodi selezionando correttamente i flag in [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice).

Per ottenere lo stato di registrazione di un'applicazione, chiamare [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) in qualsiasi momento.

## <a name="reading-raw-input"></a>Lettura dell'input non elaborato

Un'applicazione riceve input non elaborato da qualsiasi hid [la](/windows-hardware/drivers/hid/top-level-collections) cui raccolta di primo livello corrisponde a un TLC dalla registrazione. Quando un'applicazione riceve input non elaborato, la coda di messaggi riceve un messaggio [**WM \_ INPUT**](wm-input.md) e il flag di stato della coda **QS \_ RAWINPUT** è impostato (**anche QS \_ INPUT** include questo flag). Un'applicazione può ricevere dati quando sono in primo piano e quando sono in background.

Esistono due modi per leggere i dati non elaborati: il metodo senza buffer (o standard) e il metodo memorizzato nel buffer. Il metodo senza buffer ottiene i dati non elaborati una [**struttura RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) alla volta ed è adeguato per molti HID. In questo caso, [**l'applicazione chiama GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) per ottenere il [**messaggio WM \_ INPUT.**](wm-input.md) L'applicazione chiama quindi [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata) usando **l'handle RAWINPUT** contenuto in **WM \_ INPUT**. Per un esempio, vedere Doing a Standard Read of Raw Input (Eseguire [una lettura standard dell'input non elaborato).](using-raw-input.md)

Al contrario, il metodo memorizzato nel buffer ottiene una matrice di [**strutture RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) alla volta. Questo viene fornito per i dispositivi che possono produrre grandi quantità di input non elaborato. In questo metodo l'applicazione chiama [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) per ottenere una matrice **di strutture RAWINPUT.** Si noti che la macro [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock) viene usata per attraversare una matrice di **strutture RAWINPUT.** Per un esempio, vedere Doing a Buffered Read of Raw Input (Eseguire una lettura [memorizzata nel buffer dell'input non elaborato).](using-raw-input.md)

Per interpretare l'input non elaborato, sono necessarie informazioni dettagliate sugli HID. Un'applicazione ottiene le informazioni sul dispositivo chiamando [**GetRawInputDeviceInfo con**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) l'handle del dispositivo. Questo handle può derivare da [**WM \_ INPUT**](wm-input.md) o dal membro **hDevice** di [**RAWINPUTHEADER.**](/windows/win32/api/winuser/ns-winuser-rawinputheader)