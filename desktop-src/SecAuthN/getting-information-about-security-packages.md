---
description: Quando viene avviato, un client seleziona un pacchetto di sicurezza per le transazioni con un server e quindi contatta tale server. Un server seleziona uno o più pacchetti di sicurezza ed è in attesa di una connessione client.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Ottenere informazioni sui pacchetti di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129923"
---
# <a name="getting-information-about-security-packages"></a>Ottenere informazioni sui pacchetti di sicurezza

Quando viene avviato, un client seleziona un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) per le transazioni con un server e quindi contatta tale server. Un server seleziona uno o più pacchetti di sicurezza ed è in attesa di una connessione client.

Per informazioni specifiche sui pacchetti di sicurezza SSPI disponibili con un particolare SSP, è possibile chiamare la funzione [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) per recuperare una struttura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .

Per recuperare la struttura di output, il chiamante passa alla funzione l'indirizzo di un puntatore al tipo della struttura restituita. La funzione alloca memoria e restituisce i dati al chiamante assegnando l'indirizzo del buffer dei dati restituiti all'argomento. La convenzione SSPI è che la funzione alloca memoria per la struttura e l'applicazione chiamante libera tale memoria utilizzando [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).

La chiamata della funzione [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) recupera gli attributi di un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly). Sia il server che il client possono chiamare la funzione **QuerySecurityPackageInfo** per ottenere la lunghezza massima del token di sicurezza dal membro **CbMaxToken** della struttura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) . Per un esempio, vedere la chiamata alla funzione **QuerySecurityPackageInfo** illustrata in [uso di SSPI con un server Windows Sockets](using-sspi-with-a-windows-sockets-server.md).

Per ulteriori informazioni sulle funzioni del pacchetto, vedere [Gestione pacchetti](authentication-functions.md).

 

 
