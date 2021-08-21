---
title: Elemento HTMLView
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. L'elemento HTMLView specifica l'URL di base di una pagina Web HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Elemento HTMLView Windows Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 703668427757df19675734e1503296a8a7144517801d0e8fdc0fadb25a16b0a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054889"
---
# <a name="htmlview-element"></a>Elemento HTMLView

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'elemento HTMLView** specifica l'URL di base di una pagina Web HTMLView.

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obbligatorio)
</dt> <dd>

URL di base per la pagina Web HTMLView Windows Media Player visualizzata.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

È possibile usare questo elemento per integrare la funzionalità HTMLView con il negozio online. Se il dominio dell'URL specificato dal negozio online corrente corrisponde a  quello della pagina Web HTMLView, il passaggio a In riproduzione avviene senza l'intervento dell'utente e viene visualizzato il contenuto HTMLView. In caso contrario, Windows Media Player all'utente l'autorizzazione per visualizzare il contenuto HTMLView.

Ad esempio, se l'URL per la pagina Web HTMLView è e l'URL per l'attributo BaseURL è specificato come , la pagina Web HTMLView viene visualizzata senza chiedere conferma https://www.proseware.com/html/HTMLView.htm  https://www.proseware.com all'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





