---
description: In questa sezione vengono descritte le tecnologie di Windows che consentono di supportare le numerose impostazioni cultura e i linguaggi scritti del Marketplace internazionale nell'applicazione Microsoft Win32 basata su C o C++.
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Internazionalizzazione per le applicazioni di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f6e4952c94af3b14dc0e8f4f135c1cc0cebafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752335"
---
# <a name="internationalization-for-windows-applications"></a>Internazionalizzazione per le applicazioni di Windows

(In precedenza denominato "supporto internazionale")

In questa sezione vengono descritte le tecnologie di Windows che consentono di supportare le numerose impostazioni cultura e i linguaggi scritti del Marketplace internazionale nell'applicazione Microsoft Win32 basata su C o C++.

Windows è diventato una piattaforma essenziale per i clienti in tutto il mondo. Gli utenti internazionali si aspettano soluzioni adattate a lingue e aree geografiche in tutto il mondo. In questa sezione sono disponibili le informazioni necessarie per sviluppare soluzioni multilingue, multiculturali e multisito. Il supporto internazionale integrato in Windows consente di implementare molti scenari con un sovraccarico di progettazione inferiore rispetto al passato.

Per lo sviluppo di applicazioni predisposte per l'internazionalizzazione è necessario usare molti servizi e strumenti. Windows contiene funzionalità che consentono di sviluppare soluzioni che:

