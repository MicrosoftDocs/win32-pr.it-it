---
description: All'avvio, un client seleziona un pacchetto di sicurezza per le relative transazioni con un server e quindi contatta tale server. Un server seleziona uno o più pacchetti di sicurezza e attende una connessione client.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Recupero di informazioni sui pacchetti di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626b5bf53ddc9ef20f0110dc7695a7245245604ca9e11baa3cbb50b2c1bd393f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883101"
---
# <a name="getting-information-about-security-packages"></a>Recupero di informazioni sui pacchetti di sicurezza

All'avvio, un client seleziona un pacchetto [*di*](/windows/desktop/SecGloss/s-gly) sicurezza per le relative transazioni con un server e quindi contatta tale server. Un server seleziona uno o più pacchetti di sicurezza e attende una connessione client.

Per informazioni specifiche sui pacchetti di sicurezza SSPI disponibili con un determinato SSP, è possibile chiamare la funzione [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) per recuperare [**una struttura SecPkgInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)

Per recuperare la struttura di output, il chiamante passa alla funzione l'indirizzo di un puntatore al tipo della struttura restituita. La funzione alloca memoria e restituisce i dati al chiamante assegnando l'indirizzo del buffer di dati restituito all'argomento . La convenzione SSPI è che la funzione alloca memoria per la struttura e l'applicazione chiamante libera la memoria usando [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).

La chiamata [**alla funzione QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) recupera gli attributi di un pacchetto [*di sicurezza*](/windows/desktop/SecGloss/s-gly). Sia il server che il client possono chiamare la funzione **QuerySecurityPackageInfo** per ottenere la lunghezza massima del token di sicurezza dal membro **cbMaxToken** della [**struttura SecPkgInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) Per un esempio, vedere la chiamata alla **funzione QuerySecurityPackageInfo** illustrata in [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).

Per altre informazioni sulle funzioni del pacchetto, [vedere Gestione pacchetti](authentication-functions.md).

 

 
