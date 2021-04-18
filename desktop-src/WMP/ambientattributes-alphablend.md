---
title: AmbientAttributes. alphaBlend
description: L'attributo alphaBlend specifica o recupera un valore per la fusione alfa di qualsiasi visualizzazione, sottovista o widget dell'interfaccia utente.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- Media Player Windows AmbientAttributes. alphaBlend
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331411"
---
# <a name="ambientattributesalphablend"></a>AmbientAttributes. alphaBlend

L'attributo **alphaBlend** specifica o recupera un valore per la fusione alfa di qualsiasi **visualizzazione**, **sottovista** o widget dell'interfaccia utente.

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**Long**) con un valore compreso tra 0 (nessuna opacità) e 255 (opacità completa) e un valore predefinito pari a 255.

## <a name="remarks"></a>Commenti

Questo attributo consente la visualizzazione di un elemento semitrasparente, a seconda della quantità di set di opacità. Meno opacità, più trasparente verrà visualizzato l'elemento. Ogni elemento nell'interfaccia può avere un valore di opacità separato, ad eccezione degli elementi Button in un controllo **ButtonGroup** . Quando **alphaBlend** è impostato in **visualizzazione**, viene impostata l'opacità dell'intera interfaccia. Alpha Blend non funzionerà per i controlli finestra, tra cui **playlist**, **Effects**, **ListBox**, **popup**, **casella** e **video** (se la **finestra** è impostata su false). Quando **alphaBlend** è impostato su **View**, l'intera interfaccia diventa trasparente. Gli attributi **transparencyColor** usati da diversi elementi non sono supportati con **alphaBlend**.

Quando si usa **alphaBlend** con un elemento di **testo** che non ha il valore **BackgroundColor** specificato, verrà usato un colore di sfondo nero. Se il colore di primo piano è anche nero (ovvero il valore predefinito per il *testo*.**foregroundColor**), il testo potrebbe diventare illeggibile. Per evitare questo problema, specificare sempre l'attributo **BackgroundColor** o impostare **ForegroundColor** su un colore diverso dal nero.

> [!Note]  
> Questo attributo non è supportato in Windows 98.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TESTO. backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TESTO. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





