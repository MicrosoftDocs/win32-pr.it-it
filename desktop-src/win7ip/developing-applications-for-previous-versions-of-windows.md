---
title: Sviluppo di applicazioni per versioni precedenti di Windows
description: Illustra le operazioni da eseguire per sviluppare applicazioni eseguite in versioni precedenti di Windows e sfruttare i vantaggi offerti dall'API supportata con l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104401844"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Sviluppo di applicazioni per versioni precedenti di Windows

Illustra le operazioni da eseguire per sviluppare applicazioni eseguite in versioni precedenti di Windows e sfruttare i vantaggi offerti dall'API supportata con l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.

## <a name="required-downloads"></a>Download necessari

Il download e l'installazione dei pacchetti descritti nelle sezioni seguenti sono necessari se si desidera sviluppare applicazioni che utilizzano API introdotte con Microsoft Windows Software Development Kit (SDK) per Windows 7.

### <a name="microsoft-windows-sdk"></a>Microsoft Windows SDK

Il Windows SDK per Windows 7 è necessario per la creazione di applicazioni che usano le API supportate con l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.

Per accedere a risorse e informazioni aggiuntive, ad esempio download, post del forum e il Blog del team di Windows SDK, vedere il [centro per sviluppatori di Windows SDK](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

Il .NET Framework 3,5 Service Pack 1 è necessario per la creazione di applicazioni che utilizzano le API supportate dall'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.

Per ulteriori risorse e informazioni, vedere il [centro per sviluppatori .NET Framework](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>DirectX SDK è necessario quando si usa Direct3D

Se si creano applicazioni che usano Direct3D, [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) è necessario per la creazione di applicazioni che usano le API supportate dall'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="update-your-development-computer"></a>Aggiornare il computer di sviluppo

Verificare che nel computer di sviluppo siano disponibili tutti gli aggiornamenti più recenti da Windows Update.

Se si sviluppano applicazioni in una versione precedente di Windows, è necessario ottenere l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 da Windows Update. L'installazione di uno di questi aggiornamenti consentirà di sfruttare la nuova API fornita dalla Windows SDK per Windows 7.

Per ulteriori informazioni su come ottenere gli aggiornamenti da Windows Update, vedere l' [articolo della Knowledge base sull'aggiornamento della piattaforma per Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Ambiente di sviluppo

### <a name="set-the-build-target-to-windows-7"></a>Impostare la destinazione di compilazione su Windows 7

Tutte le applicazioni che utilizzano le librerie nell'aggiornamento della piattaforma per Windows Vista devono essere compilate con la piattaforma di destinazione di Windows 7.

L'impostazione di WINVER sul valore della piattaforma di destinazione Windows 7 consente di sviluppare applicazioni che utilizzano API supportate con l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 in un computer di sviluppo che esegue Windows Vista.

È possibile impostare la piattaforma di destinazione su Windows 7 nel codice sorgente o usando l'opzione/D con il compilatore di Visual Studio.

Nell'esempio seguente viene illustrato come impostare WINVER nel codice sorgente.


```C++
#define WINVER 0x0601
```



Nell'esempio seguente viene illustrato come impostare WINVER utilizzando l'opzione del compilatore/D.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Distribuzione dell'applicazione

Se si compila l'applicazione usando le intestazioni e le librerie fornite dal Windows SDK per Windows 7, le API supportate vengono eseguite in qualsiasi versione di Windows con aggiornamento della piattaforma per Windows Vista o aggiornamento della piattaforma per Windows Server 2008 installato.

> [!Note]  
> Il comportamento, le prestazioni o i requisiti per alcune API supportate con l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono variare nelle diverse versioni di Windows. Per informazioni dettagliate su un'API specifica supportata dagli aggiornamenti, vedere [informazioni sull'aggiornamento della piattaforma per Windows Vista](platform-update-for-windows-vista-overview.md).

 

### <a name="no-redistributable-components"></a>Nessun componente ridistribuibile

Non è necessario che l'applicazione installi componenti ridistribuibili, ad esempio dll o altri file di run-time.

### <a name="requires-updated-end-user-computer"></a>Richiede il computer End-User aggiornato

Poiché l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono ospitati da Windows Update, gli utenti finali con aggiornamenti automatici abilitati hanno molto probabilmente già questi aggiornamenti, oltre ai Service Pack necessari.

Se nel computer dell'utente finale non è installato l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 e l'applicazione richiede API supportate con questi aggiornamenti, è possibile che l'applicazione non sia in grado di essere eseguita nel computer dell'utente finale o che si verifichino errori durante l'esecuzione.

Per evitare i problemi che potrebbero essere causati dal computer dell'utente non aggiornato, è necessario verificare che nel computer dell'utente sia installato l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 durante l'installazione dell'applicazione. È possibile usare l' [API dell'agente di Windows Update](/windows/desktop/Wua_Sdk/portal-client) per verificare la presenza di aggiornamenti installati nel computer dell'utente finale. È anche possibile usare l'API dell'agente di Windows Update per scaricare e installare gli aggiornamenti necessari durante l'installazione dell'applicazione se l'utente finale non ha ancora installato gli aggiornamenti.

Per un esempio di un programma di installazione che illustra come usare l' [API dell'agente di Windows Update](/windows/desktop/Wua_Sdk/portal-client), vedere la pagina relativa alla distribuzione di [Direct3D 11 per sviluppatori di giochi](../direct3darticles/direct3d11-deployment.md) in [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Sebbene l'esempio di programma di installazione di D3D11InstallHelper, illustrato nella [distribuzione di Direct3D 11 per gli sviluppatori di giochi](../direct3darticles/direct3d11-deployment.md), sia stato scritto per applicazioni che utilizzano Direct3D 11, fornisce un valido esempio di interazione con l' [API dell'agente di Windows Update](/windows/desktop/Wua_Sdk/portal-client) per avviare e tenere traccia del download e dell'installazione degli aggiornamenti ospitati da Windows Update. La compilazione di questo esempio potrebbe richiedere la Windows SDK per Windows 7. Per ulteriori informazioni sull'esempio D3D11InstallHelper, inclusi i problemi noti, vedere [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) Note sulla versione per agosto 2009. aggiornamento della piattaforma per Windows Vista).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiornamento della piattaforma per Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Cenni preliminari**
</dt> <dt>

[Informazioni sull'aggiornamento della piattaforma per Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Articolo della Knowledge base sull'aggiornamento della piattaforma per Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 