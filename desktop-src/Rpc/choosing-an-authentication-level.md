---
title: Scelta di un livello di autenticazione
description: Quando si sceglie un livello di autenticazione, attenersi alle linee guida seguenti.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471150"
---
# <a name="choosing-an-authentication-level"></a>Scelta di un livello di autenticazione

Quando si sceglie un livello di autenticazione, attenersi alle linee guida seguenti. Se non è rilevante se i dati inviati possono essere intercettati e modificati e i dati ricevuti possono essere intercettati o modificati, utilizzare \_ il livello di autenticazione di RPC C \_ \_ \_ None, che è l'impostazione predefinita. Se i dati non devono essere modificati e i dati privati non vengono inviati né ricevuti, utilizzare l' \_ \_ integrità PKT del livello auth C RPC \_ \_ \_ . In tutti gli altri casi, usare \_ il \_ livello di autenticazione Pkt di RPC C \_ \_ \_ .

Non usare l' \_ impostazione predefinita del livello auth c RPC, la connessione del livello auth c \_ \_ \_ RPC \_ , la \_ chiamata al \_ \_ \_ \_ livello auth c RPC o il \_ \_ \_ \_ livello auth c \_ \_ PKT. Un utente malintenzionato sofisticato può interrompere questi livelli di autenticazione e renderli inefficaci. Ognuno di questi livelli rende leggermente più difficile per un utente malintenzionato intercettare e modificare i dati e per rappresentare, ma la sicurezza non viene realmente realizzata. Poiché il livello di sofisticazione di un utente malintenzionato è raramente noto, questi non sono scelte ottimali.

 

 




