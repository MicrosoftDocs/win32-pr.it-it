---
title: Elemento DownloadStatus (msfeeds. h)
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento DownloadStatus (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Finestra elementi DownloadStatus Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329323"
---
# <a name="downloadstatus-element"></a>Elemento DownloadStatus

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **downloadStatus** specifica un URL visualizzato da Windows Media Player come collegamento per consentire agli utenti di visualizzare lo stato del download.

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="URL"></span><span id="url"></span>URL
</dt> <dd>

URL della pagina Web visualizzata dal negozio online per mostrare lo stato di download all'utente.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

Windows Media Player visualizza un messaggio agli utenti quando è in corso un download. Se i servizi attivi correnti definiscono un URL di stato di download, l'utente può fare clic sul testo del messaggio. Quando l'utente fa clic sul messaggio, il lettore passa all'URL specificato dall'elemento **downloadStatus** in modo che l'archivio attivo corrente possa fornire informazioni dettagliate sui download in corso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/>                                          |
| Intestazione<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





