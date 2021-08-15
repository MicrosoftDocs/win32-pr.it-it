---
description: Questa sezione descrive le tecnologie in Windows che consentono di supportare le numerose impostazioni cultura e lingue scritte del marketplace internazionale nell'applicazione Microsoft Win32 basata su C o C++.
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Internazionalizzazione per le applicazioni di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78f4831390ffc31a5f3290f0784d32c3aa1044863c708e6e0329225519c2cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147544"
---
# <a name="internationalization-for-windows-applications"></a>Internazionalizzazione per le applicazioni di Windows

(in precedenza denominato "Supporto internazionale")

Questa sezione descrive le tecnologie in Windows che consentono di supportare le numerose impostazioni cultura e lingue scritte del marketplace internazionale nell'applicazione Microsoft Win32 basata su C o C++.

Windows è diventata una piattaforma essenziale per i clienti di tutto il mondo. Gli utenti internazionali si aspettano soluzioni adattate alle proprie lingue e aree geografiche in tutto il mondo. In questa sezione sono disponibili le informazioni necessarie per sviluppare soluzioni multilingue, multilingue e multisnodato. Il supporto internazionale integrato in Windows consente di implementare molti scenari con un sovraccarico di progettazione inferiore rispetto al passato.

Lo sviluppo di applicazioni di livello mondiale richiede l'uso di molti servizi e strumenti. Windows contiene funzionalità che consentono di sviluppare soluzioni che:

- Supportare le diverse esigenze specifiche della lingua e delle impostazioni locali degli utenti in tutto il mondo, tra cui supporto del testo specializzato, comportamento di ordinamento, formattazione di data e ora e layout di tastiera. Per altre informazioni, vedere [National Language Support Knowledge Center.](./national-language-support-reference.md)
- Sono globalizzati (possono essere distribuiti in tutto il mondo da una singola immagine binaria) e possono essere localizzati (possono essere adattati per mercati locali specifici). Per altre informazioni, [vedere](./multilingual-user-interface.md)interfaccia utente multilingue .
- Visualizzare i tipi di carattere e il testo internazionali e consentire agli utenti di specificare il tipo di carattere desiderato. Per altre informazioni, vedere Supporto di script e tipi di [carattere in Windows.](/globalization/input/font-support)
- Consente all'utente di immettere caratteri e simboli complessi con una tastiera standard.
- Fornire il supporto per molte lingue scritte diverse tramite Unicode e set di caratteri tradizionali.
- Individuare l'input della lingua da parte di un utente e personalizzare l'esperienza utente fornita dall'applicazione. Per altre informazioni, vedere [Writing World-Ready Applications in Windows: Extended Linguistic Services in Windows](./using-extended-linguistic-services.md).

## <a name="in-this-section"></a>Contenuto della sezione

In questa sezione sono documentate le tecnologie di supporto internazionale seguenti. Sono elencati con alcuni scenari chiave per i quali possono essere usati.

- [Attività iniziali con Lo sviluppo Windows internazionale](getting-started-with-international-development.md)

    Viene descritto come iniziare a creare applicazioni pronte per il mondo e viene fornita un'esercitazione che illustra un'attività comune nella scrittura di software globale.

    Scenari comuni:

    - Determinare un percorso da intraprendere per imparare a sviluppare software internazionale.
    - Informazioni sulle tecnologie di internazionalizzazione disponibili in Microsoft Windows Software Development Kit (SDK).
    - Seguire un'esercitazione che accetta un'applicazione monolingue esistente e aggiunge il supporto per altre lingue.

- [Servizi di globalizzazione](globalization-services.md)

    Descrive Extended [Linguistic Services (ELS),](extended-linguistic-services.md)che consentono di individuare la lingua in cui viene scritto il testo e l'input dell'utente, e [National Language Support (NLS)](national-language-support.md), che consente a un'applicazione di usare le informazioni sulle impostazioni locali per visualizzare informazioni relative alle impostazioni cultura (ad esempio ora, date e valuta) e ordinare correttamente le stringhe.

    Scenari comuni:

    - Individuare la lingua dell'input dell'utente, in modo che il contenuto della Guida possa essere visualizzato in una lingua comprensibile.
    - Individuare lo script usato nel testo da visualizzare. Se è in cinese semplificato o tradizionale, offrire all'utente la possibilità di traslitterare il testo da uno all'altro.
    - Consente all'utente di selezionare le impostazioni locali (una raccolta di informazioni sulle preferenze utente relative alla lingua).
    - Visualizzare ore, date, informazioni sul calendario, valuta e molti altri oggetti dipendenti dalle impostazioni cultura in lingue e formati appropriati.
    - Ordinare le stringhe nell'ordine previsto dall'utente delle impostazioni locali specificate.

- [Gestione metodi di input](input-method-manager.md)

    Descrive la tecnologia usata da un'applicazione per comunicare con un IME (Input Method Editor). L'IME consente agli utenti di computer di immettere caratteri e simboli complessi usando una tastiera standard.

    Scenario comune:

    - Consente all'utente di usare una tastiera standard per immettere caratteri Kanji giapponesi.

- [Tipi di carattere internazionali e visualizzazione del testo](international-fonts-and-text-display.md)

    Descrive il supporto fornito dalla piattaforma di Windows per tipi di carattere internazionali, testo internazionale e tipografia fine.

    Scenari comuni:

    - Consente all'utente di selezionare i tipi di carattere internazionali in base al set di caratteri.
    - Visualizzare il testo internazionale.
    - Elaborare script complessi, tra cui rendering bidirezionale, shaping contestuale e legature (Uniscribe).
    - Consentire un elevato livello di controllo per la tipografia fine (Uniscribe).

- [Interfaccia utente multilingue](multilingual-user-interface.md)

    Viene descritto in che modo le applicazioni possono separare le risorse dipendenti dalla lingua dal codice indipendente dalla lingua per le lingue supportate dell'interfaccia utente.

    Scenari comuni:

    - Creare immagini di distribuzione singola a livello regionale o mondiale di un'applicazione.
    - Localizzare una soluzione aggiornando le risorse dell'applicazione senza modifiche al codice sorgente dell'applicazione.
    - Consente agli utenti di passare da una lingua dell'interfaccia utente a un'altra in fase di esecuzione.

- [Unicode e set di caratteri](unicode-and-character-sets.md)

    Descrive in che modo le applicazioni possono sfruttare Unicode, lo standard di codifica dei caratteri globale che usa valori di codice a 16 bit per rappresentare tutti i caratteri usati nell'elaborazione moderna, inclusi i simboli tecnici e i caratteri speciali usati nella pubblicazione.

    Scenari comuni:

    - Supportare le diverse lingue del marketplace internazionale tramite Unicode.
    - Convertire i caratteri Unicode in e da altri set di caratteri, se necessario.

- [Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md)

    Vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alle funzionalità di supporto per lo sviluppo internazionale.

    Le informazioni di sicurezza riguardano tutti gli scenari.

## <a name="related-international-technologies"></a>Tecnologie internazionali correlate

Il supporto per lo sviluppo internazionale è disponibile anche per le applicazioni scritte in codice gestito. Se si sviluppa per il .NET Framework, saranno necessari alcuni o tutti gli elementi seguenti:

- Lo [spazio dei nomi System.Globalization contiene](/dotnet/api/system.globalization) classi che definiscono informazioni relative alle impostazioni cultura e forniscono funzioni di globalizzazione avanzate.
- Lo [spazio dei nomi System.Text](/dotnet/api/system.text) contiene classi che rappresentano codifiche di caratteri, convertono blocchi di caratteri e modificano e formattano oggetti String.
