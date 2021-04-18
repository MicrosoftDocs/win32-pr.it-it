---
title: Creazione di un'applicazione Windows Media Gestione dispositivi
description: Creazione di un'applicazione Windows Media Gestione dispositivi
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Media Gestione dispositivi, creazione di applicazioni
- Gestione dispositivi, creazione di applicazioni
- Windows Media Gestione dispositivi, Guida alla programmazione
- Gestione dispositivi, Guida alla programmazione
- Guida per programmatori, applicazioni desktop
- Guida per programmatori, Windows Media Gestione dispositivi
- Guida per programmatori, plug-in
- Guida per programmatori, creazione di applicazioni
- Windows Media Gestione dispositivi, applicazioni desktop
- Gestione dispositivi, applicazioni desktop
- Windows Media Gestione dispositivi, plug-in
- Gestione dispositivi, plug-Insp
- plug-in, creazione
- plug-in, Guida alla programmazione
- applicazioni desktop, creazione
- creazione di applicazioni Windows Media Gestione dispositivi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b50a2dfce057b993f84c0aca4c8f45796f67ba8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298047"
---
# <a name="creating-a-windows-media-device-manager-application"></a>Creazione di un'applicazione Windows Media Gestione dispositivi

In questa sezione viene descritto come utilizzare Windows Media Gestione dispositivi nell'applicazione. Il termine "applicazione" indica un eseguibile, ad esempio un lettore multimediale o un plug-in COM, ad esempio un plug-in di misurazione.

Microsoft include diversi provider di servizi con Windows XP e Windows Media Player 10, tra cui un provider di servizi MTP, un provider di servizi Windows CE (per i dispositivi che eseguono Windows CE e l'uso del protocollo RAPI, ad esempio Pocket PC) e un provider di servizi per i dispositivi di categoria di archiviazione di massa (MSC). È anche possibile creare un provider di servizi personalizzato per garantire la comunicazione con il proprio dispositivo. Per ulteriori informazioni, vedere [creazione di un provider di servizi](creating-a-service-provider.md).

Sono disponibili diversi provider di servizi legacy di terze parti che fanno riferimento a un dispositivo non MTP, non RAPI o non master di un produttore specifico. Questi provider di servizi sono inclusi nel disco driver fornito con questi dispositivi.

Un'applicazione che utilizza Windows Media Gestione dispositivi deve eseguire i passaggi seguenti.

1.  **Acquisire familiarità con i problemi di privacy relativi allo sviluppo di un'applicazione.** Vedere [informativa sulla privacy](privacy-statement.md) per informazioni su alcuni problemi di privacy riguardanti lo sviluppo di un'applicazione Windows Media Gestione dispositivi.
2.  **Includere i file di intestazione e di libreria necessari per l'applicazione.** Per informazioni sui file che è necessario includere nel progetto, vedere la [libreria e i file di intestazione necessari per un'applicazione](required-library-and-header-files-for-an-application.md) .
3.  **Autenticare l'applicazione e acquisire l'interfaccia IWMDMDevice radice.** La prima attività che un'applicazione deve eseguire per utilizzare Windows Media Gestione dispositivi consiste nell'autenticarsi autonomamente. Questo processo consente di verificare l'identità dell'applicazione in Windows Media Gestione dispositivi usando un certificato fittizio per la funzionalità limitata di Windows Media Gestione dispositivi o l'uso di un certificato ufficiale per la funzionalità completa. Per ulteriori informazioni, vedere [autenticazione dell'applicazione](authenticating-the-application.md).
4.  **Enumerare i dispositivi connessi.** Il primo passaggio per la comunicazione con i dispositivi consiste nel determinare quali dispositivi sono connessi e accessibili a Windows Media Gestione dispositivi. Per altre informazioni, vedere [enumerazione dei dispositivi](enumerating-devices.md).
5.  **Verificare lo stato dei componenti DRM del dispositivo.** Per usare i file protetti da DRM, un dispositivo deve essere compilato in una versione di Windows Media DRM per i dispositivi portatili e i componenti DRM devono essere aggiornati. Prima di iniziare a gestire i file nel dispositivo, è consigliabile verificare se il dispositivo supporta i file protetti da DRM e se è necessario aggiornare il dispositivo. Per ulteriori informazioni, vedere [gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md).
6.  **Esplorare un dispositivo.** Dopo aver trovato il dispositivo desiderato, è possibile esplorare il contenuto del dispositivo. Per altre informazioni, vedere [esplorazione di un dispositivo](exploring-a-device.md).
7.  **Leggere i file dal dispositivo e scrivere i file nel dispositivo.** Quando si è a conoscenza del layout del dispositivo, è possibile iniziare a trasferire i file da e verso il dispositivo. Per altre informazioni, vedere la pagina relativa alla [lettura di file dal dispositivo](reading-files-from-the-device.md) e [alla scrittura di file nel dispositivo](writing-files-to-the-device.md).
8.  **Creare playlist nel dispositivo.** Un tipo di file che è possibile scrivere nel dispositivo è un file astratto, ovvero una raccolta di riferimenti ad altri file. Sebbene la possibilità di scrivere file astratti in un dispositivo dipende dal provider di servizi e dal dispositivo, in genere questa funzionalità è consentita solo per i dispositivi MTP. Per altre informazioni, vedere [creazione di una playlist nel dispositivo](creating-a-playlist-on-the-device.md).

Oltre a questi passaggi, sono disponibili diverse altre funzionalità che è possibile abilitare nell'applicazione:

-   **Notifiche.** È possibile abilitare l'applicazione per ricevere notifiche quando i dispositivi si connettono o si disconnettono dal computer. Per ulteriori informazioni, vedere [Abilitazione di notifiche](enabling-notifications.md).
-   **Registrazione.** Windows Media Gestione dispositivi utilizza un oggetto di registrazione che salva una registrazione delle azioni in un file di testo locale. È possibile aggiungere messaggi a questo log per consentire l'analisi degli errori o delle prestazioni nell'applicazione. Per ulteriori informazioni, vedere [Abilitazione della registrazione](enabling-logging.md).
-   **Misurazione dell'utilizzo del contenuto.** È possibile recuperare le statistiche di utilizzo del contenuto per le licenze che concedono questo diritto. Queste statistiche possono quindi essere inviate a un server Web per calcolare i pagamenti di royalties ai proprietari di contenuti. Per ulteriori informazioni, vedere [misurazione dell'utilizzo del contenuto](metering-content-usage.md).

**Una nota cautela**

Potrebbe essere necessario che l'applicazione funzioni con un'ampia gamma di dispositivi, inclusi alcuni che non sono stati sviluppati e non hanno mai testato il codice. Questi dispositivi potrebbero o meno rispondere in modo accurato a query e comandi oppure implementare MTP o altre specifiche. Assicurarsi di includere funzionalità di controllo degli errori e di fallback affidabili per gestire l'imprevisto. Programma difensivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 




