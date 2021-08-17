---
title: Riferimenti gestiti per i comandi PowerShell di BITS
description: Servizio trasferimento intelligente in background (BITS) 4.0 può usare Windows PowerShell cmdlet per gestire i processi di trasferimento.
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7acc88c557209ed2958d06766215278e75223a1b297bd2704ca1dcba062cfed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173857"
---
# <a name="managed-reference-for-bits-powershell-commands"></a>Riferimenti gestiti per i comandi PowerShell di BITS

Servizio trasferimento intelligente in background (BITS) 4.0 può usare Windows PowerShell cmdlet per creare e gestire i processi di trasferimento e download di file.

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

Windows PowerShell cmdlet per BITS offrono gran parte delle stesse funzionalità dell'utilità della riga di comando bitsadmin. Tuttavia, Windows PowerShell esegue anche le operazioni seguenti:

-   Automatizza le attività BITS in un linguaggio di scripting estendibile e orientato alla gestione.
-   Fornisce un singolo strumento per tutte le attività correlate ai processi.

> [!Note]  
> Per usare questi comandi, è prima necessario importare il modulo PowerShell BITS usando il `Import-Module BitsTransfer` comando . Per altre informazioni, vedere l'articolo [di TechNet seguente.](/previous-versions/technet-magazine/ff382721(v=msdn.10))

 

Per altre informazioni sull'uso Windows PowerShell, [vedere Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).

## <a name="bits-powershell-classes"></a>Classi di PowerShell BITS

**Spazio** dei nomi: Microsoft.BackgroundIntelligentTransfer.Management

**Assembly**: System.Management.Automation

Queste classi di comando BITS vengono implementate da Windows PowerShell. Queste classi sono incluse in questo Software Development Kit (SDK) solo per completezza. I membri di queste classi non possono essere usati direttamente né devono essere usati per derivare altre classi.



| Classe                           | Descrizione                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AddBitsFileCommand**          | Aggiunge uno o più file a un processo di trasferimento BITS esistente.<br/> Vedere il cmdlet [Add-BitsFile](/previous-versions//dd347701(v=technet.10)) per informazioni dettagliate sui parametri e per esempi.<br/>                       |
| **ClearBitsTransferCommand**    | Annulla un processo di trasferimento BITS.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Clear-BitsTransfer.]( /previous-versions//dd347701(v=technet.10))<br/>                                          |
| **CompleteBitsTransferCommand** | Completa un processo di trasferimento BITS.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Complete-BitsTransfer.]( /previous-versions//dd347701(v=technet.10))<br/>                                     |
| **GetBitsTransferCommand**      | Recupera l'oggetto BitsJob associato per un processo di trasferimento BITS esistente.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Get-BitsTransfer.](/previous-versions//dd347701(v=technet.10))<br/> |
| **NewBitsTransferCommand**      | Crea un nuovo processo di trasferimento BITS.<br/> Vedere il cmdlet [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) per informazioni dettagliate sui parametri e per esempi.<br/>                                           |
| **ResumeBitsTransferCommand**   | Riprende un processo di trasferimento BITS.<br/> Vedere il cmdlet [Resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) per informazioni dettagliate sui parametri e per esempi.<br/>                                            |
| **SetBitsTransferCommand**      | Modifica le proprietà di un processo di trasferimento BITS esistente.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Set-BitsTransfer.](/previous-versions//dd347701(v=technet.10))<br/>                  |
| **SuspendBitsTransferCommand**  | Sospende un processo di trasferimento BITS.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Suspend-BitsTransfer.](/previous-versions//dd347701(v=technet.10))<br/>                                          |



 

 

