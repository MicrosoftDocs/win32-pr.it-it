---
title: Informazioni sull'input non elaborato
description: Questo argomento illustra l'input dell'utente da dispositivi quali joystick, touch screen e microfoni.
ms.assetid: 013ed309-f667-47ed-ade0-5e7ca5a0997a
keywords:
- input utente, input non elaborato
- acquisizione dell'input dell'utente, input non elaborato
- input non elaborato
- registrazione dell'input non elaborato
- lettura dell'input non elaborato
- input non elaborato del joystick
- input non elaborato touch screen
- input raw microfono
- Human Interface Device (HID)
- HID (dispositivo interfaccia umana)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3535e5601ec63a254c76060611999a1a2f08aeb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046737"
---
# <a name="about-raw-input"></a>Informazioni sull'input non elaborato

Accanto alla tastiera e al mouse tradizionali sono presenti molti dispositivi di input utente. Ad esempio, l'input dell'utente può provenire da un joystick, un touchscreen, un microfono o altri dispositivi che consentono una grande flessibilità nell'input dell'utente. Questi dispositivi sono collettivamente noti come Human Interface Device (HIDs). L'API di input non elaborato fornisce un modo stabile e affidabile per le applicazioni di accettare l'input non elaborato da qualsiasi HID, inclusa la tastiera e il mouse.

Questa sezione contiene gli argomenti seguenti:

