---
title: Panoramica del provider WMI DNS
description: Un provider è un elemento architetturale di Windows Management Instrumentation (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Domain Name System, provider WMI, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44103edba64a1f572beef9cff9b8aeb31f02344f172f42b2a7378a6fbf3677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913161"
---
# <a name="dns-wmi-provider-overview"></a>Panoramica del provider WMI DNS

Un provider è un elemento architetturale *di Windows Management Instrumentation (WMI).* WMI definisce un'architettura unificata per la descrizione, l'accesso e la strumentazione degli oggetti. Parte di questa architettura è un database di grandi dimensioni di classi WMI usate per eseguire attività di gestione remota su oggetti specifici.

I provider WMI fungono da intermediari tra WMI e uno o più oggetti gestiti. Quando WMI riceve una richiesta da un'applicazione di gestione per i dati non disponibili nel repository CIM o per le notifiche di eventi non supportati da WMI, inoltra la richiesta a un provider. I provider forniscono dati e notifiche di eventi per gli oggetti gestiti specifici del proprio dominio. Un provider estende lo schema WMI delle classi per consentire a WMI di funzionare con nuovi tipi di oggetti. Il provider WMI DNS definisce le classi per l'esecuzione di query e la configurazione di un server DNS, insieme alle zone DNS e ai record DNS associati.

Il provider WMI DNS espone diversi oggetti DNS ai client, inclusi gli oggetti Server DNS, Dominio DNS e DNS RR. Tramite questi oggetti, i client sono in grado di eseguire attività di gestione DNS.

Usando il provider WMI DNS, è possibile creare strumenti personalizzati per eseguire la maggior parte delle attività di amministrazione del server DNS. Ad esempio, è possibile creare, eliminare e visualizzare zone e record. reimpostare le proprietà del server e della zona; ed eseguire operazioni di amministrazione di routine, ad esempio l'aggiornamento della zona, il ricaricamento della zona, l'aggiornamento della zona, la scrittura della zona in un file o in Active Directory, la sospensione e la ripresa della zona, la cancellazione della cache, l'arresto e l'avvio del servizio DNS e la visualizzazione delle statistiche.

Il provider WMI DNS ha un set di comportamenti univoci non trovati in altri provider. Per informazioni [dettagliate sulla classe,](dns-wmi-provider-reference.md) vedere Informazioni di riferimento sul provider WMI DNS.

 

 




