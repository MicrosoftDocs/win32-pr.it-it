---
description: Utilizzato per eseguire le attività in modo asincrono e creato con D3DX10CreateThreadPump.
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: Interfaccia ID3DX10ThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9fe3f0ca5955963864ef18de5d86fe03083d3f3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132414"
---
# <a name="id3dx10threadpump-interface"></a>Interfaccia ID3DX10ThreadPump

Utilizzato per eseguire le attività in modo asincrono e creato con [**D3DX10CreateThreadPump**](d3dx10createthreadpump.md). Esistono diverse API D3DX10 che possono facoltativamente assumere un thread Pump come parametro, ad esempio [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (vedere la sezione Osservazioni per l'elenco completo). Se la pompa di thread viene passata in queste API, viene eseguita in modo asincrono su un thread della pompa di thread separato. Il vantaggio di questa operazione è che può comportare il caricamento e l'elaborazione di grandi quantità di dati senza visualizzare un rallentamento evidente delle prestazioni sullo schermo.

## <a name="members"></a>Membri

L'interfaccia **ID3DX10ThreadPump** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10ThreadPump** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX10ThreadPump** dispone di questi metodi.



| Metodo                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddWorkItem**](id3dx10threadpump-addworkitem.md)                       | Aggiungere un elemento di lavoro alla pompa di thread.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetQueueStatus**](id3dx10threadpump-getqueuestatus.md)                 | Ottenere il numero di elementi in ognuna delle tre code all'interno della pompa di thread.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**GetWorkItemCount**](id3dx10threadpump-getworkitemcount.md)             | Ottiene il numero di elementi di lavoro attualmente presenti nella pompa di thread.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**ProcessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md) | Impostare gli elementi di lavoro sul dispositivo dopo aver completato il caricamento e l'elaborazione. Al termine del caricamento e dell'elaborazione di una risorsa o di uno shader, il thread Pump lo manterrà in una coda fino a quando non viene chiamata l'API, a quel punto gli elementi elaborati verranno impostati sul dispositivo. Questa operazione è utile per controllare la quantità di elaborazione dedicata al binding delle risorse al dispositivo per ogni frame. Vedere la sezione Osservazioni.<br/> |
| [**PurgeAllItems**](id3dx10threadpump-purgeallitems.md)                   | Cancella tutti gli elementi di lavoro dalla pompa di thread.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**WaitForAllItems**](id3dx10threadpump-waitforallitems.md)               | Attendere il completamento di tutti gli elementi di lavoro della pompa di thread.<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

Il pump di thread carica ed elabora i dati in un processo in tre passaggi. Ecco:

1.  Caricare e decomprimere i dati con un caricatore di dati. L'oggetto caricatore di dati dispone di tre metodi che la pompa di thread chiamerà internamente durante il caricamento e la decompressione dei dati: [**ID3DX10DataLoader:: Load**](id3dx10dataloader-load.md), [**ID3DX10DataLoader::D eComPress**](id3dx10dataloader-decompress.md)e [**ID3DX10DataLoader::D estroy**](id3dx10dataloader-destroy.md). Le funzionalità specifiche di queste tre API variano a seconda del tipo di dati caricati e decompressi. L'interfaccia del caricatore dati può anche essere ereditata e le relative API possono essere modificate se si carica un file di dati definito in un formato personalizzato.
2.  Elaborare i dati con un elaboratore di dati. L'oggetto elaboratore di dati dispone di tre metodi che la pompa di thread chiamerà internamente durante l'elaborazione dei dati: [**ID3DX10DataProcessor::P rocess**](id3dx10dataprocessor-process.md), [**ID3DX10DataProcessor:: CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md)e [**ID3DX10DataProcessor::D estroy**](id3dx10dataprocessor-destroy.md). La modalità di elaborazione dei dati sarà diversa a seconda del tipo di dati. Se, ad esempio, i dati sono una trama archiviata come JPEG, **ID3DX10DataProcessor::P rocess** eseguirà la decompressione JPEG per ottenere i bit dell'immagine non elaborata dell'immagine. Se i dati sono uno shader, **ID3DX10DataProcessor::P rocess** compilerà il HLSL in bytecode. Dopo che i dati sono stati elaborati, viene creato un oggetto dispositivo per quei dati (con **ID3DX10DataProcessor:: CreateDeviceObject**) e l'oggetto verrà aggiunto a una coda di oggetti dispositivo. L'interfaccia del processore dati può anche essere ereditata e le relative API possono essere modificate se si sta elaborando un file di dati definito in un formato personalizzato.
3.  Associare l'oggetto dispositivo al dispositivo. Questa operazione viene eseguita quando un'applicazione chiama [**ID3DX10ThreadPump::P rocessdeviceworkitems**](id3dx10threadpump-processdeviceworkitems.md), che consente di associare al dispositivo un numero specificato di oggetti nella coda degli oggetti dispositivo.

