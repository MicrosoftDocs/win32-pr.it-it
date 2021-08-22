---
description: Questa sezione descrive le estensioni Winsock specifiche di Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX). Descrive anche gli aspetti delle funzioni winsock di base che richiedono considerazioni speciali o possono presentare un comportamento univoco.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Allegato WINSOCK IPX/SPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e5a97b90dc29f577bf2335b93a15fb3fb2c87c8362e0585151e1ac8b1e3393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051349"
---
# <a name="winsock-ipxspx-annex"></a>Allegato WINSOCK IPX/SPX

Questa sezione descrive le estensioni Winsock specifiche di Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX). Descrive anche gli aspetti delle funzioni winsock di base che richiedono considerazioni speciali o possono presentare un comportamento univoco.



| Elemento          | Descrizione                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome/i protocollo/i | IPX, SPX                                                                                                                                        |
| Descrizione      | Fornisce servizi di trasporto sul livello di rete IPX: IPX per datagrammi inaffidabili, SPX per flussi di messaggi affidabili e orientati alla connessione. |
| Famiglia di indirizzi   | AF \_ IPX                                                                                                                                         |
| File di intestazione      | Wsipx.h                                                                                                                                         |



 

Questa sezione illustra come usare Winsock con la famiglia di protocolli IPX, consentendo il porting delle applicazioni IPX tradizionali in Winsock. Le reti IPX funzionano in modo fondamentalmente diverso rispetto alle reti IP, pertanto è necessario considerare tali differenze quando si usa IPX/SPX.

 

 



