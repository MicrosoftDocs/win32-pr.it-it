---
title: Sviluppo di applicazioni per le versioni precedenti di Windows
description: Spiega cosa fare per sviluppare applicazioni eseguite in versioni precedenti di Windows e sfruttare l'API supportata con l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afbb999faf934ae621f80a824eca0289ff3df705ed11d7cfd161935c944947f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549481"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Sviluppo di applicazioni per le versioni precedenti di Windows

Spiega cosa fare per sviluppare applicazioni eseguite in versioni precedenti di Windows e sfruttare l'API supportata con l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.

## <a name="required-downloads"></a>Download necessari

Per sviluppare applicazioni che usano API introdotte con Microsoft Windows Software Development Kit (SDK) per Windows 7, è necessario scaricare e installare i pacchetti descritti nelle sezioni seguenti.

### <a name="microsoft-windows-sdk"></a>Microsoft Windows SDK

L'SDK Windows per Windows 7 è necessario per la creazione di applicazioni che usano API supportate con l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008.

Per accedere a risorse e informazioni aggiuntive, ad esempio download, post di forum e il blog del team di Windows SDK, vedere il centro per sviluppatori [di Windows SDK](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

Il .NET Framework 3.5 Service Pack 1 è necessario per la creazione di applicazioni che usano API supportate dall'aggiornamento della piattaforma per Windows Vista e dall'aggiornamento della piattaforma per Windows Server 2008.

Per altre risorse e informazioni, vedere .NET Framework [Developer Center](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>DirectX SDK obbligatorio quando si usa Direct3D

Se si creano applicazioni che usano Direct3D, [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( è necessario per la creazione di applicazioni che usano API supportate dall'aggiornamento della piattaforma per Windows Vista e dall'aggiornamento della piattaforma https://msdn.microsoft.com/directx/aa937788.aspx) per Windows Server 2008.

### <a name="update-your-development-computer"></a>Aggiornare il computer di sviluppo

Assicurarsi che nel computer di sviluppo siano disponibili tutti gli aggiornamenti più recenti Windows Update.

Se si sviluppano applicazioni in una versione precedente di Windows, è necessario ottenere l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 da Windows Update. L'installazione di uno di questi aggiornamenti consentirà di sfruttare la nuova API fornita da Windows SDK per Windows 7.

Per altre informazioni su come ottenere gli aggiornamenti da Windows Update, vedere l'articolo Knowledge Base sull'aggiornamento della piattaforma per [Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Ambiente di sviluppo

### <a name="set-the-build-target-to-windows-7"></a>Impostare La destinazione di compilazione su Windows 7

Tutte le applicazioni che usano librerie in Platform Update per Windows Vista devono essere compilate sulla Windows 7 della piattaforma di destinazione.

L'impostazione di WINVER sul valore della piattaforma di destinazione Windows 7 consente di sviluppare applicazioni che usano API supportate con l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 in un computer di sviluppo che esegue Windows Vista.

È possibile impostare la piattaforma di destinazione su Windows 7 nel codice sorgente o usando l'opzione /D con il Visual Studio compilazione.

L'esempio seguente illustra come impostare WINVER nel codice sorgente.


```C++
#define WINVER 0x0601
```



L'esempio seguente illustra come impostare WINVER usando l'opzione del compilatore /D.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Distribuzione dell'applicazione

Se si compila l'applicazione usando le intestazioni e le librerie fornite da Windows SDK per Windows 7, le API supportate verranno eseguite in qualsiasi versione di Windows in cui sia installato l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

> [!Note]  
> Il comportamento, le prestazioni o i requisiti per alcune API supportate con l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono variare in diverse versioni di Windows. Per informazioni dettagliate su un'API specifica supportata dagli aggiornamenti, vedere Informazioni sull'aggiornamento della [piattaforma per Windows Vista](platform-update-for-windows-vista-overview.md).

 

### <a name="no-redistributable-components"></a>Nessun componente ridistribuibile

L'applicazione non deve installare componenti ridistribuibili, ad esempio DLL o altri file di runtime.

### <a name="requires-updated-end-user-computer"></a>Richiede l'aggiornamento End-User computer

Poiché l'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono ospitati da Windows Update, è molto probabile che gli utenti finali con gli aggiornamenti automatici abilitati abbia già questi aggiornamenti e i Service Pack necessari.

Se nel computer dell'utente finale non è installato l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 e l'applicazione richiede API supportate con questi aggiornamenti, l'applicazione potrebbe non essere in grado di essere eseguita nel computer dell'utente finale o potrebbe verificarsi errori durante l'esecuzione.

Per evitare i problemi che potrebbero essere causati da un computer dell'utente non aggiornato, è necessario verificare che il computer dell'utente abbia l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 durante l'installazione dell'applicazione. È possibile usare [l'API Windows Update Agent](/windows/desktop/Wua_Sdk/portal-client) per verificare la presenza di aggiornamenti installati nel computer dell'utente finale. È anche possibile usare l'API Windows Update Agent per scaricare e installare gli aggiornamenti necessari durante l'installazione dell'applicazione se l'utente finale non ha già installato gli aggiornamenti.

Per un esempio di programma di installazione che illustra come usare l'API dell'agente di aggiornamento [di Windows](/windows/desktop/Wua_Sdk/portal-client), vedere [Distribuzione direct3D 11](../direct3darticles/direct3d11-deployment.md) per sviluppatori di giochi in [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Anche se l'esempio di programma di installazione D3D11InstallHelper illustrato in Distribuzione [direct3D 11](../direct3darticles/direct3d11-deployment.md)per sviluppatori di giochi è stato scritto per le applicazioni che usano Direct3D 11, fornisce un buon esempio di interazione con [l'API](/windows/desktop/Wua_Sdk/portal-client) dell'agente di aggiornamento di Windows per avviare e tenere traccia del download e dell'installazione degli aggiornamenti ospitati da Windows Update. La compilazione di questo esempio può richiedere Windows SDK per Windows 7. Per altre informazioni sull'esempio D3D11InstallHelper, inclusi i problemi noti, vedere [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( Note sulla versione per l'aggiornamento di agosto https://msdn.microsoft.com/directx/aa937788.aspx) 2009.Platform per Windows Vista

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiornamento della piattaforma per Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Cenni preliminari**
</dt> <dt>

[Informazioni sull'aggiornamento della piattaforma per Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Knowledge Base articolo sull'aggiornamento della piattaforma per Windows Vista (kb 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 