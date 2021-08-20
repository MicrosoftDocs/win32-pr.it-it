---
title: Elemento Image (WMP SDK)
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. | Elemento Image (WMP SDK)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Elemento Image Windows Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9815844833c8068fb89589368f29b15787ad8fb18a21c9f9c6867d202e3095a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862641"
---
# <a name="image-element-wmp-sdk"></a>Elemento Image (WMP SDK)

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'elemento Image** specifica le immagini Windows Media Player all'utente per rappresentare il negozio online.

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (obbligatorio per gli archivi di tipo 1, ignorato per il tipo 2)
</dt> <dd>

URL per il logo visualizzato Windows Media Player nella finestra di dialogo del contratto di licenza con l'utente finale. Deve trattarsi di un'immagine PNG di 80 x 80 pixel.

</dd> <dt>

<span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (facoltativo)
</dt> <dd>

URL dell'immagine Windows Media Player nel menu dei servizi. Questa immagine deve essere di 15 x 15 pixel.

</dd> <dt>

<span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (facoltativo)
</dt> <dd>

Per un negozio online di tipo 1, si tratta dell'URL dell'immagine Windows Media Player visualizzata nella **scheda Negozi** online. Per Windows Media Player 11, questa immagine deve avere una larghezza di 45 pixel per 13 pixel di altezza. Per Windows Media Player 12, questa immagine deve avere una larghezza di 45 pixel per 30 pixel di altezza. Per supportare entrambe le versioni 11 e 12 di Windows Media Player, è necessario fornire due documenti ServiceInfo.xml separati, ognuno dei quali punta all'immagine di dimensioni appropriate per ServiceLargeURL.

Per un negozio online di tipo 2, si tratta dell'URL dell'immagine visualizzata Windows Media Player accanto alla scheda **Negozi** online o accanto ai pulsanti del riquadro attività. Questa immagine deve essere di 30 x 30 pixel.

</dd> <dt>

<span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (facoltativo)
</dt> <dd>

URL del logo visualizzato insieme alla descrizione del marketing specificata **nell'elemento Description.** Se non viene fornito, sarà vuoto. (Tutti i tipi, facoltativo) Deve trattarsi di un'immagine PNG di 45 pixel di larghezza e 13 pixel di altezza.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

I formati di immagine supportati .gif, .jpg, .bmp e .png (che è il formato consigliato). L'uso della trasparenza Web è supportato e consigliato. I file GIF animati non sono supportati.

Se non si specifica un valore per **MenuURL,** Windows Media Player non visualizza alcun elemento grafico nel menu per il negozio online.

È possibile fornire un'immagine animata per ServiceLargeURL. In Windows Media Player 10 o 11, l'immagine viene animata. Nella Windows Media Player 12 viene visualizzato solo il primo frame dell'immagine. Per fornire un'immagine animata, creare un singolo file di immagine contenente fotogrammi successivi dell'animazione. Ad esempio, per un'immagine di 30 pixel di larghezza e 30 pixel di altezza, è possibile fornire 20 immagini successive affiancate in un'immagine di 600 pixel di larghezza e 30 pixel di altezza. Windows Media Player animare automaticamente un'immagine di questo tipo visualizzando le 20 singole immagini una dopo l'altra. Questa animazione si verifica una sola volta all'apertura del negozio online. non si ripete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





