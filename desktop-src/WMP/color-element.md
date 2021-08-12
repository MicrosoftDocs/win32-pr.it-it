---
title: Elemento Color
description: Nota In questa sezione vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. | Elemento Color
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Elemento Color Windows Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8576f94c2d1aa88608f8f40cbfe32c2d1dc315e0e4578ca6554fa5fcde82c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580756"
---
# <a name="color-element"></a>Elemento Color

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

L'elemento Color specifica il colore di sfondo per i pulsanti di spostamento del negozio online, il testo del pulsante e la barra delle applicazioni Funzionalità.

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

Assicurarsi di usare colori che semplificano la lettura del testo del pulsante da parte dell'utente. Ad esempio, è consigliabile evitare di usare il testo del pulsante bianco sui pulsanti colorati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





