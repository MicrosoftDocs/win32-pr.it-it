---
title: StorAHCI sostituisce MSAHCI
description: StorAHCI sostituisce MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300572"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI sostituisce MSAHCI

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

StorAHCI, un Storport miniport, supporta i controller AHCI (Advanced Host Controller Interface) SATA (Serial Advanced Technology Attachment) in Windows e sostituisce MSAHCI, un miniport ATAport.

## <a name="manifestation"></a>Manifestazione

Non devono essere apportate modifiche alle funzionalità e alle prestazioni. Questo driver supporta tutti gli stessi dispositivi supportati da MSAHCI.

Questa modifica è trasparente per l'utente.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Aggiornare tutte le utilità e gli script basati sui binding ATAport. Non fare affidamento sul nome dell'unità. Usare invece il rilevamento del disco standard.

 

 




