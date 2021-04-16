---
description: Le applicazioni possono eseguire query sull'hardware per rilevare i tipi di dispositivo Direct3D supportati. Questa sezione contiene informazioni sulle attività primarie necessarie per l'enumerazione degli adattatori di visualizzazione e la selezione di dispositivi Direct3D.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Selezione di un dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdfa1faf38007f00959ac7263b4538954044688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522762"
---
# <a name="selecting-a-device-direct3d-9"></a>Selezione di un dispositivo (Direct3D 9)

Le applicazioni possono eseguire query sull'hardware per rilevare i tipi di dispositivo Direct3D supportati. Questa sezione contiene informazioni sulle attività primarie necessarie per l'enumerazione degli adattatori di visualizzazione e la selezione di dispositivi Direct3D.

Un'applicazione deve eseguire una serie di attività per selezionare un dispositivo Direct3D appropriato. Si noti che i passaggi seguenti sono destinati a un'applicazione a schermo intero e che, nella maggior parte dei casi, un'applicazione a finestra può ignorare la maggior parte di questi passaggi.

1.  Inizialmente, l'applicazione deve enumerare le schede di visualizzazione nel sistema. Un adapter è un componente fisico. Si noti che la scheda grafica potrebbe contenere più di una singola scheda, come nel caso di una visualizzazione a due punte. Le applicazioni non interessate dal supporto per più monitor possono ignorare questo passaggio e passare D3DADAPTER \_ per impostazione predefinita al metodo [**IDirect3D9:: EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) nel passaggio 2.
2.  Per ogni adapter, l'applicazione enumera le modalità di visualizzazione supportate chiamando [**IDirect3D9:: EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).
3.  Se necessario, l'applicazione verifica la presenza di accelerazione hardware in ogni modalità di visualizzazione enumerata chiamando [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), come illustrato nell'esempio di codice seguente. Si noti che questo è solo uno degli usi possibili per **IDirect3D9:: CheckDeviceType**; per informazioni dettagliate, vedere [determinazione del supporto hardware (Direct3D 9)](determining-hardware-support.md).
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    Params.BackBufferFormat = D3DFMT_X1R5G5B5; 

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, 
                      Device.m_DevType, 
                      Params.BackBufferFormat, Params.BackBufferFormat, 
                      FALSE))) 
        return E_FAIL;
    ```

    

4.  L'applicazione verifica il livello di funzionalità desiderato per il dispositivo su questa scheda chiamando il metodo [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) . La funzionalità restituita da questo metodo è garantita come costante per un dispositivo in tutte le modalità di visualizzazione, verificata da [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).
5.  I dispositivi possono sempre eseguire il rendering in superfici del formato di una modalità di visualizzazione enumerata supportata dal dispositivo. Se è necessario eseguire il rendering dell'applicazione in una superficie di un formato diverso, è possibile chiamare [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat). Se è possibile eseguire il rendering del dispositivo nel formato, si garantisce che tutte le funzionalità restituite da [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) siano applicabili.
6.  Infine, l'applicazione può determinare se le tecniche di campionamento multiplo, ad esempio l'anti-aliasing della scena completa, sono supportate per un formato di rendering tramite il metodo [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) .

Dopo aver completato i passaggi precedenti, l'applicazione deve disporre di un elenco delle modalità di visualizzazione in cui può funzionare. Il passaggio finale consiste nel verificare che sia disponibile una quantità sufficiente di memoria accessibile dal dispositivo per contenere il numero necessario di buffer e l'anti-aliasing. Questo test è necessario perché il consumo di memoria per la combinazione di modalità e multicampionamento è impossibile da prevedere senza verificarlo. Inoltre, alcune architetture degli adattatori di visualizzazione potrebbero non avere una quantità costante di memoria accessibile dal dispositivo. Ciò significa che un'applicazione deve essere in grado di segnalare errori di memoria out-of-video quando si passa alla modalità schermo intero. In genere, un'applicazione deve rimuovere la modalità a schermo intero dall'elenco di modalità che offre a un utente o tentare di utilizzare una quantità di memoria inferiore riducendo il numero di buffer indietro o utilizzando una tecnica multicampionamento meno complessa.

Un'applicazione a finestra esegue un set di attività simile.

1.  Determina il rettangolo del desktop coperto dall'area client della finestra.
2.  Enumera gli adapter, cercando la scheda il cui monitoraggio copre l'area client. Se l'area client è di proprietà di più schede, l'applicazione può scegliere di instradare ogni scheda in modo indipendente o di eseguire una singola scheda con Direct3D Transfer pixel da un dispositivo a un altro alla presentazione. L'applicazione può inoltre ignorare due passaggi precedenti e utilizzare l' \_ adapter predefinito D3DADAPTER. Si noti che questo potrebbe causare un'operazione più lenta quando la finestra viene posizionata su un monitor secondario.
3.  L'applicazione deve chiamare [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) per determinare se il dispositivo è in grado di supportare il rendering in un buffer nascosto del formato specificato in modalità desktop. [**IDirect3D9:: GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) può essere usato per determinare il formato di visualizzazione del desktop, come illustrato nell'esempio di codice seguente.
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    // Use the current display mode.
    D3DDISPLAYMODE mode;

    if(FAILED(m_pD3D->GetAdapterDisplayMode(Device.m_uAdapter , &mode)))
        return E_FAIL;

    Params.BackBufferFormat = mode.Format;

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, Device.m_DevType, 
    Params.BackBufferFormat, Params.BackBufferFormat, FALSE)))
        return E_FAIL;
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
