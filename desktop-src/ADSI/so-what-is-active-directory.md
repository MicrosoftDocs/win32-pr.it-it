---
title: Panoramica dell'esercitazione ADSI con Visual Basic
description: Active Directory è un database per scopi specifici \ 8212; non si tratta di una sostituzione del registro di sistema.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104566424"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Panoramica dell'esercitazione: ADSI con Visual Basic

> [!Note]  
> La documentazione seguente fa parte di una descrizione dello scenario esteso per gli sviluppatori Visual Basic. Per una panoramica generale di Active Directory, vedere la [documentazione relativa ai professionisti IT in TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)). Per un esame più approfondito del lato sviluppo di Active Directory, vedere [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services). Per un'introduzione più ampia alle interfacce del servizio Active Directory, vedere l'argomento padre di questo argomento: [Active Directory le interfacce del servizio](active-directory-service-interfaces-adsi.md), nonché l'argomento di pari livello: [informazioni sulle interfacce di servizio di Active Directory](about-adsi.md).

 

Active Directory è un database per scopi specifici, non si tratta di una sostituzione del registro di sistema. La directory è progettata per gestire un numero elevato di operazioni di lettura e ricerca e un numero significativamente inferiore di modifiche e aggiornamenti. I dati Active Directory sono gerarchici, replicati ed estendibili. Poiché è replicato, non si desidera archiviare i dati dinamici, ad esempio i prezzi delle scorte aziendali o le prestazioni della CPU. Se i dati sono specifici del computer, archiviare i dati nel registro di sistema. Esempi tipici di dati archiviati nella directory includono i dati della coda della stampante, i dati di contatto dell'utente e i dati di configurazione di rete/computer. Il database Active Directory è costituito da oggetti e attributi. Gli oggetti e le definizioni degli attributi vengono archiviati nello schema di Active Directory.

È possibile che si stiano chiedendo quali oggetti sono attualmente archiviati in Active Directory. Active Directory dispone di tre partizioni. Questi sono anche noti come contesti di denominazione: dominio, schema e configurazione. La partizione di dominio contiene utenti, gruppi, contatti, computer, unità organizzative e molti altri tipi di oggetto. Poiché Active Directory è estensibile, è anche possibile aggiungere classi e/o attributi personalizzati. La partizione dello schema contiene le classi e le definizioni di attributo. La partizione di configurazione include i dati di configurazione per servizi, partizioni e siti.

Lo screenshot seguente mostra la partizione del dominio Active Directory.

![partizione di dominio Active Directory](images/adadsi1.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso a Active Directory tramite Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Scenario: Fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> </dl>

 

 