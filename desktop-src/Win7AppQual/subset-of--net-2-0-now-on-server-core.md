---
description: .
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Subset di .NET 2,0 ora in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e0f836ca7afaef920429df17ef8be845ce92e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234327"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Subset di .NET 2,0 ora in Server Core

## <a name="platform"></a>Piattaforma

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

L'opzione di installazione dei componenti di base del server per Windows Server 2008 R2 include ora un subset del .NET Framework 2,0. Il subset è la funzionalità di .NET 2,0 che si allinea alla funzionalità in Server Core. Nessun file binario aggiunto alla base del server core per consentire il funzionamento di qualsiasi parte di .NET 2,0.

Non è disponibile alcun supporto .NET nell'opzione di installazione dei componenti di base del server per Windows Server 2008.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

Questo consente l'esecuzione di alcune applicazioni basate su .NET 2,0 in Server Core in Windows Server 2008 R2.

## <a name="testing"></a>Test

Verificare che le classi .NET utilizzate dal codice siano incluse in Server Core. Testare anche le applicazioni che eseguono questo codice in Server Core.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Blog sui componenti di base del server](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *Vedere anche* la sezione relativa ai componenti di base del server di *Windows Server 2008 R2 SDK* quando diventa disponibile

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

 

 

 
