---
description: I provider di associazioni Windows client di Strumentazione gestione Windows (WMI) per attraversare e recuperare profili e istanze di classe associate da spazi dei nomi diversi.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Accesso ai dati nello spazio dei nomi di interoperabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855d3c302ca4af5381e1f0794abd643d19615dec2009740d1276698aba785d8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109645"
---
# <a name="accessing-data-in-the-interop-namespace"></a>Accesso ai dati nello spazio dei nomi di interoperabilità

I provider di associazioni Windows client di Strumentazione gestione Windows (WMI) per attraversare e recuperare profili e istanze di classe associate da spazi dei nomi diversi.

I provider e le classi di associazione si trovano nello spazio \\ \\ dei nomi di \\ interoperabilità radice. Per altre informazioni, vedere [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) e [Writing an Association Provider](writing-an-association-provider-for-interop.md).

I provider di associazioni espongono profili standard, ad esempio un profilo di alimentazione. Gli esempi seguenti usano il profilo di alimentazione per illustrare come individuare e accedere ai dati tramite lo spazio dei nomi di interoperabilità .

Windows PowerShell un meccanismo semplice per attraversare l'associazione appropriata, recuperare un profilo di dispositivo e chiamare un metodo.

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>Enumerazione dei profili nello spazio dei nomi root/interop

Il comando Windows PowerShell seguente enumera i profili supportati dalla[DmTF](https://www.dmtf.org/standards/wsman)(Distributed Management Task Force) in un computer Windows 7:


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>Recupero di istanze di un profilo di dispositivo specifico

Il comando Windows PowerShell seguente restituisce tutte le istanze di un profilo specificato tramite [**CIM \_ RegisteredProfile:**](/previous-versions//ee309375(v=vs.85))


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>Assegnazione del profilo di alimentazione a una variabile

Il comando Windows PowerShell seguente assegna l'istanza del profilo di alimentazione a una variabile:


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>Enumerazione delle combinazioni per il risparmio di energia in un computer

Il comando Windows PowerShell seguente enumera le combinazioni per il profilo di risparmio energia disponibili:


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>Chiamata di un metodo

Il comando Windows PowerShell seguente chiama il [**metodo Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) per la combinazione per il risparmio di energia:


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attraversamento dell'associazione tra spazi dei nomi](cross-namespace-association-traversal.md)
</dt> <dt>

[Scrittura di un provider di associazioni](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**Win32 \_ PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
