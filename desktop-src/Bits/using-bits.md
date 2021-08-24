---
title: Uso di BITS
description: Uso di BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Servizio trasferimento intelligente in background
- Servizio trasferimento intelligente in background,attività
- BITS per il trasferimento di file
- Uso di BITS BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b301c1d96956bca924d99ef41ade3032f58dc4e194b420069cbae1071c916b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801161"
---
# <a name="using-bits"></a>Uso di BITS

La procedura seguente illustra come eseguire un trasferimento di file usando le interfacce Servizio trasferimento intelligente in background [(BITS).](bits-interfaces.md)

**Per eseguire un trasferimento di file**

1.  [Connessione al servizio BITS](connecting-to-the-bits-service.md)
2.  [Creare un processo di trasferimento](creating-a-job.md)
3.  [Aggiungere file al processo](adding-files-to-a-job.md)
4.  [Avviare il processo](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Determinare se BITS ha trasferito correttamente i file](determining-the-status-of-a-job.md)
6.  [Completare il processo](completing-and-canceling-a-job.md)

I passaggi precedenti illustrano come trasferire i file usando i valori predefiniti delle proprietà per un processo. È possibile modificare il comportamento predefinito modificando uno o più valori delle proprietà del processo. Ad esempio, è possibile modificare la priorità di elaborazione del processo rispetto ad altri processi nella coda, specificare la propria impostazione proxy e registrarsi per ricevere la notifica degli eventi quando BITS ha trasferito i file. Per altre informazioni, vedere [Impostazione e recupero delle proprietà di un processo](setting-and-retrieving-the-properties-of-a-job.md).

Windows PowerShell un meccanismo semplice per gestire molte attività BITS. Questa sezione contiene gli argomenti seguenti che illustrano come usare Windows PowerShell cmdlet con BITS:

-   [Uso di Windows PowerShell per creare processi di trasferimento di BITS](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Uso dei cmdlet Windows PowerShell WinRM per gestire i processi di trasferimento BITS](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [Uso di Windows PowerShell WMI per gestire BITS Compact Server](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> A partire da Windows 10 versione 1607, è anche possibile eseguire cmdlet di PowerShell e usare BITSAdmin o altre applicazioni che usano le interfacce [BITS](bits-interfaces.md) da una riga di comando remota di PowerShell connessa a un altro computer (fisico o virtuale). Questa funzionalità non è disponibile quando si usa una riga di comando diretta di [PowerShell](/virtualization/hyper-v-on-windows/user_guide/vmsession) a una macchina virtuale nella stessa macchina fisica e non è disponibile quando si usano i cmdlet winrm.
>
> Un processo BITS creato da una sessione remota di PowerShell verrà eseguito nel contesto dell'account utente della sessione e verrà eseguito solo quando è presente almeno una sessione di accesso locale attiva o una sessione remota di PowerShell associata a tale account utente. Per altre informazioni, vedere [Per gestire le sessioni remote di PowerShell.](using-windows-powershell-to-create-bits-transfer-jobs.md)

 

Questa sezione contiene anche gli argomenti seguenti:

-   [Procedure consigliate per l'uso di BITS](best-practices-when-using-bits.md)
-   [Enumerazione dei processi nella coda di trasferimento](enumerating-jobs-in-the-transfer-queue.md)
-   [Enumerazione dei file in un processo](enumerating-files-in-a-job.md)
-   [Gestione degli errori](handling-errors.md)
-   [Recuperare la risposta da un processo di caricamento-risposta](retrieving-the-reply-from-an-upload-reply-job.md)

Per il codice di esempio che usa le interfacce BITS, vedere [Esempi e strumenti BITS](bits-samples-and-tools.md).

 

 