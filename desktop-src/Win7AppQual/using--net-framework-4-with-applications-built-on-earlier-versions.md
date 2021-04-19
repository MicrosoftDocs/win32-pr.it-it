---
description: Uso di .NET Framework 4 con applicazioni compilate in versioni precedenti
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Uso di .NET Framework 4 con applicazioni compilate in versioni precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30eb8f4be1c50904b8d5760f456f3fe20bdd3da
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314944"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Uso di .NET Framework 4 con applicazioni compilate in versioni precedenti

## <a name="platform"></a>Piattaforma

 **Client** -Windows XP, Windows Vista, Windows 7  
**Server** : windows Server 2003, windows Server 2008, windows Server 2008 R2  


## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -alta  






## <a name="description"></a>Descrizione

Il .NET Framework 4 è altamente compatibile con le applicazioni compilate utilizzando versioni di .NET Framework precedenti. Le principali modifiche apportate al .NET Framework 4 sono migliorare la sicurezza, la conformità agli standard, la correttezza, l'affidabilità e le prestazioni.

Tuttavia, .NET Framework 4 non utilizza automaticamente la versione del Common Language Runtime (CLR) per eseguire le applicazioni compilate utilizzando versioni precedenti del .NET Framework.

## <a name="manifestation"></a>Manifestazione

Se un'applicazione è stata compilata utilizzando una .NET Framework precedente e un utente apre tale applicazione in un computer in cui sono presenti sia .NET Framework 4 che la versione precedente del .NET Framework installata, l'applicazione utilizzerà la versione CLR precedente.

Tuttavia, se il .NET Framework 4 è l'unica versione runtime installata nel computer, l'applicazione genera un'eccezione e chiede all'utente di installare la versione di runtime in cui è stata compilata l'applicazione.

## <a name="solution"></a>Soluzione

Per eseguire applicazioni compilate con versioni precedenti di .NET Framework con .NET Framework 4, è necessario compilare l'applicazione in modo che abbia come destinazione la versione .NET Framework 4 specificando il valore nelle proprietà del progetto in Microsoft Visual Studio oppure è possibile specificare .NET Framework 4 nell' [**<supportedRuntime> elemento**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in un file di configurazione dell'applicazione.

Per ulteriori informazioni su come eseguire la migrazione a .NET Framework 4, vedere la [Guida alla migrazione per la .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) e la [compatibilità tra le versioni nella .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Test di compatibilità

Dopo avere apportato le modifiche, testare l'applicazione per assicurarsi che venga eseguita correttamente. È possibile testare la compatibilità come descritto nell'argomento relativo alla [compatibilità delle applicazioni .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .

Se l'applicazione o il componente non funziona dopo l'installazione di .NET Framework 4, inviare un bug tramite il sito Web [Microsoft Connect](https://connect.microsoft.com/visualstudio) .

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [**<supportedRuntime> elemento**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Guida di migrazione a .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Compatibilità tra le versioni in .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **Procedura dettagliata per la compatibilità delle applicazioni .NET Framework 4 RTM:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
