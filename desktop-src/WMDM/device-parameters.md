---
title: Parametri del dispositivo
description: Parametri del dispositivo
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Media Gestione dispositivi, parametri del dispositivo
- Gestione dispositivi, parametri del dispositivo
- Guida per programmatori, parametri del dispositivo
- provider di servizi, parametri del dispositivo
- creazione di provider di servizi, parametri del dispositivo
- parametri del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3ad1a1bfc6a24736fdad8385e6cc03e0b20be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329455"
---
# <a name="device-parameters"></a>Parametri del dispositivo

Windows Media Gestione dispositivi usa i parametri del dispositivo per controllare il comportamento di un dispositivo. Questi parametri vengono aggiunti al registro di sistema come specificato nel file di installazione del dispositivo (file INF). La tabella seguente elenca i parametri di dispositivo che Windows Media Gestione dispositivi esegue query.



| Nome parametro dispositivo | Tipo di dati del registro di sistema | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *WMDMSPCLSID*         | **REG \_ SZ**        | Valore che specifica il CLSID del provider di servizi che controlla il dispositivo. Questo parametro è obbligatorio per il supporto PnP.<br/> Il valore del parametro deve essere CLSID, non il ProgID del provider di servizi. Questo parametro è obbligatorio per supportare Plug and Play (PnP) in Windows Media Gestione dispositivi. Per ulteriori informazioni, vedere [Abilitazione di PNP per i dispositivi](enabling-pnp-for-devices.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *OptimalTransferSize* | **REG \_ DWORD**     | Valore facoltativo che specifica la dimensione di trasferimento preferita utilizzata da Windows Media Gestione dispositivi durante le operazioni di lettura e scrittura. Se non viene specificato, viene utilizzata una dimensione di trasferimento predefinita.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **REG \_ DWORD**     | Parametro facoltativo che specifica se Windows Media Gestione dispositivi organizza il contenuto in base ai metadati durante la presentazione del contenuto del dispositivo alle applicazioni. Il valore predefinito, utilizzato quando questo parametro non viene specificato, è 0.<br/> Quando le applicazioni enumerano il contenuto nelle archiviazioni di un lettore audio portatile, Windows Media Gestione dispositivi può presentare il contenuto organizzato in base ai metadati. Questa operazione è particolarmente utile per i dispositivi con capacità di archiviazione di grandi dimensioni.<br/> Le applicazioni e i dispositivi sono in grado di controllare questo comportamento. I dispositivi indicano le loro preferenze tramite il parametro di dispositivo *UseMetadataViews*.<br/> Sono supportati i due valori integer seguenti:<br/> Richiede che il contenuto venga presentato alle applicazioni esattamente come organizzato nel file system del dispositivo.<br/> Richiede che il contenuto venga presentato alle applicazioni organizzate in base ai metadati.<br/> |
| *ShowInShell*         | **REG \_ DWORD**     | Parametro facoltativo che specifica se il dispositivo deve essere visualizzato in Esplora risorse. Il valore 1 indica che il dispositivo deve essere visualizzato in Esplora risorse. Per ulteriori informazioni, vedere [requisiti per la visualizzazione dei lettori audio portatili in Esplora risorse](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *UseExtendedWmdm*     | **REG \_ DWORD**     | Parametro facoltativo che avvisa Windows Media Gestione dispositivi che il provider di servizi supporti **IMDSPDevice3**, **IMDSPObject2** e **IMDSPStorage4**. Senza questo flag, Windows Media Gestione dispositivi non chiamerà mai queste interfacce. Il valore 1 indica che queste interfacce sono supportate.<br/> Questo flag è necessario per i provider di servizi che si sincronizzano con Windows Media Player. (Vedere [Abilitazione della sincronizzazione con Windows Media Player](enabling-synchronization-with-windows-media-player.md)).<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

**Codifica del file INF**

Il codice di esempio seguente da un file INF del dispositivo illustra l'impostazione di alcuni parametri del dispositivo durante l'installazione del dispositivo.


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> <dt>

[**Interfaccia IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[**Interfaccia IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





