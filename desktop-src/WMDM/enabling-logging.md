---
title: Abilitazione della registrazione
description: Abilitazione della registrazione
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Gestione dispositivi multimediali, registrazione
- Gestione dispositivi, registrazione
- applicazioni desktop, registrazione
- provider di servizi, registrazione
- guida per programmatori, registrazione
- registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff937b2a3abd16f7319c3abb73a3a2159350049fff8c89d343cc5545f8a21ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585119"
---
# <a name="enabling-logging"></a>Abilitazione della registrazione

Windows Gestione dispositivi multimediali fornisce un oggetto di registrazione che consente di salvare le informazioni in un file di testo in fase di esecuzione. Gli sviluppatori di applicazioni e provider di servizi possono usare questo oggetto per archiviare i messaggi in un file di log mentre l'applicazione o il provider di servizi è in esecuzione. Questo oggetto è particolarmente utile quando si gestisce file protetti da DRM, perché Windows Gestione dispositivi multimediali non consente di collegare un debugger a un processo che gestisce i file protetti da DRM.

Il logger è un oggetto COM con l'ID di classe CLSID WMDMLogger che espone \_ un'interfaccia, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger). I componenti non necessitano di un certificato per usare l'oggetto di registrazione.

Per impostazione predefinita, Windows Gestione dispositivi multimediali gestisce un file di log, indipendentemente dal fatto che un'applicazione usi **IWMDMLogger**. Questo file di log è un semplice file di testo e ogni voce include una voce preceduta da un timestamp nel formato AAAAMMGGHHMMSS, usando l'ora locale di 24 ore. Windows Gestione dispositivi multimediali registra tutte le chiamate API, insieme a tutte le voci che si aggiungono chiamando **i messaggi IWMDMLogger.** Tutte le voci del file di log vengono aggiunte al file fino a quando non viene chiamato [**reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) o il file supera le dimensioni massime. Il file viene chiuso automaticamente dopo ogni operazione di registrazione. Lo stesso file di log viene usato per le voci dell'applicazione e le voci di sistema.

La procedura seguente illustra come usare l'oggetto di registrazione:

1.  Includere wmdmlog.h nel progetto.
2.  Creare un oggetto di registrazione chiamando **CoCreateInstance**(CLSID \_ WMDMLogger) e richiedendo **l'interfaccia IWMDMLogger.** Assegnare il puntatore a interfaccia a una variabile globale.
3.  Verificare che la registrazione sia abilitata chiamando [**IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); In caso contrario, abilitarlo chiamando [**IWMDMLogger::Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).
4.  Specificare un nome e una dimensione del file di log personalizzati. Questa operazione viene eseguita chiamando [**IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) e [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).
5.  Nei punti del codice in cui si vuole creare una voce nel log, chiamare [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) per registrare le stringhe contenenti variabili (questo metodo è simile a **wsprintf** nel modo in cui consente di formattare una stringa contenente un valore di variabile) o chiamare [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) per registrare le stringhe costanti.

Per codice di esempio, vedere le pagine di riferimento per i metodi di [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività comuni ad applicazioni e provider di servizi**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




