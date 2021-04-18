---
title: Elemento color
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento color
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Finestra elementi colori Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331763"
---
# <a name="color-element"></a>Elemento color

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento color specifica il colore di sfondo per i pulsanti di spostamento online, il testo del pulsante e la barra delle applicazioni delle funzionalità.

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (obbligatorio)
</dt> <dd>

Valore di colore RGB esadecimale. Specifica il colore di sfondo per i pulsanti e la barra delle applicazioni.

</dd> <dt>

<span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (obbligatorio)
</dt> <dd>

Valore di colore RGB esadecimale. Specifica il colore per il testo del pulsante.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

Il valore predefinito per **MediaPlayer** è \# 7C9AD6. Il valore predefinito per **MediaPlayerText** è \# FFFFFF.

Assicurarsi di usare i colori che semplificano la lettura del testo del pulsante da parte dell'utente. Ad esempio, è consigliabile evitare di usare il testo del pulsante bianco sui pulsanti di colore chiaro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





