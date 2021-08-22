---
title: AmbientAttributes.alphaBlend
description: L'attributo alphaBlend specifica o recupera un valore per la fusione alfa di qualsiasi widget VIEW, SUBVIEW o UI.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- AmbientAttributes.alphaBlend Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b7170931c8fc266fdc335076dbc6dc687795f9bb432518b62a39d1f610b601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391711"
---
# <a name="ambientattributesalphablend"></a>AmbientAttributes.alphaBlend

**L'attributo alphaBlend** specifica o recupera un valore per la fusione alfa di qualsiasi widget **VIEW,** **SUBVIEW** o UI.

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero di lettura/scrittura **(** **long**) con un valore compreso tra 0 (nessuna opacità) e 255 (opacità completa) e un valore predefinito di 255.

## <a name="remarks"></a>Commenti

Questo attributo consente a un elemento di apparire semitrasparente, a seconda della quantità di opacità impostata. Minore è l'opacità, più trasparente sarà l'elemento. Ogni elemento dell'interfaccia può avere un valore di opacità separato, ad eccezione degli elementi pulsante in un **controllo BUTTONGROUP.** Quando **alphaBlend è** impostato in **VIEW,** verrà impostata l'opacità dell'intera interfaccia. La fusione alfa non funziona per i controlli finestra, tra cui **PLAYLIST,** **EFFECTS,** **LISTBOX,** **POPUP,** **EDITBOX** e **VIDEO** (se **windowless** è impostato su false). Quando **alphaBlend è** impostato su **VIEW,** l'intera interfaccia diventa trasparente. Gli **attributi transparencyColor** usati da diversi elementi non sono supportati con **alphaBlend.**

Quando si usa **alphaBlend** con un elemento **TEXT** per cui non è specificato **backgroundColor,** verrà usato un colore di sfondo nero. Se anche il colore di primo piano è nero ,ovvero il valore predefinito per *TEXT.***foregroundColor**), il testo potrebbe diventare illeggibile. Per evitare questo problema, specificare sempre **l'attributo backgroundColor** o impostare **foregroundColor** su un colore diverso dal nero.

> [!Note]  
> Questo attributo non è supportato in Windows 98.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT.foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