-   [Modello di input non elaborato](#raw-input-model)
-   [Registrazione per l'input non elaborato](#registration-for-raw-input)
-   [Lettura dell'input non elaborato](#reading-raw-input)

## <a name="raw-input-model"></a>Modello di input non elaborato

In precedenza, la tastiera e il mouse generavano in genere dati di input. Il sistema ha interpretato i dati provenienti da questi dispositivi in modo da eliminare i dettagli specifici del dispositivo delle informazioni non elaborate. Ad esempio, la tastiera genera il codice di analisi specifico del dispositivo, ma il sistema fornisce un'applicazione con il codice della chiave virtuale. Oltre a nascondere i dettagli dell'input non elaborato, gestione finestre non supportava tutti i nuovi HIDs. Per ottenere l'input dalla HIDs non supportata, un'applicazione deve eseguire molte operazioni: aprire il dispositivo, gestire la modalità condivisa, leggere periodicamente il dispositivo o configurare la porta di completamento I/O e così via. Il modello di input non elaborato e le API associate sono stati sviluppati per consentire l'accesso semplice a un input non elaborato da tutti i dispositivi di input, tra cui la tastiera e il mouse.

Il modello di input non elaborato è diverso dal modello di input Windows originale per la tastiera e il mouse. Nel modello di input originale, un'applicazione riceve un input indipendente dal dispositivo sotto forma di messaggi inviati o inviati alle finestre, ad esempio [**WM \_ char**](wm-char.md), [**WM \_ MOUSEMOVE**](wm-mousemove.md)e [**WM \_ APPCOMMAND**](wm-appcommand.md). Per l'input non elaborato, invece, un'applicazione deve registrare i dispositivi da cui desidera ottenere i dati. Inoltre, l'applicazione ottiene l'input non elaborato tramite il messaggio di [**\_ input WM**](wm-input.md) .

Il modello di input non elaborato presenta diversi vantaggi:

-   Non è necessario che un'applicazione rilevi o apra il dispositivo di input.
-   Un'applicazione ottiene i dati direttamente dal dispositivo ed elabora i dati per le proprie esigenze.
-   Un'applicazione può distinguere l'origine dell'input anche se è dello stesso tipo di dispositivo. Ad esempio, due dispositivi mouse.
-   Un'applicazione gestisce il traffico dati specificando i dati da una raccolta di dispositivi o solo specifici tipi di dispositivi.
-   I dispositivi HID possono essere usati quando diventano disponibili nel Marketplace, senza attendere che nuovi tipi di messaggio o un sistema operativo aggiornato dispongano di nuovi comandi in [**WM \_ APPCOMMAND**](wm-appcommand.md).

Si noti che [**WM \_ APPCOMMAND**](wm-appcommand.md) fornisce alcuni dispositivi HID. Tuttavia, **WM \_ APPCOMMAND** è un evento di input di livello superiore indipendente dal dispositivo, mentre l' [**\_ input WM**](wm-input.md) invia dati non elaborati di basso livello specifici di un dispositivo.

## <a name="registration-for-raw-input"></a>Registrazione per l'input non elaborato

Per impostazione predefinita, nessuna applicazione riceve input non elaborato. Per ricevere input non elaborato da un dispositivo, un'applicazione deve registrare il dispositivo.

Per registrare i dispositivi, un'applicazione crea prima di tutto una matrice di strutture [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice) che specificano la [raccolta di livello superiore](/windows-hardware/drivers/hid/top-level-collections) (TLC) per i dispositivi desiderati. Il TLC è definito da una [pagina di utilizzo](/windows-hardware/drivers/hid/hid-usages#usage-page) (la classe del dispositivo) e da un [ID di utilizzo](/windows-hardware/drivers/hid/hid-usages#usage-id) (il dispositivo all'interno della classe). Ad esempio, per ottenere la tastiera di TLC, impostare UsagePage = 0x01 e UsageID = 0x06. L'applicazione chiama [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) per registrare i dispositivi.

Si noti che un'applicazione può registrare un dispositivo che non è attualmente collegato al sistema. Quando il dispositivo è collegato, Windows Manager invierà automaticamente l'input non elaborato all'applicazione. Per ottenere l'elenco di dispositivi di input non elaborati nel sistema, un'applicazione chiama [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist). Utilizzando *hDevice* da questa chiamata, un'applicazione chiama [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) per ottenere le informazioni sul dispositivo.

Tramite il membro **dwFlags** di [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice), un'applicazione può selezionare i dispositivi da ascoltare e anche quelli che vogliono ignorare. Ad esempio, un'applicazione può richiedere l'input da tutti i dispositivi di telefonia ad eccezione dei computer che rispondono. Per il codice di esempio, vedere [la pagina relativa alla registrazione per l'input non elaborato](using-raw-input.md).

Si noti che anche il mouse e la tastiera sono HIDs, quindi i dati provenienti da essi possono essere inclusi sia nell' [**\_ input WM**](wm-input.md) del messaggio HID che nei messaggi tradizionali. Un'applicazione può selezionare uno dei metodi in base alla selezione appropriata dei flag in [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice).

Per ottenere lo stato di registrazione di un'applicazione, chiamare [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) in qualsiasi momento.

## <a name="reading-raw-input"></a>Lettura dell'input non elaborato

Un'applicazione riceve input non elaborato da qualsiasi HID la cui [raccolta di livello superiore](/windows-hardware/drivers/hid/top-level-collections) (TLC) corrisponde a una TLC dalla registrazione. Quando un'applicazione riceve un input non elaborato, la coda di messaggi riceve un messaggio di [**\_ input WM**](wm-input.md) e il flag di stato della coda **QS \_ rawinput** è impostato (l'**\_ input QS** include anche questo flag). Un'applicazione può ricevere dati quando si trova in primo piano e quando si trova in background.

Esistono due modi per leggere i dati non elaborati: il metodo non memorizzato nel buffer (o standard) e il metodo memorizzato nel buffer. Il metodo non memorizzato nel buffer ottiene i dati non elaborati una struttura [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) alla volta ed è adeguata per molti HIDS. In questo caso, l'applicazione chiama [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) per ottenere il messaggio di [**\_ input WM**](wm-input.md) . Quindi, l'applicazione chiama [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata) usando l'handle **rawinput** contenuto **nell' \_ input WM**. Per un esempio, vedere la pagina relativa alla [lettura di un input non elaborato standard](using-raw-input.md).

Al contrario, il metodo memorizzato nel buffer ottiene una matrice di strutture [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) alla volta. Viene fornito per i dispositivi che possono produrre grandi quantità di input non elaborato. In questo metodo, l'applicazione chiama [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) per ottenere una matrice di strutture **rawinput** . Si noti che la macro [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock) viene utilizzata per attraversare una matrice di strutture **rawinput** . Per un esempio, vedere la pagina relativa alla [lettura di un input non elaborato memorizzato nel buffer](using-raw-input.md).

Per interpretare l'input non elaborato, è necessario ottenere informazioni dettagliate sul HIDs. Un'applicazione ottiene le informazioni sul dispositivo chiamando [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) con l'handle del dispositivo. Questo handle può provenire dall' [**\_ input WM**](wm-input.md) o dal membro **hDevice** di [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader).