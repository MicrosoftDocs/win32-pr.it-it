---
title: BITS Compact Server
description: Il server di Servizio trasferimento intelligente in background (BITS) Compact è un file server HTTP/HTTPS autonomo che consente di trasferire in modo asincrono un numero limitato di file di grandi dimensioni tra computer.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872753"
---
# <a name="bits-compact-server"></a>BITS Compact Server

Il server di Servizio trasferimento intelligente in background (BITS) Compact è un file server HTTP/HTTPS autonomo che consente di trasferire in modo asincrono un numero limitato di file di grandi dimensioni tra computer. Compact Server è compilato come servizio NT e utilizza HTTP.SYS.

BITS Compact Server è progettato per l'uso da parte dei clienti aziendali e Small Business in base alle condizioni seguenti:

-   L'utilizzo previsto è costituito da un massimo di 25 gruppi di URL e ogni gruppo di URL supporta 3 trasferimenti di file simultanei.
-   I trasferimenti di file si verificano tra computer nello stesso dominio o domini con trust reciproco.
-   I trasferimenti di file non sono destinati ai client connessi a Internet.

## <a name="installing-the-bits-compact-server"></a>Installazione di BITS Compact Server

BITS Compact Server è un componente server facoltativo. Per installare BITS Compact Server è possibile usare una delle opzioni seguenti:

-   Server Manager

-   Windows PowerShell

-   Gestione pacchetti

**Per installare BITS Compact Server utilizzando Server Manager**

1.  Nella sezione **Riepilogo funzionalità** della **Server Manager** fare clic su **Aggiungi funzionalità**.
2.  Nell'aggiunta guidata funzionalità selezionare **servizio trasferimento intelligente in background (BITS)** e **Compact Server**.
3.  Seguire le istruzioni della procedura guidata, inclusa l'installazione del software richiesto, se specificato.

Per ulteriori informazioni, vedere la Guida in linea di **Server Manager** .

**Per installare BITS Compact Server usando Windows PowerShell**

1.  Al prompt dei comandi di Windows PowerShell digitare il comando seguente: **Import-Module ServerManager**. Premere quindi INVIO.
2.  Digitare il comando seguente: **Add-WINDOWSFEATURE BITS-Compact-Server**. Premere quindi INVIO.

Nell'esempio basato su testo seguente viene illustrata l'installazione di BITS Compact Server utilizzando i cmdlet di Windows PowerShell.

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

Per informazioni sull'utilizzo dei cmdlet, vedere la documentazione di [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .

Per ulteriori informazioni sul cmdlet di Import-Module, vedere [Import-Module](/previous-versions//dd347701(v=technet.10)) nella libreria Microsoft TechNet. Per informazioni sulla riga di comando, digitare **Get-Help Import-Module**.

Per ulteriori informazioni sul cmdlet di Add-WindowsFeature, vedere [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) nella libreria Microsoft TechNet. Per informazioni sulla riga di comando, digitare **Get-Help Add-WindowsFeature**.

**Per installare BITS Compact Server tramite Gestione pacchetti**

-   Immettere il comando seguente: **PkgMgr.exe/IU: LightweightServer**.

> [!Note]  
> Le impostazioni vengono perse se il servizio Compact Server viene riavviato o se il computer viene riavviato.

 

## <a name="bits-compact-server-remote-management"></a>Gestione remota BITS Compact Server

BITS Compact Server con gestione remota BITS consente trasferimenti di file remoti più sicuri. Gestione remota BITS usa un provider Strumentazione gestione Windows (WMI) per consentire a un amministratore di sistema o a un'applicazione controller di creare in modalità remota processi di trasferimento BITS nei client e di pubblicare file per l'hosting nel server BITS Compact. Il provider BITS può essere utilizzato anche per consentire a un'applicazione di utilizzare in modalità remota il client BITS insieme a BITS Compact Server per trasferire file da un computer remoto a un altro computer remoto.

Per ulteriori informazioni, vedere la documentazione del [provider bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 