---
title: VIDEO. zoom
description: L'attributo zoom specifica la percentuale in base alla quale ridimensionare il video.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VIDEO. Zoom Media Player Windows
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324080"
---
# <a name="videozoom"></a>VIDEO. zoom

L'attributo **Zoom** specifica la percentuale in base alla quale ridimensionare il video.

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**Long**) compreso tra 1 e le dimensioni massime consentite dalla larghezza e dall'altezza del controllo video. Il valore predefinito è 100.

## <a name="remarks"></a>Commenti

Questo attributo non può essere usato in combinazione con l'attributo **FullScreen** .

Se si specifica **Width** e **Height** e la finestra video risultante è più grande del video riprodotto, è possibile aumentare le dimensioni del video scalando fino alla dimensione massima consentita dalla finestra. Se non si specifica **Width** e **Height** , **lo zoom** è limitato ai valori di 100 o meno.

Se la proprietà **shrinkToFit** è impostata su false, il video verrà modificato proporzionalmente allo zoom, per adattarsi allo spazio disponibile. Se **shrinkToFit** è true, il video verrà compattato per adattarsi alla dimensione più restrittiva, mantenendo le proporzioni originali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> <dt>

[**VIDEO. fullScreen**](video-fullscreen.md)
</dt> <dt>

[**VIDEO. shrinkToFit**](video-shrinktofit.md)
</dt> </dl>

 

 





