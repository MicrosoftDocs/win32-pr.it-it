---
title: Convalida basata su GPU e livello di debug Direct3D 12
description: Questo argomento descrive come usare al meglio il livello di debug Direct3D 12. La convalida basata su GPU (GBV) consente scenari di convalida nella sequenza temporale GPU che non sono possibili durante le chiamate API sulla CPU.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548875"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a>Convalida basata su GPU e livello di debug Direct3D 12

Questo argomento descrive come usare al meglio il livello di debug Direct3D 12. La convalida basata su GPU (GBV) consente scenari di convalida nella sequenza temporale GPU che non sono possibili durante le chiamate API sulla CPU. GBV è disponibile a partire da strumenti di grafica per l'aggiornamento dell'anniversario di Windows 10.

## <a name="purpose-of-gpu-based-validation"></a>Scopo della convalida basata su GPU

La convalida basata su GPU consente di identificare gli errori seguenti:

- Utilizzo di descrittori non inizializzati o incompatibili in uno shader.
- Uso di descrittori che fanno riferimento a risorse eliminate in uno shader.
- Convalida degli Stati delle risorse promossi e del decadimento dello stato delle risorse.
- Indicizzazione oltre la fine dell'heap del descrittore in uno shader.
- Gli accessi allo shader di risorse in stato incompatibile.
- Utilizzo di campioni non inizializzati o incompatibili in uno shader.

GBV funziona creando shader con patch con la convalida aggiunta direttamente allo shader. Gli shader con patch controllano gli argomenti radice e le risorse a cui si accede durante l'esecuzione dello shader e segnalano gli errori a un buffer del log. GBV inserisce anche operazioni aggiuntive e invia chiamate agli elenchi di comandi dell'applicazione per convalidare e tenere traccia delle modifiche apportate allo stato delle risorse imposte dall'elenco dei comandi nella sequenza temporale GPU.

Poiché GBV richiede la possibilità di eseguire shader, gli elenchi di comandi di copia vengono emulati da un elenco di comandi di calcolo. Questo può potenzialmente modificare il modo in cui l'hardware esegue le copie anche se il risultato finale non deve essere modificato. L'applicazione continuerà a percepire gli elenchi di comandi di copia e il livello di debug li convaliderà come tali.

## <a name="turning-on-gpu-based-validation"></a>Attivazione della convalida basata su GPU

GBV può essere forzata usando il pannello di controllo DirectX (DXCPL) forzando il livello di debug Direct3D 12 e forzando la convalida basata su GPU (nuova scheda nel pannello di controllo). Una volta abilitata, GBV rimarrà abilitato fino al rilascio del dispositivo Direct3D 12. In alternativa, è possibile abilitare GBV a livello di codice prima di creare il dispositivo Direct3D 12:

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a>Uso consigliato

In genere, è consigliabile eseguire il codice con il livello di debug abilitato per la maggior parte del tempo. Tuttavia, GBV può rallentare molto l'attività. Gli sviluppatori possono prendere in considerazione l'abilitazione di GBV con set di dati più piccoli (ad esempio, demo del motore o piccoli livelli di gioco con meno impostazioni e risorse di PSO) o durante l'introduzione anticipata dell'applicazione per ridurre i problemi di prestazioni. Con contenuto di dimensioni maggiori, è consigliabile attivare GBV in uno o due computer di test in un test notturno superato.

## <a name="debug-output"></a>Output di debug

GBV produce l'output di debug dopo che una chiamata a [**oggetti executecommandlist**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) completa l'esecuzione sulla GPU. Poiché si trova nella sequenza temporale GPU, l'output di debug può essere asincrono con altre convalide della sequenza temporale della CPU. Gli sviluppatori di applicazioni possono voler inserire il proprio Wait-after-Execute per sincronizzare l'output di debug.

L'output di GBV identifica la posizione in cui si è verificato un errore in uno shader, insieme al conteggio e alle identità correnti degli oggetti correlati, ad esempio elenco dei comandi, coda, PSO e così via.

## <a name="example-debug-message"></a>Messaggio di debug di esempio

Il messaggio di errore seguente indica che è stato eseguito l'accesso a una risorsa denominata "buffer del colore principale" in uno shader come risorsa dello shader, ma che era nello stato di accesso non ordinato quando lo shader è stato eseguito nella GPU. Vengono fornite anche informazioni aggiuntive, ad esempio la posizione nell'origine dello shader, il nome dell'elenco di comandi e il conteggio di disegni (indice di estrazione) e i nomi degli oggetti dell'interfaccia D3D correlati.

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a>API del livello di debug

Per abilitare il livello di debug, chiamare [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).

Per abilitare la convalida basata su GPU, chiamare [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)e fare riferimento ai metodi delle interfacce seguenti:

- [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

Vedere le enumerazioni e le strutture seguenti:

- [**\_Tipo di \_ parametro dell'elenco di comandi di debug D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [**\_Tipo di \_ parametro del dispositivo di debug D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [**D3D12 \_ \_ \_ \_ \_ \_ creare flag per lo stato della pipeline di convalida basata \_ sulla GPU**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [**\_ \_ \_ \_ \_ Modalità patch shader di convalida basata su \_ GPU D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [**\_Impostazioni di \_ \_ \_ \_ convalida basate su GPU \_ per l'elenco dei \_ comandi di debug D3D12**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [**\_Impostazioni di \_ \_ \_ convalida basate su \_ GPU \_ del dispositivo debug D3D12**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni sul livello di debug Direct3D 12](understanding-the-d3d12-debug-layer.md)