- Supportare le diverse esigenze specifiche della lingua e delle impostazioni locali degli utenti in tutto il mondo (inclusi il supporto per testo specializzato, il comportamento di ordinamento, la formattazione di data e ora e i layout di tastiera). Per ulteriori informazioni, vedere [Knowledge Center per il supporto nazionale](./national-language-support-reference.md).
- Sono globalizzate (possono essere distribuite in tutto il mondo da un'unica immagine binaria) e possono essere localizzate (in grado di essere adattate per mercati locali specifici). Per ulteriori informazioni, vedere [interfaccia utente multilingue](./multilingual-user-interface.md).
- Visualizzare i tipi di carattere e il testo internazionali e consentire agli utenti di specificare il tipo di carattere desiderato. Per ulteriori informazioni, vedere [supporto di script e tipi di carattere in Windows](/globalization/input/font-support).
- Consente all'utente di immettere caratteri e simboli complessi con una tastiera standard.
- Fornire il supporto per molte lingue scritte diverse tramite i set di caratteri Unicode e tradizionali.
- Individuare l'input della lingua da parte di un utente e personalizzare l'esperienza utente fornita dall'applicazione. (Per altre informazioni, vedere [scrittura di applicazioni internazionali in Windows: Servizi linguistici estesi in Windows](./using-extended-linguistic-services.md)).

## <a name="in-this-section"></a>Contenuto della sezione

In questa sezione sono descritte le tecnologie di supporto internazionale seguenti. Sono elencati con alcuni scenari chiave per cui possono essere usati.

- [Introduzione con sviluppo Windows internazionale](getting-started-with-international-development.md)

    Viene descritto come iniziare a creare applicazioni internazionali e viene fornita un'esercitazione che illustra un'attività comune per la scrittura di software globale.

    Scenari comuni:

    - Determinare un percorso da seguire per apprendere come sviluppare software internazionale.
    - Scopri le tecnologie di internazionalizzazione disponibili nel Software Development Kit (SDK) di Microsoft Windows.
    - Seguire un'esercitazione che accetta un'applicazione monolingue esistente e aggiunge il supporto per altre lingue.

- [Servizi di globalizzazione](globalization-services.md)

    Descrive i [servizi linguistici estesi (ELS)](extended-linguistic-services.md), che consentono di individuare la lingua in cui è scritto il testo e l'input dell'utente e il [NLS (National Language Support)](national-language-support.md), che consente a un'applicazione di usare le informazioni sulle impostazioni locali per visualizzare informazioni dipendenti dalle impostazioni cultura, ad esempio ora, date e valuta, e ordinare correttamente le stringhe.

    Scenari comuni:

    - Individuare la lingua dell'input dell'utente, in modo che il contenuto della guida possa essere visualizzato in un linguaggio comprensibile.
    - Individuare lo script utilizzato nel testo da visualizzare. Se è semplificato o cinese tradizionale, offrire all'utente la possibilità di fare in modo che il testo venga traslitterato da uno all'altro.
    - Consente all'utente di selezionare le impostazioni locali, ovvero una raccolta di informazioni sulle preferenze dell'utente relative alla lingua.
    - Visualizza orari, date, informazioni sul calendario, valuta e molti altri oggetti dipendenti dalle impostazioni cultura in linguaggi e formati appropriati.
    - Ordinare le stringhe nell'ordine previsto dall'utente delle impostazioni locali specificate.

- [Gestione metodo di input](input-method-manager.md)

    Viene descritta la tecnologia utilizzata da un'applicazione per comunicare con un Input Method Editor (IME). L'IME consente agli utenti del computer di immettere caratteri e simboli complessi utilizzando una tastiera standard.

    Scenario comune:

    - Consente all'utente di usare una tastiera standard per immettere caratteri kanji giapponesi.

- [Caratteri internazionali e visualizzazione del testo](international-fonts-and-text-display.md)

    Viene descritto il supporto fornito dalla piattaforma Windows per i tipi di carattere internazionali, testo internazionale e tipografia.

    Scenari comuni:

    - Consente all'utente di selezionare i caratteri internazionali in base al set di caratteri.
    - Visualizza testo internazionale.
    - Elabora script complessi, tra cui il rendering bidirezionale, il Shaping contestuale e le legature (Uniscribe).
    - Consente un elevato livello di controllo per la tipografia fine (Uniscribe).

- [Interfaccia utente multilingue](multilingual-user-interface.md)

    Viene descritto in che modo le applicazioni possono separare le risorse dipendenti dalla lingua dal codice indipendente dalla lingua per le lingue supportate dell'interfaccia utente.

    Scenari comuni:

    - Creare immagini di distribuzione singola a livello di area o globale di un'applicazione.
    - Localizzare una soluzione aggiornando le risorse dell'applicazione senza apportare modifiche al codice sorgente dell'applicazione.
    - Consente agli utenti di passare da una lingua dell'interfaccia utente a un'altra in fase di esecuzione.

- [Unicode e set di caratteri](unicode-and-character-sets.md)

    Viene descritto in che modo le applicazioni possono sfruttare i vantaggi di Unicode, lo standard di codifica dei caratteri in tutto il mondo che utilizza valori di codice a 16 bit per rappresentare tutti i caratteri utilizzati nell'elaborazione moderna, inclusi i simboli tecnici e i caratteri speciali utilizzati per la pubblicazione.

    Scenari comuni:

    - Supporta le varie lingue del Marketplace internazionale tramite Unicode.
    - Convertire i caratteri Unicode in e da altri set di caratteri, quando necessario.

- [Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md)

    Vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alle funzionalità di supporto per lo sviluppo internazionale.

    Le informazioni di sicurezza sono relative a tutti gli scenari.

## <a name="related-international-technologies"></a>Tecnologie internazionali correlate

Il supporto per lo sviluppo internazionale è disponibile anche per le applicazioni scritte in codice gestito. Se si sta sviluppando per il .NET Framework, saranno necessari alcuni o tutti i seguenti:

- Lo [spazio dei nomi System. Globalization](/dotnet/api/system.globalization) contiene classi che definiscono le informazioni correlate alle impostazioni cultura e forniscono funzioni di globalizzazione avanzate.
- Lo [spazio dei nomi System. Text](/dotnet/api/system.text) contiene classi che rappresentano codifiche di caratteri, convertono blocchi di caratteri e modificano e formattano oggetti stringa.
