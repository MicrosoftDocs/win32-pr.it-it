---
title: StorAHCI sostituisce MSAHCI
description: StorAHCI sostituisce MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6affffe41dd00c009ebb7bebf508dac1b63bec673c17783f594d22969822e542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932141"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI sostituisce MSAHCI

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

StorAHCI, un miniport Storport, supporta controller ADVANCED Host Controller Interface (AHCI) SATA (Serial Advanced Technology Attachment) in Windows e sostituisce MSAHCI, un miniport ATAport.

## <a name="manifestation"></a>Manifestazione

Non devono essere presenti modifiche nelle funzionalità o nelle prestazioni. questo driver supporta tutti gli stessi dispositivi supportati da MSAHCI.

Questa modifica è trasparente per l'utente.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Aggiornare le utilità e gli script che si basano sulle associazioni ATAport. Non basarsi sul nome dell'unità. Usare invece il rilevamento dei dischi standard.

 

 




