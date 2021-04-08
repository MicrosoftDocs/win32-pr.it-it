---
description: I provider di associazioni consentono ai client di Strumentazione gestione Windows (WMI) di attraversare e recuperare i profili e le istanze di classe associate da spazi dei nomi diversi.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Accesso ai dati nello spazio dei nomi Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968370"
---
# <a name="accessing-data-in-the-interop-namespace"></a>Accesso ai dati nello spazio dei nomi Interop

I provider di associazioni consentono ai client di Strumentazione gestione Windows (WMI) di attraversare e recuperare i profili e le istanze di classe associate da spazi dei nomi diversi.

I provider di associazioni e le classi si trovano nello \\ \\ \\ spazio dei nomi di interoperabilità radice. Per ulteriori informazioni, vedere attraversamento dell' [associazione tra spazi dei nomi](cross-namespace-association-traversal.md) e [scrittura di un provider di associazioni](writing-an-association-provider-for-interop.md).

I provider di associazioni espongono i profili standard, ad esempio un profilo di alimentazione. Gli esempi seguenti usano il profilo Power per illustrare come individuare e accedere ai dati tramite lo spazio dei nomi Interop.

Windows PowerShell fornisce un meccanismo semplice per attraversare l'associazione appropriata, recuperare un profilo di dispositivo e chiamare un metodo.

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>Enumerazione di profili nello spazio dei nomi radice/interoperabilità

Il comando di Windows PowerShell seguente enumera i profili supportati da Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) in un computer Windows 7:


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>Recupero di istanze di un profilo di dispositivo specifico

Il comando di Windows PowerShell seguente restituisce tutte le istanze di un profilo specificato tramite [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)):


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>Assegnazione del profilo di alimentazione a una variabile

Con il comando di Windows PowerShell seguente viene assegnata l'istanza del profilo Power a una variabile:


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>Enumerazione delle combinazioni per il risparmio di energia in un computer

Il comando di Windows PowerShell seguente enumera i piani di Power profile disponibili:


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>Chiamata di un metodo

Il seguente comando di Windows PowerShell chiama il metodo [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) per la combinazione per il risparmio di energia:


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attraversamento dell'associazione tra spazi dei nomi](cross-namespace-association-traversal.md)
</dt> <dt>

[Scrittura di un provider di associazioni](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**\_PowerPlan Win32**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
