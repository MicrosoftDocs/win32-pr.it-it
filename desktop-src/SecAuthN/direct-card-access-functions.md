---
description: Utilizzando il sottosistema Smart Card, è possibile comunicare con schede che potrebbero non essere conformi alle specifiche ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funzioni di accesso diretto alle schede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878629"
---
# <a name="direct-card-access-functions"></a>Funzioni di accesso diretto alle schede

Utilizzando il sottosistema [*Smart Card*](/windows/desktop/SecGloss/s-gly) , è possibile comunicare con schede che potrebbero non essere conformi alle specifiche ISO 7816. A tale scopo, le funzioni seguenti consentono di controllare gli attributi delle comunicazioni tra l'applicazione e la scheda fornendo una manipolazione diretta di basso livello del [*lettore*](/windows/desktop/SecGloss/r-gly).

Per usare queste funzioni, è necessario specificare un identificatore per l'attributo in questione. Per gli identificatori e i valori validi per gli attributi, vedere la tabella 3-1 in *requisiti per i dispositivi di interfaccia PC-Connected*.



| Argomento                                    | Descrizione                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Fornire il controllo diretto del lettore. |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Ottiene gli attributi del lettore.                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Imposta attributo Reader.                 |



 

 

 
