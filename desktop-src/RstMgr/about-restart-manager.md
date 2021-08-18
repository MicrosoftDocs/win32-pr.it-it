---
title: Informazioni su Gestione riavvio
description: Il motivo principale per cui l'installazione del software e gli aggiornamenti richiedono un riavvio del sistema è che alcuni dei file che vengono aggiornati vengono attualmente usati da un'applicazione o un servizio in esecuzione.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Restart Manager Restart Mgr , about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98003ff4193ce26eb4ed2a3bdab60db8d58adf86698c6b9369a80b8043458579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010299"
---
# <a name="about-restart-manager"></a>Informazioni su Gestione riavvio

Il motivo principale per cui l'installazione del software e gli aggiornamenti richiedono un riavvio del sistema è che alcuni dei file che vengono aggiornati vengono attualmente usati da un'applicazione o un servizio in esecuzione. Gestione riavvio consente di arrestare e riavviare tutte le applicazioni e i servizi critici, ad esempio . In questo modo i file in uso vengono liberati e le operazioni di installazione possono essere completate. Può anche eliminare o ridurre il numero di riavvii del sistema necessari per completare un'installazione o un aggiornamento.

Gestione riavvio arresta le applicazioni nell'ordine seguente e, dopo l'aggiornamento delle applicazioni, riavvia le applicazioni registrate per il riavvio nell'ordine inverso.

1.  Applicazioni GUI
2.  Applicazioni console
3.  Servizi Windows
4.  Windows explorer

Restart Manager arresta l'applicazione o i servizi solo se il chiamante dispone delle autorizzazioni necessarie. Si noti che l'arresto tra le sessioni non è supportato.

Le applicazioni che usano il Windows [installer](/windows/desktop/Msi/windows-installer-portal) versione 4.0 per l'installazione e la manutenzione usano automaticamente Gestione riavvio per ridurre i riavvii del sistema. I programmi di installazione personalizzati possono anche essere progettati per chiamare l'API Restart Manager per arrestare e riavviare applicazioni e servizi. Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare l'API Gestione riavvii per pianificare i riavvii in modo da ridurre al minimo l'interruzione del flusso di lavoro dell'utente.

Per informazioni sull'uso dell'API Gestione riavvii durante l'installazione e gli aggiornamenti, vedere [Uso di Gestione riavvio](using-restart-manager.md).

I servizi di sistema critici non possono essere arrestati e riavviati da Gestione riavvio senza un riavvio del sistema. Per altre informazioni sull'identificazione dei servizi di sistema critici, vedere [Servizi di sistema critici](critical-system-services.md).

Le applicazioni e i servizi devono essere pronti per essere arrestati da Gestione riavvii e salvare i dati utente e le informazioni sullo stato necessari per un riavvio pulito. Per altre informazioni su come preparare le applicazioni e i servizi per l'utilizzo con Gestione riavvio, vedere [Linee guida per applicazioni e servizi.](guidelines-for-applications-and-services.md)

Per informazioni di riferimento sulle enumerazioni, le strutture e le funzioni dell'API Gestione riavvio, vedere la sezione Informazioni di riferimento su [Gestione](restart-manager-reference.md) riavvio

 

 