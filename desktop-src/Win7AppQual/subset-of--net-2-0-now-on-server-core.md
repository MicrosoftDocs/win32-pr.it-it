---
description: Subset di .NET 2.0 ora in Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Subset di .NET 2.0 ora in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6ef839f525acf190df384e3fe8394f2b785d45
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116149"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Subset di .NET 2.0 ora in Server Core

## <a name="platform"></a>Piattaforma

**Server** - Windows Server 2008 R2  



## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

L'opzione di installazione Dei componenti di base del server per Windows Server 2008 R2 include ora un subset .NET Framework 2.0. Il subset è la funzionalità di .NET 2.0 allineata alla funzionalità in Server Core. Non sono stati aggiunti file binari alla base di Server Core per consentire il funzionamento di qualsiasi parte di .NET 2.0.

L'opzione di installazione Dei componenti di base del server per Windows Server 2008 non supporta .NET.

## <a name="manifestation-of-impact"></a>Impatto significativo

In questo modo alcune applicazioni basate su .NET 2.0 possono essere eseguite in Server Core in Windows Server 2008 R2.

## <a name="testing"></a>Test

Verificare che le classi .NET utilizzate dal codice siano incluse in Server Core. Testare anche tutte le applicazioni che eseguono questo codice in Server Core.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Blog dei componenti di base del server](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *Vedere anche* la sezione Server Core di *Windows Server 2008 R2 SDK* quando diventa disponibile

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.

 

 

 