La pompa di thread può essere usata per caricare i dati in uno dei due modi seguenti: chiamando un'API che accetta un thread Pump come parametro, ad esempio [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CompileFromFile**](d3dx10compilefromfile.md), oppure chiamando [**ID3DX10ThreadPump:: AddWorkItem**](id3dx10threadpump-addworkitem.md). Nel caso delle API che accettano un thread Pump, il caricatore di dati e il processore di dati vengono creati internamente. Nel caso di **AddWorkItem**, il caricatore di dati e il processore di dati devono essere creati in anticipo e vengono quindi passati in AddWorkItem. D3DX10 fornisce un set di API per la creazione di caricatori di dati e processori di dati con funzionalità per il caricamento e l'elaborazione di formati di dati comuni (vedere la sezione Osservazioni per l'elenco completo delle API). Per i formati di dati personalizzati, le interfacce del caricatore di dati e del processore di dati devono essere ereditate e i relativi metodi devono essere ridefiniti.

L'oggetto della pompa di thread occupa una quantità sostanziale di risorse, quindi in genere è necessario crearne solo una per ogni applicazione.

Caricatori dati D3DX10 predefiniti



|                                                                            |                                          |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | Creare un caricatore di file in modo asincrono.     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | Creare un caricatore dati in modo asincrono.     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | Creare un caricatore di risorse in modo asincrono. |



 

Processori di dati D3DX10 predefiniti



|                                                                                                  |                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | Creare un elaboratore di dati da utilizzare con una pompa di thread. Questa API è simile a D3DX10CreateAsyncTextureInfoProcessor, ma carica anche la trama. |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | Creare un elaboratore di dati da utilizzare con una pompa di thread.                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | Compilare uno shader e creare un elaboratore di dati in modo asincrono.                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | Creare un effetto con un elaboratore di dati in modo asincrono.                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | Creare un pool di effetti in modo asincrono.                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | Creare un elaboratore di dati in modo asincrono.                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | Creare un elaboratore di dati per uno shader in modo asincrono.                                                                                               |



 

API che accettano un thread Pump come parametro.



|                                                                                                  |                                                                  |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)                                           | Compilare uno shader da un file.                                    |
| [**D3DX10CompileFromMemory**](d3dx10compilefrommemory.md)                                       | Compilare uno shader che risiede in memoria.                             |
| [**D3DX10CompileFromResource**](d3dx10compilefromresource.md)                                   | Compilare uno shader da una risorsa.                                |
| [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md)                                 | Creare un effetto da un file.                                    |
| [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)                             | Creare un effetto dalla memoria.                                    |
| [**D3DX10CreateEffectFromResource**](d3dx10createeffectfromresource.md)                         | Creare un effetto da una risorsa.                                |
| [**D3DX10CreateEffectPoolFromFile**](d3dx10createeffectpoolfromfile.md)                         | Creare un pool di effetti da un file.                               |
| [**D3DX10CreateEffectPoolFromMemory**](d3dx10createeffectpoolfrommemory.md)                     | Creare un pool di effetti da un file che risiede in memoria.            |
| [**D3DX10CreateEffectPoolFromResource**](d3dx10createeffectpoolfromresource.md)                 | Creare un pool di effetti da una risorsa.                           |
| [**D3DX10PreprocessShaderFromFile**](d3dx10preprocessshaderfromfile.md)                         | Creare uno shader da un file senza compilarlo.                |
| [**D3DX10PreprocessShaderFromMemory**](d3dx10preprocessshaderfrommemory.md)                     | Creare uno shader dalla memoria senza compilarlo.                |
| [**D3DX10PreprocessShaderFromResource**](d3dx10preprocessshaderfromresource.md)                 | Creare uno shader da una risorsa senza compilarlo.            |
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | Creare una visualizzazione risorse shader da un file.                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | Creare una visualizzazione risorse shader da un file in memoria.             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | Creare una visualizzazione risorse shader da una risorsa.                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | Recupera le informazioni su un file di immagine specificato.                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | Ottenere informazioni su un'immagine già caricata in memoria.       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | Recupera le informazioni su una determinata immagine in una risorsa.         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | Creare una risorsa di trama da un file.                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | Creare una risorsa di trama da un file che risiede nella memoria di sistema. |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | Creare una risorsa di trama da un'altra risorsa.                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
