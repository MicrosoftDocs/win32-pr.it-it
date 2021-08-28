---
description: Uso .NET Framework 4 con applicazioni compilate in versioni precedenti
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Uso .NET Framework 4 con applicazioni compilate in versioni precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12eb34b00cfe14a18e83e7726f1ffa962ba03f8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884743"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Uso .NET Framework 4 con applicazioni compilate in versioni precedenti

## <a name="platform"></a>Piattaforma

 **Client** - Windows XP, Windows Vista, Windows 7  
**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Alta  






## <a name="description"></a>Descrizione

Il .NET Framework 4 è altamente compatibile con le applicazioni compilate usando versioni .NET Framework precedenti. Le principali modifiche in .NET Framework 4 sono il miglioramento della sicurezza, della conformità agli standard, della correttezza, dell'affidabilità e delle prestazioni.

Tuttavia, .NET Framework 4 non usa automaticamente la versione di Common Language Runtime (CLR) per eseguire applicazioni compilate usando versioni precedenti del .NET Framework.

## <a name="manifestation"></a>Manifestazione

Se è stata compilata un'applicazione usando un .NET Framework precedente e un utente apre l'applicazione in un computer in cui sono installati sia .NET Framework 4 che la versione precedente del .NET Framework, l'applicazione usa la versione precedente di CLR.

Tuttavia, se il .NET Framework 4 è l'unica versione di runtime installata nel computer, l'applicazione genera un'eccezione e chiede all'utente di installare la versione di runtime su cui è stata compilata l'applicazione.

## <a name="solution"></a>Soluzione

Per eseguire applicazioni compilate con versioni precedenti di .NET Framework con .NET Framework 4, è necessario compilare l'applicazione per la versione .NET Framework 4 specificandola nelle proprietà del progetto in Microsoft Visual Studio oppure è possibile specificare .NET Framework 4 nell'elemento [**&lt; supportedRuntime &gt;**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in un file di configurazione dell'applicazione.

Per altre informazioni su come eseguire la migrazione a .NET Framework 4, vedere Migration Guide to the .NET Framework 4 (Guida alla migrazione a [.NET Framework 4)](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) e Version Compatibility [(Compatibilità delle versioni) .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Test di compatibilità

Dopo aver apportato le modifiche, testare l'applicazione per assicurarsi che venga eseguita correttamente. È possibile testare la compatibilità come descritto nell'.NET Framework Compatibilità delle applicazioni [di .NET Framework 4.](/previous-versions/dd889541(v=msdn.10))

Se l'applicazione o il componente non funziona dopo .NET Framework 4, inviare un bug tramite il sito Web [di Microsoft Connessione.](https://connect.microsoft.com/visualstudio)

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [**&lt;elemento &gt; supportedRuntime**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Guida di migrazione a .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Compatibilità tra le versioni in .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **.NET Framework 4 RTM Application Compatibility Walkthrough:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
