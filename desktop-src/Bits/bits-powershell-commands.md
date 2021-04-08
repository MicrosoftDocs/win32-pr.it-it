---
title: Riferimenti gestiti per i comandi PowerShell di BITS
description: Servizio trasferimento intelligente in background (BITS) 4,0 può utilizzare i cmdlet di Windows PowerShell per gestire i processi di trasferimento.
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bd195d2202849c2bf2df580d159ee401911c51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872750"
---
# <a name="managed-reference-for-bits-powershell-commands"></a>Riferimenti gestiti per i comandi PowerShell di BITS

Servizio trasferimento intelligente in background (BITS) 4,0 può utilizzare i cmdlet di Windows PowerShell per creare e gestire i processi di download e caricamento dei file.

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

I cmdlet di Windows PowerShell per BITS forniscono gran parte delle funzionalità dell'utilità della riga di comando Bitsadmin. Tuttavia, Windows PowerShell esegue anche le operazioni seguenti:

-   Automatizza le attività BITS in un linguaggio di scripting estendibile e orientato alla gestione.
-   Fornisce un unico strumento per tutte le attività correlate ai processi.

> [!Note]  
> Per usare questi comandi, è necessario prima importare il modulo PowerShell BITS, usando il `Import-Module BitsTransfer` comando. Per ulteriori informazioni, vedere l' [articolo TechNet](/previous-versions/technet-magazine/ff382721(v=msdn.10))seguente.

 

Per ulteriori informazioni sull'utilizzo di Windows PowerShell, vedere [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).

## <a name="bits-powershell-classes"></a>Classi PowerShell BITS

**Spazio dei nomi**: Microsoft. BackgroundIntelligentTransfer. Management

**Assembly**: System. Management. Automation

Queste classi di comandi BITS sono implementate da Windows PowerShell. Queste classi sono incluse in questo Software Development Kit (SDK) solo per completezza. I membri di queste classi non possono essere usati direttamente, né devono essere usati per derivare altre classi.



| Classe                           | Descrizione                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AddBitsFileCommand**          | Aggiunge uno o più file a un processo di trasferimento BITS esistente.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Add-BitsFile](/previous-versions//dd347701(v=technet.10)) .<br/>                       |
| **ClearBitsTransferCommand**    | Annulla un processo di trasferimento BITS.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Clear-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .<br/>                                          |
| **CompleteBitsTransferCommand** | Completa un processo di trasferimento BITS.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .<br/>                                     |
| **GetBitsTransferCommand**      | Recupera l'oggetto BitsJob associato per un processo di trasferimento BITS esistente.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Get-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/> |
| **NewBitsTransferCommand**      | Crea un nuovo processo di trasferimento BITS.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                                           |
| **ResumeBitsTransferCommand**   | Riprende un processo di trasferimento BITS.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                                            |
| **SetBitsTransferCommand**      | Modifica le proprietà di un processo di trasferimento BITS esistente.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [set-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                  |
| **SuspendBitsTransferCommand**  | Sospende un processo di trasferimento BITS.<br/> Per informazioni dettagliate sui parametri e per esempi, vedere il cmdlet [Suspend-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                                          |



 

 

