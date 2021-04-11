---
title: Panoramica del provider WMI DNS
description: Un provider è un elemento architetturale di Strumentazione gestione Windows (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Domain Name System, provider WMI, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044585"
---
# <a name="dns-wmi-provider-overview"></a>Panoramica del provider WMI DNS

Un provider è un elemento architetturale di *Strumentazione gestione Windows (WMI)*. WMI definisce un'architettura unificata per la descrizione, l'accesso e la strumentazione degli oggetti. Parte di questa architettura è un database di grandi dimensioni di classi WMI utilizzate per eseguire attività di gestione remota su oggetti specifici.

I provider WMI fungono da intermediari tra WMI e uno o più oggetti gestiti. Quando WMI riceve una richiesta da un'applicazione di gestione per i dati che non sono disponibili dal repository CIM o per le notifiche di eventi non supportati da WMI, inoltra la richiesta a un provider. I provider forniscono dati e notifiche di eventi per gli oggetti gestiti specifici del proprio dominio. Un provider estende lo schema WMI delle classi per consentire l'utilizzo di WMI con nuovi tipi di oggetti. Il provider WMI DNS definisce le classi per l'esecuzione di query e la configurazione di un server DNS, insieme alle zone DNS e ai record DNS associati.

Il provider WMI DNS espone alcuni oggetti DNS ai client, tra cui server DNS, dominio DNS e oggetti RR DNS. Attraverso questi oggetti, i client sono in grado di eseguire attività di gestione DNS.

Utilizzando il provider WMI DNS, è possibile creare strumenti personalizzati per eseguire la maggior parte delle attività di amministrazione del server DNS. Ad esempio, è possibile creare, eliminare e visualizzare le zone e i record; Reimposta le proprietà del server e della zona; ed eseguono operazioni di amministrazione di routine, ad esempio l'aggiornamento della zona, il ricaricamento della zona, l'aggiornamento della zona, la riscrittura della zona in un file o Active Directory, la sospensione e la ripresa della zona, la cancellazione della cache, l'arresto e l'avvio del servizio DNS e la visualizzazione delle statistiche.

Il provider WMI DNS ha un set di comportamenti univoci non trovato in altri provider. Per informazioni dettagliate sulla classe, vedere la Guida di [riferimento del provider WMI DNS](dns-wmi-provider-reference.md) .

 

 




