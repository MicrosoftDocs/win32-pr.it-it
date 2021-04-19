---
description: L'utente può avviare un servizio con l'utilità pannello di controllo servizi. L'utente può specificare gli argomenti per il servizio nel campo parametri di avvio. Un programma di controllo del servizio può avviare un servizio e specificare i relativi argomenti con la funzione StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Avvio dei servizi su richiesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317668"
---
# <a name="starting-services-on-demand"></a>Avvio dei servizi su richiesta

L'utente può avviare un servizio con l'utilità pannello di controllo servizi. L'utente può specificare gli argomenti per il servizio nel campo **parametri di avvio** . Un programma di controllo del servizio può avviare un servizio e specificare i relativi argomenti con la funzione [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .

Quando il servizio viene avviato, SCM esegue i passaggi seguenti:

-   Recuperare le informazioni sull'account archiviate nel database.
-   Accedere all'account del servizio.
-   Caricare il profilo utente.
-   Creare il servizio nello stato Suspended.
-   Assegnare il token di accesso al processo.
-   Consente l'esecuzione del processo.

 

 



