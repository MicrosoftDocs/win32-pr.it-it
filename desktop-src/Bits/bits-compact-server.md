---
title: BITS Compact Server
description: Il Servizio trasferimento intelligente in background (BITS) Compact Server è un file server HTTP/HTTPS autonomo che consente di trasferire in modo asincrono un numero limitato di file di grandi dimensioni tra computer.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41cfbc18a8dc06bb474ab8df9df85fb7b8a96838db14bbc18aee4d94881985d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529191"
---
# <a name="bits-compact-server"></a>BITS Compact Server

Il Servizio trasferimento intelligente in background (BITS) Compact Server è un file server HTTP/HTTPS autonomo che consente di trasferire in modo asincrono un numero limitato di file di grandi dimensioni tra computer. Compact Server è compilato come servizio NT e usa HTTP.SYS.

BITS Compact Server è destinato all'uso da parte dei clienti aziendali e di piccole imprese nelle condizioni seguenti:

-   L'utilizzo previsto è un massimo di 25 gruppi di URL e ogni gruppo di URL supporta 3 trasferimenti di file simultanei.
-   I trasferimenti di file vengono eseguiti tra computer nello stesso dominio o domini reciprocamente attendibili.
-   I trasferimenti di file non sono destinati ai client con connessione Internet.

## <a name="installing-the-bits-compact-server"></a>Installazione di BITS Compact Server

BITS Compact Server è un componente server facoltativo. È possibile usare una delle opzioni seguenti per installare BITS Compact Server:

-   Server Manager

-   Windows PowerShell

-   Gestione pacchetti

**Per installare BITS Compact Server usando Server Manager**

1.  Nella sezione **Riepilogo funzionalità del** Server Manager fare clic su Aggiungi **funzionalità**. 
2.  Nell'Aggiunta guidata funzionalità selezionare **Servizio trasferimento intelligente in background (BITS)** e **Compact Server**.
3.  Seguire le istruzioni della procedura guidata, inclusa l'installazione del software necessario, se indicato.

Per altre informazioni, vedere la Guida **Server Manager** online.

**Per installare BITS Compact Server usando Windows PowerShell**

1.  In un Windows PowerShell comando digitare il comando seguente: **Import-Module ServerManager**. Premere quindi INVIO.
2.  Digitare il comando seguente: **Add-WindowsFeature BITS-Compact-Server**. Premere quindi INVIO.

L'esempio basato su testo seguente illustra l'installazione di BITS Compact Server usando Windows PowerShell cmdlet.

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

Per informazioni sull'uso dei cmdlet, vedere la [documentazione Windows PowerShell.](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx)

Per altre informazioni sul cmdlet Import-Module, vedere [Import-Module](/previous-versions//dd347701(v=technet.10)) in Microsoft TechNet Library. Per informazioni sulla riga di comando, digitare **get-help import-module**.

Per altre informazioni sul cmdlet Add-WindowsFeature, vedere [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) in Microsoft TechNet Library. Per informazioni sulla riga di comando, digitare **get-help Add-WindowsFeature**.

**Per installare BITS Compact Server usando Gestione pacchetti**

-   Immettere il comando seguente: **PkgMgr.exe /iu:LightweightServer**.

> [!Note]  
> Le impostazioni vengono perse se il servizio Compact Server viene riavviato o se il computer viene riavviato.

 

## <a name="bits-compact-server-remote-management"></a>Gestione remota di BITS Compact Server

BITS Compact Server con gestione remota BITS consente trasferimenti di file remoti più sicuri. Gestione remota BITS usa un provider wmi (Windows Management Instrumentation) per consentire a un amministratore di sistema o a un'applicazione controller di creare in remoto processi di trasferimento BITS nei client e di pubblicare file per l'hosting in BITS Compact Server. Il provider BITS può essere usato anche per consentire a un'applicazione di usare in remoto il client BITS insieme a BITS Compact Server per trasferire file da un computer remoto a un altro computer remoto.

Per altre informazioni, vedere la documentazione [del provider BITS.](/previous-versions/windows/desktop/bitsprov/bits-provider)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 