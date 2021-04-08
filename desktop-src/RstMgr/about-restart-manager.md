---
title: Informazioni su Gestione riavvio
description: Il motivo principale per cui l'installazione e gli aggiornamenti del software richiede un riavvio del sistema è che alcuni dei file da aggiornare sono attualmente utilizzati da un'applicazione o da un servizio in esecuzione.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Riavviare Gestione riavvio gestione, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1cfd300d554e311ab43cc0a9413514b6b60081
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729575"
---
# <a name="about-restart-manager"></a>Informazioni su Gestione riavvio

Il motivo principale per cui l'installazione e gli aggiornamenti del software richiede un riavvio del sistema è che alcuni dei file da aggiornare sono attualmente utilizzati da un'applicazione o da un servizio in esecuzione. Gestione riavvio consente l'arresto e il riavvio di tutti i servizi e delle applicazioni critiche. Ciò consente di liberare i file in uso e di completare le operazioni di installazione. Consente inoltre di eliminare o ridurre il numero di riavvii del sistema necessari per completare un'installazione o un aggiornamento.

Gestione riavvio interrompe le applicazioni nell'ordine seguente e, dopo l'aggiornamento delle applicazioni, riavvia le applicazioni che sono state registrate per il riavvio in ordine inverso.

1.  Applicazioni GUI
2.  Applicazioni console
3.  Servizi Windows
4.  Esplora risorse

Gestione riavvio arresta l'applicazione o i servizi solo se il chiamante dispone delle autorizzazioni necessarie. Si noti che l'arresto tra le sessioni non è supportato.

Le applicazioni che usano la versione di [Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4,0 per l'installazione e la manutenzione utilizzano automaticamente Gestione riavvio per ridurre i riavvii del sistema. I programmi di installazione personalizzati possono anche essere progettati per chiamare l'API di gestione riavvio per arrestare e riavviare le applicazioni e i servizi. Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare l'API di gestione riavvio per pianificare i riavvii in modo da ridurre al minimo l'alterazione del flusso di lavoro dell'utente.

Per informazioni sull'uso dell'API Gestione riavvio durante l'installazione e gli aggiornamenti, vedere [uso di gestione riavvio](using-restart-manager.md).

I servizi di sistema critici non possono essere arrestati e riavviati da Gestione riavvio senza riavvio del sistema. Per ulteriori informazioni sull'identificazione dei servizi di sistema critici, vedere [Critical System Services](critical-system-services.md).

Le applicazioni e i servizi devono essere preparati per essere arrestati da Gestione riavvio e salvare i dati utente e le informazioni sullo stato necessarie per un riavvio pulito. Per ulteriori informazioni su come preparare le applicazioni e i servizi in modo che funzionino con Gestione riavvio, vedere [linee guida per le applicazioni e i servizi](guidelines-for-applications-and-services.md).

Per informazioni di riferimento sulle enumerazioni, le strutture e le funzioni dell'API di gestione riavvio, vedere la sezione [riferimento a gestione riavvio](restart-manager-reference.md)

 

 