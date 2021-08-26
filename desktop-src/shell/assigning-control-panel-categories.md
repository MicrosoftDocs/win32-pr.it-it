---
description: A Windows XP, Pannello di controllo supporta la categorizzazione Pannello di controllo elementi. Gli elementi vengono registrati per essere visualizzati in una o più categorie. Non è possibile creare nuove categorie.
title: Assegnazione di Pannello di controllo categorie
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b6785a786bfe80f5a5b13bc5e9dfbe39507a2c9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478487"
---
# <a name="assigning-control-panel-categories"></a>Assegnazione di Pannello di controllo categorie

A Windows XP, Pannello di controllo supporta la categorizzazione Pannello di controllo elementi. Gli elementi vengono registrati per essere visualizzati in una o più categorie. Non è possibile creare nuove categorie.

Per registrare un elemento Pannello di controllo in una o più [](registering-control-panel-items.md) categorie, aggiungere i valori come illustrato nella sezione Registrazione elemento Pannello di controllo eseguibile o registrazione elemento [DLL Pannello di controllo](registering-control-panel-items.md) di Registrazione elementi Pannello di controllo [,](registering-control-panel-items.md)in base alle esigenze.




| ID della categoria | Nome categoria (Windows 7) | Nome categoria (Windows Vista) | Nome categoria (Windows XP) | 
|-------------|---------------------------|-------------------------------|----------------------------|
| 0 | "Tutti Pannello di controllo elementi" | "Opzioni aggiuntive"<blockquote>[!Note]<br />Qualsiasi Pannello di controllo elemento che non specifica un ID categoria viene visualizzato in questa categoria.</blockquote><br /> | "Altre Pannello di controllo opzioni"<blockquote>[!Note]<br />Qualsiasi Pannello di controllo elemento che non specifica un ID categoria viene visualizzato in questa categoria.</blockquote><br /> | 
| 1 | "Aspetto e personalizzazione" | "Aspetto e personalizzazione" | "Aspetto e temi" | 
| 2 | "Hardware e suono" | "Hardware e suono" | "Stampanti e altro hardware" | 
| 3 | "Rete e Internet" | "Rete e Internet" | "Connessioni di rete e Internet" | 
| 4 | Non più utilizzata. Qualsiasi elemento che si aggiunge solo alla categoria 4 viene visualizzato nella categoria 2 (Hardware e suono). | Non più utilizzata. Qualsiasi elemento che si aggiunge solo alla categoria 4 viene visualizzato nella categoria 2 (Hardware e suono). | "Suoni, voce e dispositivi audio" | 
| 5 | "Sistema e sicurezza" | "Sistema e manutenzione" | "Prestazioni e manutenzione" | 
| 6 | "Orologio, lingua e area geografica" | "Orologio, lingua e area geografica" | "Data, ora, lingua e opzioni internazionali" | 
| 7 | "Accessibilità" | "Accessibilità" | "Opzioni di accessibilità" | 
| 8 | "Programmi" | "Programmi" | "Installazione applicazioni" | 
| 9 | "Account utente"<blockquote>[!Note]<br />Quando non si è connessi a un dominio, si chiama "Account utente e Family Safety".</blockquote><br /> | "Account utente"<blockquote>[!Note]<br />Quando non si è connessi a un dominio, si chiama "Account utente e Family Safety".</blockquote><br /> | "Account utente" | 
| 10 | Non più utilizzata. Gli elementi registrati in questa categoria vengono visualizzati nella categoria 5 (Sistema e sicurezza). | "Security" | "Centro sicurezza"<blockquote>[!Note]<br />Disponibile solo in Windows XP Service Pack 2 (SP2) o versione successiva.</blockquote><br /> | 
| 11 | Non più utilizzata. Gli elementi registrati in questa categoria vengono visualizzati nella categoria 0 (Tutti Pannello di controllo elementi). | "PC mobile"<blockquote>[!Note]<br />Questa categoria è visibile solo nei PC mobili.</blockquote><br /> | Non usato. | 




 

In Windows XP, le  categorie Installazione  applicazioni e Account utente funzionano in modo leggermente diverso rispetto ad altre categorie in Pannello di controllo. Quando uno o più elementi vengono aggiunti a una di queste due categorie, il collegamento associato in Pannello di controllo apre una pagina di categoria. Gli elementi registrati vengono visualizzati nella parte inferiore della pagina sotto l'intestazione "o Selezionare un Pannello di controllo icona". Quando non viene registrato alcun elemento per una di queste categorie, il collegamento associato in Pannello di controllo richiama direttamente l'elemento Windows standard per tale categoria. In Windows Vista e versioni successive, la **categoria Programmi** e la **categoria Account** utente non hanno questa proprietà.

Anche **la categoria Del** Centro sicurezza, disponibile solo Windows XP SP2, è in qualche modo non standard. Facendo clic su questa categoria si apre la pagina **Centro** sicurezza in una nuova finestra. Gli elementi registrati **per il Centro sicurezza** vengono visualizzati nella parte inferiore della pagina sotto l'intestazione Gestisci impostazioni di sicurezza **per:**. Facendo clic su un'icona si apre Pannello di controllo elemento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pannello di controllo elementi](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione di Pannello di controllo elementi](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Pannello di controllo di messaggi](message-processing.md)
</dt> <dt>

[Esecuzione di Pannello di controllo elementi](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi Pannello di controllo sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Creazione di collegamenti di attività ricercabili per un Pannello di controllo elemento](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al Pannello di controllo in modalità Cassaforte in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




