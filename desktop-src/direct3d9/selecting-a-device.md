---
description: Le applicazioni possono eseguire query sull'hardware per rilevare i tipi di dispositivi Direct3D supportati. Questa sezione contiene informazioni sulle attività principali relative all'enumerazione delle schede di visualizzazione e alla selezione di dispositivi Direct3D.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Selezione di un dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63428e15948e15790364f310d55989a9bbc7339846f7db5d301e316bee4d872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044249"
---
# <a name="selecting-a-device-direct3d-9"></a>Selezione di un dispositivo (Direct3D 9)

Le applicazioni possono eseguire query sull'hardware per rilevare i tipi di dispositivi Direct3D supportati. Questa sezione contiene informazioni sulle attività principali relative all'enumerazione delle schede di visualizzazione e alla selezione di dispositivi Direct3D.

Un'applicazione deve eseguire una serie di attività per selezionare un dispositivo Direct3D appropriato. Si noti che i passaggi seguenti sono destinati a un'applicazione a schermo intero e che, nella maggior parte dei casi, un'applicazione a finestre può ignorare la maggior parte di questi passaggi.

1.  Inizialmente, l'applicazione deve enumerare le schede video nel sistema. Un adattatore è un componente hardware fisico. Si noti che la scheda grafica può contenere più di un singolo adattatore, come nel caso di uno schermo a due teste. Le applicazioni che non hanno a che fare con il supporto multi-monitoraggio possono ignorare questo passaggio e passare D3DADAPTER DEFAULT al metodo \_ [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) nel passaggio 2.
2.  Per ogni adattatore, l'applicazione enumera le modalità di visualizzazione supportate chiamando [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).
3.  Se necessario, l'applicazione verifica la presenza di accelerazione hardware in ogni modalità di visualizzazione enumerata chiamando [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), come illustrato nell'esempio di codice seguente. Si noti che si tratta solo di uno degli utilizzi possibili per **IDirect3D9::CheckDeviceType**; Per informazioni dettagliate, vedere [Determinazione del supporto hardware (Direct3D 9).](determining-hardware-support.md)
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

    

4.  L'applicazione verifica il livello di funzionalità desiderato per il dispositivo in questo adattatore chiamando il metodo [**IDirect3D9::GetDeviceCaps.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) La funzionalità restituita da questo metodo è garantita come costante per un dispositivo in tutte le modalità di visualizzazione, verificata da [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).
5.  I dispositivi possono sempre eseguire il rendering su superfici del formato di una modalità di visualizzazione enumerata supportata dal dispositivo. Se l'applicazione deve eseguire il rendering su una superficie di un formato diverso, può chiamare [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat). Se il dispositivo può eseguire il rendering nel formato , è garantito che tutte le funzionalità restituite da [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) siano applicabili.
6.  Infine, l'applicazione può determinare se le tecniche di multicampionamento, ad esempio l'antialiasing a scena completa, sono supportate per un formato di rendering usando il metodo [**IDirect3D9::CheckDeviceMultiSampleType.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)

Dopo aver completato i passaggi precedenti, l'applicazione deve avere un elenco di modalità di visualizzazione in cui può operare. Il passaggio finale consiste nel verificare che sia disponibile una quantità sufficiente di memoria accessibile al dispositivo per soddisfare il numero richiesto di buffer e antialiasing. Questo test è necessario perché il consumo di memoria per la combinazione di modalità e multicampionamento è impossibile da stimare senza verificarlo. Inoltre, alcune architetture di schede video potrebbero non avere una quantità costante di memoria accessibile dal dispositivo. Ciò significa che un'applicazione deve essere in grado di segnalare errori di memoria fuori video quando si entra in modalità schermo intero. In genere, un'applicazione deve rimuovere la modalità schermo intero dall'elenco di modalità offerte a un utente oppure tentare di utilizzare meno memoria riducendo il numero di buffer nascosto o usando una tecnica di multicampionamento meno complessa.

Un'applicazione con finestre esegue un set simile di attività.

1.  Determina il rettangolo del desktop coperto dall'area client della finestra.
2.  Enumera gli adattatori, cercando l'adattatore il cui monitoraggio copre l'area client. Se l'area client è di proprietà di più di un adattatore, l'applicazione può scegliere di guidare ogni scheda in modo indipendente o di guidare un singolo adattatore e trasferire i pixel direct3D da un dispositivo a un altro durante la presentazione. L'applicazione può anche ignorare due passaggi precedenti e usare l'adattatore D3DADAPTER \_ DEFAULT. Si noti che ciò potrebbe comportare un'operazione più lenta quando la finestra viene posizionata su un monitor secondario.
3.  L'applicazione deve chiamare [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) per determinare se il dispositivo può supportare il rendering in un buffer nascosto del formato specificato in modalità desktop. [**IDirect3D9::GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) può essere usato per determinare il formato di visualizzazione del desktop, come illustrato nell'esempio di codice seguente.
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

 

 
