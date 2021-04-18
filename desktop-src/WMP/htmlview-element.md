---
title: Elemento HTMLView
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento HTMLView specifica l'URL di base di una pagina Web HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Finestra elementi HTMLView Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327876"
---
# <a name="htmlview-element"></a>Elemento HTMLView

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **HtmlView** specifica l'URL di base di una pagina Web htmlview.

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseUrl** (obbligatorio)
</dt> <dd>

URL di base per la pagina Web HTMLView visualizzata da Windows Media Player.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

È possibile usare questo elemento per integrare la funzionalità HTMLView con il negozio online. Se il dominio dell'URL specificato dall'archivio online corrente corrisponde a quello per la pagina Web HTMLView, l'opzione per la **riproduzione** avviene senza l'intervento dell'utente e viene visualizzato il contenuto di htmlview. In caso contrario, Windows Media Player chiede all'utente l'autorizzazione per visualizzare il contenuto di HTMLView.

Ad esempio, se l'URL per la pagina Web HTMLView è https://www.proseware.com/html/HTMLView.htm e l'URL per l'attributo **BaseUrl** è specificato come https://www.proseware.com , viene visualizzata la pagina Web HtmlView senza richiedere conferma all'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**PARAM (elemento)**](param-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





