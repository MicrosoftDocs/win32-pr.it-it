---
description: Determinare la versione di Windows Update Agent (WUA) prima di usarla.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Determinazione della versione corrente di WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309732"
---
# <a name="determining-the-current-version-of-wua"></a>Determinazione della versione corrente di WUA

Per informazioni generali sull'aggiornamento del WUA, incluse le istruzioni dettagliate per determinare a livello di codice dall'interno dell'app se la versione di WUA in esecuzione nel computer soddisfa le esigenze, vedere [aggiornamento dell'agente di Windows Update](updating-the-windows-update-agent.md).

Nelle versioni di Windows precedenti a Windows 7 e Windows Server 2008 R2, è necessario determinare la versione installata di Windows Update Agent (WUA) prima di usarla. La versione corrente di WUA è determinata dalla versione del Wuaueng.dll in esecuzione nella \\ sottodirectory System32 dell'installazione di Windows corrente. Se la versione di Wuaueng.dll è la versione 5.4.3790.1000 o successiva, WUA è installato. Una versione precedente A 5.4.3790.1000 indica che è installato software Update Services (SUS) 1,0.

Quando viene effettuata una chiamata a SUS 1,0 usando l'API WUA, viene restituito un **HRESULT** di Wu \_ E \_ au \_ LEGACYSERVER.

È anche possibile usare il metodo [**IWindowsUpdateAgentInfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) per recuperare la versione del file corrente di Wuapi.dll in esecuzione in un computer. L'interfaccia [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) non è supportata in WUA 1,0.
