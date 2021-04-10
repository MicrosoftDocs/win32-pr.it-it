---
title: Uso dei cmdlet di Windows PowerShell per WMI per gestire BITS Compact Server
description: Windows PowerShell fornisce un meccanismo semplice per connettersi a Strumentazione gestione Windows (WMI) in un computer remoto e gestire il server di Servizio trasferimento intelligente in background (BITS) Compact.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963252"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>Uso dei cmdlet di Windows PowerShell per WMI per gestire BITS Compact Server

Windows PowerShell fornisce un meccanismo semplice per connettersi a Strumentazione gestione Windows (WMI) in un computer remoto e gestire il server di Servizio trasferimento intelligente in background (BITS) Compact. BITS Compact Server è un componente server facoltativo che deve essere installato separatamente. Per informazioni sull'installazione di Compact Server, vedere la documentazione di [BITS Compact Server](bits-compact-server.md) .

1.  Connettersi al provider BITS.

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    Il cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) richiede le credenziali dell'utente per connettersi al computer remoto e assegna le credenziali all'oggetto $cred.

    Gli oggetti restituiti dal cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) vengono assegnati alla variabile $BCS. Nell'esempio precedente, il cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) recupera la classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) nello \\ \\ spazio dei nomi Microsoft bits radice di Server1. I metodi statici esposti dalla classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) possono essere chiamati sull'oggetto $BCS. Per ulteriori informazioni sulla gestione remota BITS, vedere classi del [provider bits e](/previous-versions/windows/desktop/bitsprov/bits-provider) del [provider bits]( /previous-versions//dd904507(v=vs.85)).

    > [!Note]  
    > Il carattere di accento grave ( \` ) viene usato per indicare un'interruzioni di riga.

     

2.  Creare un gruppo di URL nel server.

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    La https://Server1:80/testurlgroup stringa del prefisso URL "" viene assegnata alla variabile $URLGroup. La variabile $URLGroup viene passata al metodo [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , che crea il gruppo di URL in Server1.

    È possibile specificare un gruppo di URL diverso. Il gruppo di URL deve essere conforme a una stringa di prefisso URL valida. Per ulteriori informazioni sui prefissi URL, vedere [URLPrefix Strings](../http/urlprefix-strings.md).

3.  Ospitare un file nel gruppo di URL.

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    L'istanza di BITSCompactServerUrlGroup restituita dal cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) viene assegnata alla variabile $bcsObj. Il metodo [CreateURL](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) viene chiamato per il $bcsObj con il suffisso "url.txt" URL, il \\ \\ percorso di origine "c: temp \\ \\1.txt" per il file e una stringa del descrittore di sicurezza vuota come parametri. Il suffisso "url.txt" viene aggiunto al prefisso del gruppo di URL. I client possono scaricare il file dall'indirizzo seguente: https://Server1:80/testurlgroup/url.txt .

4.  Pulire l'URL e il gruppo di URL.

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    Il metodo **System. Object Delete** Elimina l'oggetto $bcsObj.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[BITS Compact Server](./bits-compact-server.md)
</dt> <dt>

[Provider BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[Classi del provider BITS]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 