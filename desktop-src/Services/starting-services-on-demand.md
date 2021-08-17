---
description: L'utente può avviare un servizio con l'utilità del Pannello di controllo Servizi. L'utente può specificare gli argomenti per il servizio nel campo Parametri di avvio. Un programma di controllo del servizio può avviare un servizio e specificarne gli argomenti con la funzione StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Avvio di servizi su richiesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3762721eaeaea32d42da729f57c0753b18fb951cb57ad091aa697c144df0de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888467"
---
# <a name="starting-services-on-demand"></a>Avvio di servizi su richiesta

L'utente può avviare un servizio con l'utilità del Pannello di controllo Servizi. L'utente può specificare gli argomenti per il servizio nel **campo Parametri di** avvio. Un programma di controllo del servizio può avviare un servizio e specificarne gli argomenti con la [**funzione StartService.**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)

Quando il servizio viene avviato, Gestione controllo servizi esegue la procedura seguente:

-   Recuperare le informazioni sull'account archiviate nel database.
-   Accedere all'account del servizio.
-   Caricare il profilo utente.
-   Creare il servizio nello stato sospeso.
-   Assegnare il token di accesso al processo.
-   Consentire l'esecuzione del processo.

 

 



