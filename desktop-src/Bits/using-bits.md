---
title: Uso di BITS
description: Uso di BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Servizio trasferimento intelligente in background
- Servizio trasferimento intelligente in background, attività
- BIT di trasferimento di file
- Uso di bit BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300346"
---
# <a name="using-bits"></a>Uso di BITS

Nei passaggi seguenti viene illustrato come eseguire un trasferimento di file utilizzando le  [interfacce](bits-interfaces.md)servizio trasferimento intelligente in background (BITS).

**Per eseguire un trasferimento di file**

1.  [Connettersi al servizio BITS](connecting-to-the-bits-service.md)
2.  [Creazione di un processo di trasferimento](creating-a-job.md)
3.  [Aggiungere file al processo](adding-files-to-a-job.md)
4.  [Avviare il processo](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Determinare se i BITS hanno trasferito correttamente i file](determining-the-status-of-a-job.md)
6.  [Completare il processo](completing-and-canceling-a-job.md)

I passaggi precedenti illustrano come trasferire file usando i valori di proprietà predefiniti per un processo. È possibile modificare il comportamento predefinito modificando uno o più valori di proprietà del processo. È ad esempio possibile modificare la priorità in base alla quale il processo viene elaborato rispetto ad altri processi nella coda, specificare l'impostazione del proxy e registrarsi per ricevere la notifica degli eventi quando i file vengono trasferiti da BITS. Per ulteriori informazioni, vedere [impostazione e recupero delle proprietà di un processo](setting-and-retrieving-the-properties-of-a-job.md).

Windows PowerShell fornisce un meccanismo semplice per gestire molte attività BITS. Questa sezione contiene gli argomenti seguenti che illustrano come usare i cmdlet di Windows PowerShell con BITS:

-   [Uso di Windows PowerShell per creare processi di trasferimento di BITS](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Utilizzo dei cmdlet di Windows PowerShell per WinRM per gestire i processi di trasferimento BITS](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [Uso dei cmdlet di Windows PowerShell per WMI per gestire BITS Compact Server](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> A partire da Windows 10, versione 1607, è anche possibile eseguire i cmdlet di PowerShell e usare BITSAdmin o altre applicazioni che usano le [interfacce](bits-interfaces.md) BITS da una riga di comando remota di PowerShell connessa a un altro computer (fisico o virtuale). Questa funzionalità non è disponibile quando si usa una riga di comando di [PowerShell diretta](/virtualization/hyper-v-on-windows/user_guide/vmsession) in una macchina virtuale nello stesso computer fisico e non è disponibile quando si usano i cmdlet WinRM.
>
> Un processo BITS creato da una sessione remota di PowerShell verrà eseguito nel contesto dell'account utente della sessione e verrà eseguito solo quando esiste almeno una sessione di accesso locale attiva o una sessione remota di PowerShell associata a tale account utente. Per altre informazioni, vedere [per gestire le sessioni remote di PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).

 

Questa sezione contiene anche gli argomenti seguenti:

-   [Procedure consigliate per l'uso di BITS](best-practices-when-using-bits.md)
-   [Enumerazione dei processi nella coda di trasferimento](enumerating-jobs-in-the-transfer-queue.md)
-   [Enumerazione dei file in un processo](enumerating-files-in-a-job.md)
-   [Gestione degli errori](handling-errors.md)
-   [Recuperare la risposta da un processo di caricamento-risposta](retrieving-the-reply-from-an-upload-reply-job.md)

Per il codice di esempio che usa le interfacce BITS, vedere [esempi e strumenti bits](bits-samples-and-tools.md).

 

 