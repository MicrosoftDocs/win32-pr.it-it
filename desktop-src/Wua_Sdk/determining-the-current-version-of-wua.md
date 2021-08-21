---
description: Determinare la versione di Windows Update Agent (WUA) prima di usarla.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Determinazione della versione corrente di WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d8e013f4e8189c71b9e4510fdaebcdf1e2f749e3d8dfffd6256128e214ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049499"
---
# <a name="determining-the-current-version-of-wua"></a>Determinazione della versione corrente di WUA

Per informazioni generali sull'aggiornamento di WUA, incluse istruzioni dettagliate per determinare a livello di codice all'interno dell'app se la versione di WUA in esecuzione nel computer soddisfa le proprie esigenze, vedere Aggiornamento dell'agente di aggiornamento [Windows](updating-the-windows-update-agent.md).

Nelle versioni di Windows precedenti Windows 7 e Windows Server 2008 R2, è necessario determinare la versione installata di Windows Update Agent (WUA) prima di usarla. La versione corrente di WUA è determinata dalla versione del Wuaueng.dll in esecuzione nella sottodirectory System32 dell'installazione Windows \\ corrente. Se la versione di Wuaueng.dll è la versione 5.4.3790.1000 o successiva, viene installato WUA. Una versione precedente alla 5.4.3790.1000 indica che è installato Software Update Services (SUS) 1.0.

Quando viene effettuata una chiamata a SUS 1.0 usando l'API WUA, viene restituito un **valore HRESULT** di WU \_ E AU \_ \_ LEGACYSERVER.

È anche possibile usare il [**metodo IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) per recuperare la versione corrente del file Wuapi.dll in esecuzione in un computer. [**L'interfaccia IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) non è supportata in WUA 1.0.
