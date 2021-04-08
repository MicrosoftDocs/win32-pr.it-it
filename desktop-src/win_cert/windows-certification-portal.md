---
title: Certificare l'applicazione desktop
description: Seguire questa procedura per ottenere la certificazione dell'app desktop per Windows 7, Windows 8, Windows 8.1 e Windows 10. Se si vuole convertire l'app desktop in modo che sia compatibile con i piattaforma UWP (Universal Windows Platform) e Windows Store, si userà Windows Desktop Bridge. in questo caso, è necessario seguire le indicazioni sul Bridge per la procedura di certificazione. Se si sta sviluppando e certificando un'app UWP dall'inizio, vedere linee guida per la certificazione delle app Windows in UWP per informazioni sulla certificazione.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734559"
---
# <a name="certify-your-desktop-application"></a>Certificare l'applicazione desktop

> [!IMPORTANT]
> La certificazione per le applicazioni desktop Win32 è [deprecata](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920). Inviare invece [i file qui](https://www.microsoft.com/wdsi/filesubmission/).

Seguire questa procedura per ottenere la certificazione dell'app desktop per Windows 7, Windows 8, Windows 8.1 e Windows 10.

Se si vuole convertire l'app desktop in modo che sia compatibile con il piattaforma UWP (Universal Windows Platform) e Windows Store, si userà [Windows Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop). in questo caso, è necessario seguire le indicazioni sul Bridge per i [Desktop](/windows/uwp/porting/desktop-to-uwp-root) per le procedure di certificazione.

Se si sta sviluppando e certificando un'app UWP dall'inizio, vedere [linee guida per la certificazione delle app Windows in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) per informazioni sulla certificazione.

## <a name="step-1-prepare-for-certification"></a>Passaggio 1: preparare la certificazione



| Argomento                                                                                       | Descrizione                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Quali sono i vantaggi?](what-are-the-benefits-.md)<br/>                             | La certificazione dell'app desktop offre diversi vantaggi per l'utente e i clienti.              |
| [Leggere i requisiti](certification-requirements-for-windows-desktop-apps.md)<br/> | Esaminare i requisiti tecnici e le qualifiche di idoneità che devono essere soddisfatte da un'applicazione desktop. |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a>Passaggio 2: testare l'app con il kit di certificazione app Windows



| Argomento                                                          | Descrizione                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ottenere il kit](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | Per certificare l'app, è necessario installare ed eseguire il kit di certificazione applicazioni Windows (incluso nella Windows SDK).                                                                     |
| [Uso del kit](using-the-windows-app-certification-kit.md)   | Prima di poter inviare l'app, è necessario testarla per verificarne la conformità. È anche possibile scaricare una copia della [white paper di certificazione dell'app](https://www.microsoft.com/download/details.aspx?id=27414). |
| [Esaminare i dettagli del test](windows-app-certification-kit-tests.md) | Ottenere l'elenco dei test che devono essere superati dall'app per qualificarsi per la compatibilità con il sistema operativo Windows più recente.                                                               |



 

Nota: i driver di filtro devono anche passare il [Kit di certificazione hardware](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe). Vedere [la sezione 6,2 relativa ai requisiti di certificazione per le app desktop di Windows](certification-requirements-for-windows-desktop-apps.md).

## <a name="step-3-use-the-windows-certification-dashboard"></a>Passaggio 3: usare il dashboard di certificazione di Windows

Per inviare l'app per la certificazione, è necessario accedere o registrare un account aziendale nel [Dashboard certificazione Windows](/previous-versions/hh833792(v=msdn.10)). Una volta eseguita questa operazione, non solo sarà possibile ottenere la certificazione dell'app, ma si otterrà anche l'accesso agli strumenti per rivedere e gestire l'app in tutte le fasi del processo.



| Argomento                                                                                                                   | Descrizione                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configurare l'account](/windows-hardware/drivers/dashboard/)                 | Se la società non è già registrata, è necessario registrarla tramite il dashboard di certificazione Windows.                                        |
| [Ottenere un certificato di firma del codice](/windows-hardware/drivers/dashboard/)      | Prima di poter stabilire un account dashboard di certificazione Windows, è necessario ottenere un certificato di firma codice per proteggere le informazioni digitali. |
| [Testare localmente e caricare i risultati](/windows-hardware/drivers/dashboard/) | Dopo aver eseguito i test del kit di certificazione app Windows, caricare i risultati nel dashboard di certificazione Windows.                                 |
| [Gestire l'invio](/windows-hardware/drivers/dashboard/)              | Dopo aver inviato l'app per la certificazione, è possibile esaminare l'invio tramite il dashboard di certificazione Windows.                           |



 

## <a name="step-4-promote-your-desktop-app"></a>Passaggio 4: promuovere l'app desktop



| Argomento                                                                      | Descrizione                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Verifica compatibilità app](/windows/compatibility/windows-8-1-introduction) | Se si compila un'app per Windows 8.1, analizzare i problemi di compatibilità.                                           |
| [Usare il logo con l'app](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | Consente di visualizzare il logo nella creazione di pacchetti e negli annunci e in altri materiali promozionali in base alle linee guida. Solo per Windows 7. |



 

## <a name="see-also"></a>Vedere anche la pagina relativa alla

[Forum sulla compatibilità delle app](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): supporto della community sulla compatibilità e sulla certificazione del logo.

[Blog Windows SDK](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): suggerimenti e notizie relativi alla certificazione delle app.

[Forum su Windows Server]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): visitare il forum di certificazione per ottenere risposte.

[Cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)per la compatibilità: informazioni sulle novità o le modifiche apportate alla versione più recente di Windows.

 

