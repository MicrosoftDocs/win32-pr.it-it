---
description: Uso .NET Framework 4 con applicazioni compilate in versioni precedenti
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Uso .NET Framework 4 con applicazioni compilate in versioni precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c400f38efe93d2fc77d5de1f700b550f455f3e29db8ba96ef778771d82158c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994571"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Uso .NET Framework 4 con applicazioni compilate in versioni precedenti

## <a name="platform"></a>Piattaforma

 **Client** - Windows XP, Windows Vista, Windows 7  
**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Alta  






## <a name="description"></a>Descrizione

La .NET Framework 4 è altamente compatibile con le applicazioni compilate usando versioni .NET Framework precedenti. Le principali modifiche di .NET Framework 4 sono il miglioramento della sicurezza, della conformità degli standard, della correttezza, dell'affidabilità e delle prestazioni.

Tuttavia, .NET Framework 4 non usa automaticamente la versione di Common Language Runtime (CLR) per eseguire applicazioni compilate con versioni precedenti del .NET Framework.

## <a name="manifestation"></a>Manifestazione

Se è stata compilata un'applicazione usando un .NET Framework precedente e un utente apre l'applicazione in un computer in cui sono installati sia .NET Framework 4 che la versione precedente del .NET Framework, l'applicazione usa la versione precedente di CLR.

Tuttavia, se la .NET Framework 4 è l'unica versione di runtime installata nel computer, l'applicazione genera un'eccezione e chiede all'utente di installare la versione di runtime su cui è stata compilata l'applicazione.

## <a name="solution"></a>Soluzione

Per eseguire applicazioni compilate con versioni precedenti di .NET Framework con .NET Framework 4, è necessario compilare l'applicazione per la versione .NET Framework 4 specificandola nelle proprietà del progetto [**<supportedRuntime>**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in Microsoft Visual Studio oppure è possibile specificare .NET Framework 4 nell'elemento in un file di configurazione dell'applicazione.

Per altre informazioni su come eseguire la migrazione a .NET Framework 4, vedere Migration [Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) and Version Compatibility in the [.NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Test di compatibilità

Dopo aver apportato le modifiche, testare l'applicazione per assicurarsi che venga eseguita correttamente. È possibile testare la compatibilità come descritto nell'argomento [Compatibilità .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) applicazioni.

Se l'applicazione o il componente non funziona dopo l'.NET Framework 4, inviare un bug tramite il sito Web [microsoft Connessione.](https://connect.microsoft.com/visualstudio)

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [**<supportedRuntime> Elemento**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Guida di migrazione a .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Compatibilità tra le versioni in .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **.NET Framework 4 compatibilità delle applicazioni RTM:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
