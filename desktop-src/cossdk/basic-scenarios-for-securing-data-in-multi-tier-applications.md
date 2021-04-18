---
description: In questo argomento vengono illustrati alcuni scenari di blocco di compilazione, in cui vengono illustrati i criteri descritti in decidere dove applicare la protezione.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Scenari di base per la protezione dei dati nelle applicazioni multilivello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305021"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a>Scenari di base per la protezione dei dati nelle applicazioni multilivello

In questo argomento vengono illustrati alcuni scenari di blocco di compilazione, in cui vengono illustrati i criteri descritti in [decidere dove applicare la protezione](deciding-where-to-enforce-security.md).

## <a name="trusted-server-scenario"></a>Scenario server attendibile

-   Il database considera completamente attendibile l'applicazione COM+ per autenticare e autorizzare gli utenti finali ad accedere ai dati nel database.
-   Preferibilmente, il database è protetto da qualsiasi accesso, tranne che tramite l'applicazione.
-   L'applicazione COM+ utilizza la protezione basata sui ruoli per autorizzare gli utenti.
-   Le connessioni vengono aperte sotto l'identità dell'applicazione COM+ e sono completamente pool.
-   Il controllo e la registrazione possono essere eseguiti dall'applicazione COM+ oppure è possibile passare queste informazioni nel database dall'applicazione.

Questo scenario è ottimale per i dati a cui è possibile accedere da categorie stimabili di utenti che possono essere incapsulati in ruoli. Ad esempio, solo "managers", "Tellers" e "Accountants" hanno l'autorizzazione per accedere agli account. La logica di business di tutti gli elementi abilitati per l'esecuzione viene applicata al livello intermedio.

## <a name="impersonation-scenario"></a>Scenario di rappresentazione

-   Il database esegue l'autenticazione e l'autorizzazione degli utenti finali per limitare l'accesso ai dati nel database.
-   L'applicazione COM+ rappresenta i client ogni volta che accedono al database.
-   Le connessioni vengono effettuate per ogni singola chiamata e non possono essere riutilizzate.

Questo scenario funziona in modo ottimale per i dati strettamente associati a classi di utenti di dimensioni molto ridotte. Ogni dipendente può ad esempio accedere solo al proprio file personale e ogni responsabile può accedere solo ai file personali dei report.

## <a name="hybrid-scenario"></a> Scenario ibrido

Combinazione dei due scenari precedenti, in cui la rappresentazione viene utilizzata solo quando è necessario.

Questo scenario è ottimale nelle situazioni in cui si hanno relazioni ibride tra dati utente. Ad esempio, si hanno "Manager", "cassieri", "ragionieri" e migliaia di singoli client Web che possono accedere solo ai propri account. È possibile separare i percorsi logici attraverso l'applicazione, potenzialmente con componenti distinti, per gestire la seconda classe di utenti, in particolare laddove i presupposti delle prestazioni per tali utenti sono diversi.

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a>Scenario attendibile mediante ruoli di Microsoft SQL Server

-   Microsoft SQL Server 7,0 e versioni successive possono autorizzare l'accesso a righe specifiche utilizzando i ruoli, ma considera attendibile l'applicazione COM+ per autenticare e autorizzare gli utenti e per eseguirne il mapping ai ruoli corretti nel database.
-   L'applicazione COM+ autorizza gli utenti a utilizzare la protezione basata sui ruoli e i ruoli dell'applicazione corrispondono perfettamente ai ruoli del database.
-   È possibile aprire le connessioni specifiche di un particolare ruolo del database. Queste connessioni possono essere riutilizzate se vengono mantenute da oggetti in pool nelle applicazioni COM+. Per informazioni dettagliate su come eseguire questa operazione, vedere la pagina relativa al [pool di oggetti com+](com--object-pooling.md).
-   Il controllo e la registrazione possono essere eseguiti dall'applicazione COM+ oppure tali informazioni possono essere passate al database dall'applicazione.

Questo scenario funziona meglio per gli stessi tipi di utenti e dati del primo scenario server attendibile, perché l'applicazione COM+ è ancora in gran parte attendibile per gestire correttamente l'autorizzazione. Tuttavia, contribuisce a proteggere il database da accessi non autorizzati, consentendo potenzialmente l'accesso da più origini all'esterno dell'applicazione COM+, senza incorrere in problemi di scalabilità e prestazioni presenti nello scenario di rappresentazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Decidere dove applicare la protezione](deciding-where-to-enforce-security.md)
</dt> <dt>

[Sicurezza delle applicazioni a più livelli](multi-tier-application-security.md)
</dt> </dl>

 

 



