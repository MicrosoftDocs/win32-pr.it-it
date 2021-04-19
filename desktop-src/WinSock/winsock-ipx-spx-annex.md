---
description: In questa sezione vengono descritte le estensioni Winsock specifiche di Internet-Packet Exchange/Sequenced Packet Exchange (IPX/SPX). Vengono inoltre descritti gli aspetti delle funzioni Winsock di base che richiedono una particolare attenzione oppure possono presentare un comportamento univoco.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Winsock IPX/SPX Annex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308861"
---
# <a name="winsock-ipxspx-annex"></a>Winsock IPX/SPX Annex

In questa sezione vengono descritte le estensioni Winsock specifiche di Internet-Packet Exchange/Sequenced Packet Exchange (IPX/SPX). Vengono inoltre descritti gli aspetti delle funzioni Winsock di base che richiedono una particolare attenzione oppure possono presentare un comportamento univoco.



| Elemento          | Descrizione                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome/i protocollo | IPX, SPX                                                                                                                                        |
| Descrizione      | Fornisce servizi di trasporto sul livello di rete IPX: IPX per datagrammi non affidabili, SPX per flussi di messaggi affidabili e orientati alla connessione. |
| Famiglia di indirizzi   | \_IPX AF                                                                                                                                         |
| File di intestazione      | WSIPX. h                                                                                                                                         |



 

In questa sezione viene illustrato come utilizzare Winsock con la famiglia di protocolli IPX, consentendo il trasferimento di applicazioni IPX tradizionali in Winsock. Le reti IPX operano in modo sostanzialmente diverso rispetto alle reti IP, pertanto è necessario considerare tali differenze quando si utilizza IPX/SPX.

 

 



