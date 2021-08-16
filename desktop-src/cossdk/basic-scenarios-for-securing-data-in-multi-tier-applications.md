---
description: Questo argomento presenta alcuni scenari predefiniti, che illustrano i criteri illustrati in Decidere dove applicare la sicurezza.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Scenari di base per la protezione dei dati in applicazioni multilivello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c4bafb0334bb9e5f124eb184f6ebf2d17f4f0dc40ef04421162dc6604f531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308743"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a>Scenari di base per la protezione dei dati in applicazioni multilivello

Questo argomento presenta alcuni scenari predefiniti, che illustrano i criteri illustrati in [Decidere dove applicare la sicurezza.](deciding-where-to-enforce-security.md)

## <a name="trusted-server-scenario"></a>Trusted Server Scenario

-   Il database considera completamente attendibile l'applicazione COM+ per autenticare e autorizzare gli utenti finali ad accedere ai dati nel database.
-   Preferibilmente, il database è protetto da qualsiasi accesso, ad eccezione dell'applicazione.
-   L'applicazione COM+ usa la sicurezza basata sui ruoli per autorizzare gli utenti.
-   Le connessioni vengono aperte con l'identità dell'applicazione COM+ e sono completamente disponibili in pool.
-   Il controllo e la registrazione possono essere evasi dall'applicazione COM+ oppure queste informazioni possono essere passate nel database dall'applicazione.

Questo scenario è ideale per i dati a cui possono accedere categorie prevedibili di utenti che possono essere incapsulati nei ruoli. Ad esempio, solo "Manager", "Tellers" e "Accountants" sono autorizzati ad accedere agli account. Nel livello intermedio viene applicata la logica di business di ogni operazione abilitata.

## <a name="impersonation-scenario"></a>Scenario di rappresentazione

-   Il database esegue l'autenticazione e l'autorizzazione degli utenti finali per limitare l'accesso ai dati nel database.
-   L'applicazione COM+ rappresenta i client ogni volta che accede al database.
-   Le connessioni vengono effettuate in base alle chiamate e non possono essere riutilizzate.

Questo scenario funziona meglio per i dati strettamente associati a classi molto piccole di utenti. Ad esempio, ogni dipendente può accedere solo al proprio file personale e ogni responsabile può accedere solo ai file del personale dei suoi report.

## <a name="hybrid-scenario"></a> Scenario ibrido

Combinazione dei due scenari precedenti, in cui la rappresentazione viene utilizzata solo quando è necessaria.

Questo scenario funziona meglio nelle situazioni in cui si hanno relazioni utente-dati ibride. Ad esempio, si dispone di "Manager", "Responsabili", "Contabili" e di migliaia di singoli client Web che possono accedere solo ai propri account. È possibile separare i percorsi logici tramite l'applicazione, potenzialmente con componenti separati, per gestire la seconda classe di utenti, in particolare quando i presupposti relativi alle prestazioni per tali utenti sono diversi.

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a>Scenario attendibile con ruoli Microsoft SQL Server attendibili

-   Microsoft SQL Server 7.0 e versioni successive possono autorizzare l'accesso a righe specifiche usando ruoli, ma considera attendibile l'applicazione COM+ per autenticare e autorizzare gli utenti ed eseguine il mapping ai ruoli corretti nel database.
-   L'applicazione COM+ autorizza gli utenti usando la sicurezza basata sui ruoli e i ruoli applicazione corrispondono bene ai ruoli del database.
-   È possibile aprire connessioni specifiche di un ruolo del database specifico. Queste connessioni possono essere riutilizzate se sono mantenute da oggetti in pool nelle applicazioni COM+. Per informazioni dettagliate su come eseguire questa operazione, vedere [Pool di oggetti COM+.](com--object-pooling.md)
-   Il controllo e la registrazione possono essere evasi dall'applicazione COM+ oppure queste informazioni possono essere passate al database dall'applicazione.

Questo scenario funziona meglio per gli stessi tipi di utenti e dati del primo scenario server attendibile perché l'applicazione COM+ è ancora ampiamente attendibile per gestire correttamente l'autorizzazione. Tuttavia, consente di proteggere il database da accessi non autorizzati consentendo al tempo stesso l'accesso potenzialmente da più origini esterne all'applicazione COM+, senza incorrere nelle penalità di scalabilità e prestazioni presenti nello scenario di rappresentazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scelta della posizione in cui applicare la sicurezza](deciding-where-to-enforce-security.md)
</dt> <dt>

[Sicurezza delle applicazioni multilivello](multi-tier-application-security.md)
</dt> </dl>

 

 



