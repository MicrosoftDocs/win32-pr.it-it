---
title: Elemento Image (WMP SDK)
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento Image (WMP SDK)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Finestra elemento immagine Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330893"
---
# <a name="image-element-wmp-sdk"></a>Elemento Image (WMP SDK)

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **Image** specifica le immagini che Windows Media Player visualizza all'utente per rappresentare l'archivio online.

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

URL del logo visualizzato da Windows Media Player nella finestra di dialogo contratto di licenza con l'utente finale (EULA). Deve essere un'immagine PNG di 80 x 80 pixel.

</dd> <dt>

<span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (facoltativo)
</dt> <dd>

URL dell'immagine visualizzata da Windows Media Player nel menu servizi. Questa immagine deve essere di 15 x 15 pixel.

</dd> <dt>

<span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (facoltativo)
</dt> <dd>

Per un archivio online di tipo 1, questo è l'URL dell'immagine visualizzata da Windows Media Player nella scheda **Store online** . Per Windows Media Player 11, questa immagine deve essere di 45 pixel di larghezza per 13 pixel di altezza. Per Windows Media Player 12, questa immagine deve essere di 45 pixel di larghezza per 30 pixel di altezza. Per supportare entrambe le versioni 11 e 12 di Windows Media Player, è necessario fornire due documenti ServiceInfo.xml distinti, ognuno dei quali fa riferimento all'immagine di dimensioni appropriate per ServiceLargeURL.

Per un archivio di tipo 2 online, questo è l'URL dell'immagine visualizzata da Windows Media Player accanto alla scheda **Store online** o accanto ai pulsanti del riquadro attività. Questa immagine deve essere di 30 x 30 pixel.

</dd> <dt>

<span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (facoltativo)
</dt> <dd>

URL per il logo visualizzato insieme alla descrizione di marketing specificata nell'elemento **Description** . Se non viene specificato, sarà vuoto. (Tutti i tipi, facoltativo) Deve essere un'immagine PNG di 45 pixel di larghezza e 13 pixel di altezza.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

I formati di immagine supportati sono. gif,. jpg,. bmp e. png (il formato consigliato). L'uso della trasparenza web è supportato e consigliato. I file GIF animati non sono supportati.

Se non si specifica un valore per **MenuURL**, Windows Media Player non visualizza alcun grafico nel menu per il negozio online.

È possibile specificare un'immagine animata per ServiceLargeURL. In Windows Media Player 10 o 11, l'immagine viene animata. In Windows Media Player 12, viene visualizzato solo il primo frame dell'immagine. Per fornire un'immagine animata, creare un singolo file di immagine che contiene i frame successivi dell'animazione. Ad esempio, per un'immagine con una larghezza di 30 pixel e 30 pixel di altezza, è possibile fornire 20 immagini successive affiancate in un'immagine di 600 pixel di larghezza e 30 pixel di altezza. Windows Media Player eseguirà automaticamente l'animazione di tale immagine mostrando 20 immagini singole una dopo l'altra. Questa animazione viene eseguita una sola volta quando si apre l'archivio online; non si ripete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





