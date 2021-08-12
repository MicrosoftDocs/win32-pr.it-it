---
title: Parametri del dispositivo
description: Parametri del dispositivo
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Gestione dispositivi multimediali, parametri del dispositivo
- Gestione dispositivi, parametri del dispositivo
- guida alla programmazione, parametri del dispositivo
- provider di servizi, parametri del dispositivo
- creazione di provider di servizi, parametri del dispositivo
- parametri del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef097940670148551042c22fd8efc6aa51c641960bf0f821361aaf3c29c731d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585350"
---
# <a name="device-parameters"></a>Parametri del dispositivo

Windows Gestione dispositivi multimediali usa i parametri del dispositivo per controllare il comportamento di un dispositivo. Questi parametri vengono aggiunti al Registro di sistema come specificato nel file di installazione del dispositivo (file INF). La tabella seguente elenca i parametri del dispositivo che Windows query di Gestione dispositivi multimediali.



| Nome del parametro del dispositivo | Tipo di dati del Registro di sistema | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *WMDMSPCLSID*         | **REG \_ SZ**        | Valore che specifica il CLSID del provider di servizi che controlla il dispositivo. Questo parametro è obbligatorio per il supporto PnP.<br/> Il valore del parametro deve essere il CLSID, non il ProgID del provider di servizi. Questo parametro è obbligatorio per supportare Plug and Play (PnP) in Windows Gestione dispositivi multimediali. Per altre informazioni, vedere [Abilitazione di PnP per i dispositivi.](enabling-pnp-for-devices.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *OptimalTransferSize* | **REG \_ DWORD**     | Valore facoltativo che specifica le dimensioni di trasferimento preferite Windows gestione dispositivi multimediali durante le operazioni di lettura e scrittura. Se non viene specificato, viene utilizzata una dimensione di trasferimento predefinita.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **REG \_ DWORD**     | Parametro facoltativo che specifica se Windows Gestione dispositivi multimediali organizza il contenuto in base ai metadati durante la presentazione del contenuto del dispositivo alle applicazioni. Il valore predefinito, utilizzato quando questo parametro non viene specificato, è 0.<br/> Quando le applicazioni enumerano il contenuto nelle risorse di archiviazione di un lettore audio portatile, Windows Gestione dispositivi multimediali può presentare il contenuto organizzato in base ai metadati. Ciò è particolarmente utile per i dispositivi con capacità di archiviazione di grandi dimensioni.<br/> Le applicazioni e i dispositivi sono in grado di controllare questo comportamento. I dispositivi indicano la loro preferenza tramite il parametro *del dispositivo UseMetadataViews*.<br/> Sono supportati i due valori interi seguenti:<br/> Richiede che il contenuto sia presentato alle applicazioni esattamente come organizzato file system del dispositivo.<br/> Richiede che il contenuto sia presentato alle applicazioni organizzate in base ai metadati.<br/> |
| *ShowInShell*         | **REG \_ DWORD**     | Parametro facoltativo che specifica se il dispositivo deve essere visualizzato in Windows Explorer. Il valore 1 indica che il dispositivo deve essere visualizzato in Windows Explorer. Per altre informazioni, vedere Requisiti per la visualizzazione dei lettori audio portatili [in Windows Explorer.](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *UseExtendedWmdm*     | **REG \_ DWORD**     | Parametro facoltativo che Windows Gestione dispositivi multimediali che il provider di servizi supporta **IMDSPDevice3,** **IMDSPObject2** e **IMDSPStorage4.** Senza questo flag, Windows Gestione dispositivi multimediali non chiamerà mai queste interfacce. Il valore 1 indica che queste interfacce sono supportate.<br/> Questo flag è obbligatorio per i provider di servizi che si sincronizzano con Windows Media Player. Vedere [Abilitazione della sincronizzazione con Windows Media Player](enabling-synchronization-with-windows-media-player.md).<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

**Codifica del file INF**

Il codice di esempio seguente dal file INF di un dispositivo illustra l'impostazione di alcuni parametri del dispositivo durante l'installazione del dispositivo.


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

[**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[**Interfaccia IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





