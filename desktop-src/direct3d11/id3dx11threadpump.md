---
title: Interfaccia ID3DX11ThreadPump (D3DX11core.h)
description: Un thread pump esegue le attività in modo asincrono.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Interfaccia ID3DX11ThreadPump Direct3D 11
- ID3DX11ThreadPump interface Direct3D 11 , descritto
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
ms.openlocfilehash: 9b4bcfbc5fcf128f3ef71250180b487c83ce3c0d5430a563dfa3b7069e4235e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858041"
---
# <a name="id3dx11threadpump-interface"></a>Interfaccia ID3DX11ThreadPump

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Un thread pump esegue le attività in modo asincrono. Viene creato chiamando [**D3DX11CreateThreadPump.**](d3dx11createthreadpump.md) Esistono diverse API che accettano un thread pump facoltativo come parametro, ad esempio [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); Se si passa un'interfaccia pump di thread in queste API, le funzioni verranno eseguite in modo asincrono in un thread separato. In particolare nei computer multiprocessore, una pompa di thread può caricare le risorse ed elaborare i dati senza una notevole riduzione delle prestazioni.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11ThreadPump** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11ThreadPump** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11ThreadPump** include questi metodi.



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
<br/> Aggiunge un elemento di lavoro alla pompa del thread.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Ottiene il numero di elementi in ognuna delle tre code all'interno del thread pump.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Ottiene il numero di elementi di lavoro nel thread pump.<br/></td>
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
<br/> Cancella tutti gli elementi di lavoro dalla pompa del thread.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Attende il completamento di tutti gli elementi di lavoro nel thread pump.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

### <a name="using-a-thread-pump"></a>Uso di un thread pump

Il thread pump carica ed elabora i dati usando il processo in tre passaggi seguente:

1.  Caricare e decomprimere i dati con un [**caricatore dati**](id3dx11dataloader.md). L'oggetto caricatore di dati ha tre metodi che il thread pump chiamerà internamente durante il caricamento e la decompressione dei dati: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D ecompress**](id3dx11dataloader-decompress.md)e [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md). La funzionalità specifica di queste tre API varia a seconda del tipo di dati caricati e decompressi. L'interfaccia del caricatore di dati può anche essere ereditata e le RELATIVE API possono essere modificate se si carica un file di dati definito nel proprio formato personalizzato.
2.  Elaborare i dati con un [**processore di dati**](id3dx11dataprocessor.md). L'oggetto processore di dati ha tre metodi che il thread pump chiamerà internamente durante l'elaborazione dei dati: [**ID3DX11DataProcessor::P rocess,**](id3dx11dataprocessor-process.md) [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)e [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md). Il modo in cui elabora i dati sarà diverso a seconda del tipo di dati. Ad esempio, se i dati sono una trama archiviata come JPEG, [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) farà la decompressione JPEG per ottenere i bit di immagine non elaborati dell'immagine. Se i dati sono uno shader, [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) compilerà HLSL in bytecode. Dopo l'elaborazione dei dati, verrà creato un oggetto dispositivo per i dati (con [**ID3DX11DataProcessor::CreateDeviceObject)**](id3dx11dataprocessor-createdeviceobject.md)e l'oggetto verrà aggiunto a una coda di oggetti dispositivo. L'interfaccia dell'elaboratore di dati può anche essere ereditata e le RELATIVE API possono essere modificate se si elabora un file di dati definito nel proprio formato personalizzato.
3.  Associare l'oggetto dispositivo al dispositivo. Questa operazione viene eseguita quando l'applicazione chiama [**ID3DX11ThreadPump::P rocessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md), che associa al dispositivo un numero specificato di oggetti nella coda di oggetti dispositivo.

Il thread pump può essere usato per caricare i dati in uno dei due modi seguenti: chiamando un'API che accetta un thread pump come parametro, ad esempio [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md)o chiamando [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md). Nel caso delle API che accettano un thread pump, il caricatore di dati e il processore di dati vengono creati internamente. Nel caso di AddWorkItem, il caricatore dati e l'elaboratore dati devono essere creati in anticipo e quindi passati ad AddWorkItem. D3DX11 offre un set di API per la creazione di caricatori di dati e processori di dati con funzionalità per il caricamento e l'elaborazione di formati di dati comuni. Per i formati di dati personalizzati, le interfacce del caricatore di dati e dell'elaboratore dati devono essere ereditate e i relativi metodi devono essere ridefinito.

L'oggetto thread pump occupa una notevole quantità di risorse, quindi in genere ne deve essere creata una sola per ogni applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>D3DX11core.h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

