---
description: Usato per eseguire attività in modo asincrono e creato con D3DX10CreateThreadPump.
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: Interfaccia ID3DX10ThreadPump (D3DX10.h)
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
ms.openlocfilehash: ef95e4087d2d50e00bf7637119038f35378b8ef1657c23ac8b7a11e62acad3a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046869"
---
# <a name="id3dx10threadpump-interface"></a>Interfaccia ID3DX10ThreadPump

Usato per eseguire attività in modo asincrono e creato con [**D3DX10CreateThreadPump.**](d3dx10createthreadpump.md) Sono disponibili diverse API D3DX10 che possono facoltativamente prendere un pump di thread come parametro, ad esempio [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (vedere le note per l'elenco completo). Se il thread pump viene passato a queste API, verrà eseguito in modo asincrono in un thread pump separato. Il vantaggio di questa operazione è che può fare in modo che il caricamento e l'elaborazione di grandi quantità di dati avvengano senza un notevole rallentamento delle prestazioni sullo schermo.

## <a name="members"></a>Membri

**L'interfaccia ID3DX10ThreadPump** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10ThreadPump** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX10ThreadPump** include questi metodi.



| Metodo                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddWorkItem**](id3dx10threadpump-addworkitem.md)                       | Aggiungere un elemento di lavoro al thread pump.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetQueueStatus**](id3dx10threadpump-getqueuestatus.md)                 | Ottiene il numero di elementi in ognuna delle tre code all'interno del thread pump.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**GetWorkItemCount**](id3dx10threadpump-getworkitemcount.md)             | Ottiene il numero di elementi di lavoro attualmente presenti nel thread pump.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**ProcessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md) | Impostare gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione. Al termine del caricamento e dell'elaborazione di una risorsa o di uno shader, il thread pump lo conterà in una coda fino a quando non viene chiamata questa API, a quel punto gli elementi elaborati verranno impostati sul dispositivo. Ciò è utile per controllare la quantità di elaborazione che viene impiegato per associare le risorse al dispositivo per ogni frame. Vedere la sezione Osservazioni.<br/> |
| [**PurgeAllItems**](id3dx10threadpump-purgeallitems.md)                   | Cancellare tutti gli elementi di lavoro dalla pompa del thread.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**WaitForAllItems**](id3dx10threadpump-waitforallitems.md)               | Attendere il completamento di tutti gli elementi di lavoro nel thread pump.<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

Il thread pump carica ed elabora i dati in un processo in 3 passaggi. Si tratta di:

1.  Caricare e decomprimere i dati con un caricatore dati. L'oggetto caricatore di dati ha tre metodi che il thread pump chiamerà internamente durante il caricamento e la decompressione dei dati: [**ID3DX10DataLoader::Load**](id3dx10dataloader-load.md), [**ID3DX10DataLoader::D ecompress**](id3dx10dataloader-decompress.md)e [**ID3DX10DataLoader::D estroy**](id3dx10dataloader-destroy.md). La funzionalità specifica di queste tre API varia a seconda del tipo di dati caricati e decompressi. L'interfaccia del caricatore di dati può anche essere ereditata e le RELATIVE API possono essere modificate se si carica un file di dati definito nel proprio formato personalizzato.
2.  Elaborare i dati con un processore di dati. L'oggetto processore di dati ha tre metodi che il thread pump chiamerà internamente durante l'elaborazione dei dati: [**ID3DX10DataProcessor::P rocess,**](id3dx10dataprocessor-process.md) [**ID3DX10DataProcessor::CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md)e [**ID3DX10DataProcessor::D estroy**](id3dx10dataprocessor-destroy.md). Il modo in cui elabora i dati sarà diverso a seconda del tipo di dati. Ad esempio, se i dati sono una trama archiviata come JPEG, **ID3DX10DataProcessor::P roces** farà la decompressione JPEG per ottenere i bit di immagine non elaborati dell'immagine. Se i dati sono uno shader, **ID3DX10DataProcessor::P rocess** compilerà HLSL in bytecode. Dopo l'elaborazione dei dati, verrà creato un oggetto dispositivo per i dati (con **ID3DX10DataProcessor::CreateDeviceObject)** e l'oggetto verrà aggiunto a una coda di oggetti dispositivo. L'interfaccia dell'elaboratore di dati può anche essere ereditata e le RELATIVE API possono essere modificate se si elabora un file di dati definito nel proprio formato personalizzato.
3.  Associare l'oggetto dispositivo al dispositivo. Questa operazione viene eseguita quando l'applicazione chiama [**ID3DX10ThreadPump::P rocessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md), che associa al dispositivo un numero specificato di oggetti nella coda di oggetti dispositivo.

Il thread pump può essere usato per caricare i dati in uno dei due modi seguenti: chiamando un'API che accetta un thread pump come parametro, ad esempio [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)o chiamando [**ID3DX10ThreadPump::AddWorkItem**](id3dx10threadpump-addworkitem.md). Nel caso delle API che accettano un thread pump, il caricatore di dati e il processore di dati vengono creati internamente. Nel caso di **AddWorkItem**, il caricatore dati e l'elaboratore dati devono essere creati in anticipo e quindi passati ad AddWorkItem. D3DX10 offre un set di API per la creazione di caricatori di dati e processori di dati con funzionalità per il caricamento e l'elaborazione di formati di dati comuni (vedere le note per l'elenco completo delle API). Per i formati di dati personalizzati, le interfacce del caricatore di dati e dell'elaboratore dati devono essere ereditate e i relativi metodi devono essere ridefinito.

L'oggetto thread pump occupa una notevole quantità di risorse, quindi in genere ne deve essere creata una sola per ogni applicazione.

Caricatori di dati D3DX10 predefiniti



|                                                                           |  Descrizione                                        |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | Creare un caricatore di file in modo asincrono.     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | Creare un caricatore dati in modo asincrono.     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | Creare un caricatore di risorse in modo asincrono. |



 

Processori di dati D3DX10 predefiniti



|                                                                                                 |  Descrizione                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | Creare un processore di dati da usare con una pompa di thread. Questa API è simile a D3DX10CreateAsyncTextureInfoProcessor, ma carica anche la trama. |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | Creare un processore di dati da usare con una pompa di thread.                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | Compilare uno shader e creare un processore di dati in modo asincrono.                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | Creare un effetto con un processore di dati in modo asincrono.                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | Creare un pool di effetti in modo asincrono.                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | Creare un processore di dati in modo asincrono.                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | Creare un processore di dati per uno shader in modo asincrono.                                                                                               |



 

API che accettano un pump di thread come parametro.



|                                                                                                 | Descrizione                                                                 |
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
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | Creare una visualizzazione shader-risorsa da un file.                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | Creare una visualizzazione shader-risorsa da un file in memoria.             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | Creare una visualizzazione shader-risorsa da una risorsa.                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | Recupera informazioni su un file di immagine specificato.                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | Ottenere informazioni su un'immagine già caricata in memoria.       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | Recupera informazioni su una determinata immagine in una risorsa.         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | Creare una risorsa trama da un file.                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | Creare una risorsa trama da un file che risiede nella memoria di sistema. |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | Creare una risorsa trama da un'altra risorsa.                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
