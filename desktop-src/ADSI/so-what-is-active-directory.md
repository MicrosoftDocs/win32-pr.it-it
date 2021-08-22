---
title: Panoramica dell'esercitazione su ADSI con Visual Basic
description: Active Directory è un database per scopi speciali \ 8212; non è una sostituzione del Registro di sistema.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cd6afe11b8991b6ced53367582ddf11d8eba0ea428105d3e9ba39c625d54fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082251"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Panoramica dell'esercitazione: ADSI con Visual Basic

> [!Note]  
> La documentazione seguente fa parte di una descrizione estesa dello scenario per Visual Basic sviluppatori. Per una panoramica generale di Active Directory, vedere la documentazione it [Pro su Technet.](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)) Per un'analisi più approfondita del lato sviluppo di Active Directory, vedere Active Directory Domain Services [.](/windows/desktop/AD/active-directory-domain-services) Per un'introduzione più ampia alle interfacce del servizio [Active Directory,](active-directory-service-interfaces-adsi.md)vedere l'argomento padre di questo argomento: Interfacce del servizio Active Directory, nonché l'argomento di pari livello Informazioni sulle interfacce del servizio Active [Directory.](about-adsi.md)

 

Active Directory è un database per scopi speciali, non è una sostituzione del Registro di sistema. La directory è progettata per gestire un numero elevato di operazioni di lettura e ricerca e un numero significativamente inferiore di modifiche e aggiornamenti. I dati di Active Directory sono gerarchici, replicati ed estensibili. Poiché viene replicato, non si vogliono archiviare dati dinamici, ad esempio i prezzi delle azioni aziendali o le prestazioni della CPU. Se i dati sono specifici del computer, archiviare i dati nel registro. Esempi tipici di dati archiviati nella directory includono i dati della coda della stampante, i dati di contatto dell'utente e i dati di configurazione di rete/computer. Il database di Active Directory è costituito da oggetti e attributi. Gli oggetti e le definizioni degli attributi vengono archiviati nello schema di Active Directory.

Ci si potrebbe chiedere quali oggetti sono attualmente archiviati in Active Directory. Active Directory ha tre partizioni. Questi sono noti anche come contesti di denominazione: dominio, schema e configurazione. La partizione di dominio contiene utenti, gruppi, contatti, computer, unità organizzative e molti altri tipi di oggetto. Poiché Active Directory è estendibile, è anche possibile aggiungere classi e/o attributi personalizzati. La partizione dello schema contiene classi e definizioni di attributi. La partizione di configurazione include i dati di configurazione per servizi, partizioni e siti.

Lo screenshot seguente mostra la partizione di dominio di Active Directory.

![partizione di dominio active directory](images/adadsi1.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso ad Active Directory tramite Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Scenario: The Fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> </dl>

 

 