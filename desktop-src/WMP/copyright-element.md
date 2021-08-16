---
title: Elemento COPYRIGHT (Msfeeds.h)
description: L'elemento COPYRIGHT definisce una stringa di testo che specifica le informazioni sul copyright per un elemento ASX o ENTRY.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Elemento COPYRIGHT Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5a01e97364aa47182e38e3e3066895c771e2d5edb6c480e8108cb168e7f8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997461"
---
# <a name="copyright-element"></a>Elemento COPYRIGHT

**L'elemento COPYRIGHT** definisce una stringa di testo che specifica le informazioni sul copyright per **un elemento ASX** **o ENTRY.**

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **ASX**, **ENTRY** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento definisce una stringa di testo che specifica le informazioni sul copyright per **un elemento ASX** **o ENTRY.**

Quando questo elemento viene visualizzato all'interno **di un elemento ASX,** la stringa di copyright viene visualizzata solo come **Mostra** informazioni. Quando questo elemento viene visualizzato all'interno di **un elemento ENTRY,** il testo viene visualizzato come informazioni sul clip. Ogni elemento **ASX e** **ENTRY** padre deve contenere al massimo un elemento **COPYRIGHT** figlio. Più **elementi COPYRIGHT** dopo il primo verranno ignorati e non verranno visualizzati.

I caratteri per i simboli di registrazione del copyright e del marchio ( o ) potrebbero non essere visualizzati correttamente se il metafile non è codificato usando lo schema di codifica UTF-8. In questo caso, per visualizzare correttamente uno di questi simboli per tutti gli utenti, è possibile usare gli equivalenti ASCII (c) e (R).

Se il metafile viene codificato usando UTF-8, i simboli di copyright e marchio verranno visualizzati correttamente.

## <a name="examples"></a>Esempio


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/>                                 |
| Intestazione<br/>  | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di caratteri di copyright ai metafile**](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





