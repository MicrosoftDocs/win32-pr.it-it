---
description: Usando il sottosistema smart card, è possibile comunicare con schede che potrebbero non essere conformi alle specifiche ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funzioni di accesso diretto alle schede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72b606cd766ea9a8930599bd2a44e117dea0bffdef6474c038b39294c08acf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008459"
---
# <a name="direct-card-access-functions"></a>Funzioni di accesso diretto alle schede

Usando il [*sottosistema smart card,*](/windows/desktop/SecGloss/s-gly) è possibile comunicare con schede che potrebbero non essere conformi alle specifiche ISO 7816. A tale scopo, le funzioni seguenti consentono di controllare gli attributi delle comunicazioni tra l'applicazione e la scheda fornendo una manipolazione diretta e di basso livello del [*lettore*](/windows/desktop/SecGloss/r-gly).

Per usare queste funzioni, è necessario fornire un identificatore per l'attributo in questione. Per gli identificatori e i valori di attributo validi, vedere la tabella 3-1 in *Requisiti per PC-Connected dispositivi dell'interfaccia*.



| Argomento                                    | Descrizione                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Fornire il controllo diretto del lettore. |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Ottenere gli attributi del lettore.                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Impostare l'attributo reader.                 |



 

 

 
