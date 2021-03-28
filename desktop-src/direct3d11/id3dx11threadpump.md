---
title: Interfaccia ID3DX11ThreadPump (D3DX11core. h)
description: Una pompa di thread esegue le attività in modo asincrono.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Interfaccia ID3DX11ThreadPump Direct3D 11
- Interfaccia ID3DX11ThreadPump Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119175"
---
# <a name="id3dx11threadpump-interface"></a>Interfaccia ID3DX11ThreadPump

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Una pompa di thread esegue le attività in modo asincrono. Viene creato chiamando [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md). Sono disponibili diverse API che accettano un thread Pump facoltativo come parametro, ad esempio [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); Se si passa un'interfaccia di thread Pump a queste API, le funzioni vengono eseguite in modo asincrono in un thread separato. In particolare sui computer multiprocessore, una pompa di thread può caricare le risorse ed elaborare i dati senza una riduzione notevole delle prestazioni.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11ThreadPump** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11ThreadPump** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11ThreadPump** dispone di questi metodi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Metodo</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Aggiunge un elemento di lavoro alla pompa di thread.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Ottiene il numero di elementi in ognuna delle tre code all'interno della pompa di thread.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Ottiene il numero di elementi di lavoro nella pompa di thread.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Imposta gli elementi di lavoro sul dispositivo al termine del caricamento e dell'elaborazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Cancella tutti gli elementi di lavoro dalla pompa di thread.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Attende il completamento di tutti gli elementi di lavoro nella pompa di thread.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

### <a name="using-a-thread-pump"></a>Utilizzo di una pompa di thread

Il pump di thread carica ed elabora i dati usando il processo in tre passaggi seguente:

1.  Caricare e decomprimere i dati con un [**caricatore di dati**](id3dx11dataloader.md). L'oggetto caricatore di dati dispone di tre metodi che la pompa di thread chiamerà internamente durante il caricamento e la decompressione dei dati: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D eComPress**](id3dx11dataloader-decompress.md)e [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md). Le funzionalità specifiche di queste tre API variano a seconda del tipo di dati caricati e decompressi. L'interfaccia del caricatore dati può anche essere ereditata e le relative API possono essere modificate se si carica un file di dati definito in un formato personalizzato.
2.  Elaborare i dati con un [**elaboratore di dati**](id3dx11dataprocessor.md). L'oggetto elaboratore di dati dispone di tre metodi che la pompa di thread chiamerà internamente durante l'elaborazione dei dati: [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)e [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md). La modalità di elaborazione dei dati sarà diversa a seconda del tipo di dati. Se, ad esempio, i dati sono una trama archiviata come JPEG, [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) eseguirà la decompressione JPEG per ottenere i bit dell'immagine non elaborata dell'immagine. Se i dati sono uno shader, [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) compilerà il HLSL in bytecode. Dopo che i dati sono stati elaborati, viene creato un oggetto dispositivo per quei dati (con [**ID3DX11DataProcessor:: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) e l'oggetto verrà aggiunto a una coda di oggetti dispositivo. L'interfaccia del processore dati può anche essere ereditata e le relative API possono essere modificate se si sta elaborando un file di dati definito in un formato personalizzato.
3.  Associare l'oggetto dispositivo al dispositivo. Questa operazione viene eseguita quando un'applicazione chiama [**ID3DX11ThreadPump::P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md), che consente di associare al dispositivo un numero specificato di oggetti nella coda degli oggetti dispositivo.

La pompa di thread può essere usata per caricare i dati in uno dei due modi seguenti: chiamando un'API che accetta un thread Pump come parametro, ad esempio [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), oppure chiamando [**ID3DX11ThreadPump:: AddWorkItem**](id3dx11threadpump-addworkitem.md). Nel caso delle API che accettano un thread Pump, il caricatore di dati e il processore di dati vengono creati internamente. Nel caso di AddWorkItem, il caricatore di dati e il processore di dati devono essere creati in anticipo e vengono quindi passati in AddWorkItem. D3DX11 fornisce un set di API per la creazione di caricatori di dati e processori di dati con funzionalità per il caricamento e l'elaborazione di formati di dati comuni. Per i formati di dati personalizzati, le interfacce del caricatore di dati e del processore di dati devono essere ereditate e i relativi metodi devono essere ridefiniti.

L'oggetto della pompa di thread occupa una quantità sostanziale di risorse, quindi in genere è necessario crearne solo una per ogni applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

