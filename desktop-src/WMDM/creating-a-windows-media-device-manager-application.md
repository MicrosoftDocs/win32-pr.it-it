---
title: Creazione di un'Windows di Gestione dispositivi multimediali
description: Creazione di un'Windows di Gestione dispositivi multimediali
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Gestione dispositivi multimediali, creazione di applicazioni
- Gestione dispositivi, creazione di applicazioni
- Windows Gestione dispositivi multimediali, guida alla programmazione
- Gestione dispositivi, guida alla programmazione
- guida per programmatori, applicazioni desktop
- Guida per programmatori, Windows Gestione dispositivi multimediali
- guida per programmatori, plug-in
- guida per programmatori, creazione di applicazioni
- Windows Gestione dispositivi multimediali, applicazioni desktop
- Gestione dispositivi, applicazioni desktop
- Windows Gestione dispositivi multimediali, plug-in
- Gestione dispositivi, plug-insp
- plug-in, creazione
- plug-in, guida per programmatori
- applicazioni desktop, creazione
- creazione Windows applicazioni di Gestione dispositivi multimediali, informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba468d4d9a04176847259087b8ba2626c2ffa3e0cac089f8433993320a7e125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585558"
---
# <a name="creating-a-windows-media-device-manager-application"></a>Creazione di un'Windows di Gestione dispositivi multimediali

In questa sezione viene descritto come usare Windows Gestione dispositivi multimediali nell'applicazione. Il termine "applicazione" in questo caso indica un eseguibile, ad esempio un lettore multimediale, o un plug-in COM, ad esempio un plug-in di controllo.

Microsoft include diversi provider di servizi con Windows XP e Windows Media Player 10, tra cui un provider di servizi MTP, un provider di servizi Windows CE (per i dispositivi che eseguono Windows CE e che usano il protocollo RAPI, ad esempio Pocket PC) e un provider di servizi per dispositivi di categoria di archiviazione di massa (MSC). È anche possibile creare un provider di servizi personalizzato per garantire la comunicazione con il proprio dispositivo. Per altre informazioni, vedere [Creazione di un provider di servizi](creating-a-service-provider.md).

Esistono diversi provider di servizi legacy di terze parti che si indirizzano al dispositivo non MTP, non RAPI o non MSC di un determinato produttore. Questi provider di servizi sono inclusi nel disco driver fornito con questi dispositivi.

Un'applicazione che usa Windows Gestione dispositivi multimediali deve eseguire la procedura seguente.

1.  **Tenere presente i problemi di privacy relativi allo sviluppo di un'applicazione.** Per [informazioni su alcuni](privacy-statement.md) problemi di privacy relativi allo sviluppo di un'Windows Media Device Manager, vedere Informativa sulla privacy.
2.  **Includere la libreria e i file di intestazione necessari per l'applicazione.** Per [informazioni sui](required-library-and-header-files-for-an-application.md) file da includere nel progetto, vedere Libreria e file di intestazione necessari per un'applicazione.
3.  **Autenticare l'applicazione e acquisire l'interfaccia IWMDMDevice radice.** La prima attività che un'applicazione deve eseguire per Windows Gestione dispositivi multimediali è l'autenticazione. Questo processo verifica l'identità dell'applicazione Windows Gestione dispositivi multimediali usando un certificato fittizio per funzionalità limitate di Gestione dispositivi multimediali di Windows o usando un certificato ufficiale per la funzionalità completa. Per altre informazioni, vedere [Autenticazione dell'applicazione](authenticating-the-application.md).
4.  **Enumerare i dispositivi connessi.** Il primo passaggio per la comunicazione con i dispositivi consiste nel individuare i dispositivi connessi e accessibili Windows Gestione dispositivi multimediali. Per altre informazioni, vedere [Enumerazione dei dispositivi](enumerating-devices.md).
5.  **Controllare lo stato dei componenti DRM del dispositivo.** Per usare file protetti da DRM, è necessario che un dispositivo sia basato su una versione di Windows Media DRM per dispositivi portatili e che i componenti DRM siano aggiornati. Prima di iniziare a gestire i file nel dispositivo, è meglio verificare se il dispositivo supporta i file protetti da DRM e se il dispositivo deve essere aggiornato. Per altre informazioni, vedere [Gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md).
6.  **Esplorare un dispositivo.** Dopo aver trovato il dispositivo desiderato, è possibile esplorarne il contenuto. Per altre informazioni, vedere [Esplorazione di un dispositivo](exploring-a-device.md).
7.  **Leggere i file dal dispositivo e scrivere i file nel dispositivo.** Dopo aver informazioni sul layout del dispositivo, è possibile iniziare a trasferire i file da e verso il dispositivo. Per altre informazioni, vedere [Lettura di file dal dispositivo](reading-files-from-the-device.md) e Scrittura di file nel [dispositivo](writing-files-to-the-device.md).
8.  **Creare playlist nel dispositivo.** Un tipo di file che è possibile scrivere nel dispositivo è un file astratto, ovvero una raccolta di riferimenti ad altri file. Anche se la possibilità di scrivere file astratti in un dispositivo dipende dal provider di servizi e dal dispositivo, in genere solo i dispositivi MTP hanno questa funzionalità. Per altre informazioni, vedere [Creazione di una playlist nel dispositivo](creating-a-playlist-on-the-device.md).

Oltre a questi passaggi, sono disponibili diverse altre funzionalità che è possibile abilitare nell'applicazione:

-   **Notifiche.** È possibile abilitare l'applicazione per ricevere notifiche quando i dispositivi si connettono o si disconnettino dal computer. Per altre informazioni, vedere [Abilitazione delle notifiche](enabling-notifications.md).
-   **Registrazione.** Windows Gestione dispositivi multimediali usa un oggetto di registrazione che salva un record delle relative azioni in un file di testo locale. È possibile aggiungere messaggi a questo log per analizzare gli errori o le prestazioni nell'applicazione. Per altre informazioni, vedere [Abilitazione della registrazione](enabling-logging.md).
-   **Misurazione dell'utilizzo del contenuto.** È possibile recuperare le statistiche di utilizzo del contenuto per le licenze che concedono questo diritto. Queste statistiche possono quindi essere inviate a un server Web per calcolare i pagamenti delle royalty ai proprietari di contenuti. Per altre informazioni, vedere [Controllo dell'utilizzo del contenuto.](metering-content-usage.md)

**Nota di cautela**

L'applicazione potrebbe dover usare un'ampia gamma di dispositivi, inclusi alcuni che non sono stati sviluppati e non hanno mai testato il codice. Questi dispositivi potrebbero o meno rispondere in modo accurato a query e comandi o implementare MTP o altre specifiche. Assicurarsi di includere funzionalità affidabili di controllo degli errori e fallback per gestire l'imprevisto. Programmare in modo difensivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 




