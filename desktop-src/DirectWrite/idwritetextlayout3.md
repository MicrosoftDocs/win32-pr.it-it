---
title: Interfaccia IDWriteTextLayout3
description: Rappresenta un blocco di testo dopo che è stato analizzato e formattato completamente. | Interfaccia IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Interfaccia IDWriteTextLayout3 Direct Write
- Interfaccia IDWriteTextLayout3 Direct Write , descritta
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f3a6d441c3f7d8ac9bf356bd835f800e026f8c6e27cb083a57ced571ba68fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070651"
---
# <a name="idwritetextlayout3-interface"></a>Interfaccia IDWriteTextLayout3

Rappresenta un blocco di testo dopo che è stato analizzato e formattato completamente.

## <a name="members"></a>Membri

**L'interfaccia IDWriteTextLayout3** eredita da [**IDWriteTextLayout2.**](idwritetextlayout2.md) **IDWriteTextLayout3** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDWriteTextLayout3** include questi metodi.



| Metodo                                                          | Descrizione                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)     | Recupera le proprietà di ogni riga.<br/>                                                                                                                                                                                                                        |
| [**GetLineSpacing**](idwritetextlayout3-getlinespacing.md)     | Ottiene informazioni sull'interlinea.<br/>                                                                                                                                                                                                                            |
| [**InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) | Invalida il layout, forzando la ricorsione del layout prima di chiamare le funzioni di metrica o disegno. Ciò è utile se la localizzazione di un tipo di carattere cambia e il layout deve essere ridisegnato o se le dimensioni di un idWriteInlineObject implementato dal client cambiano. <br/> |
| [**SetLineSpacing**](idwritetextlayout3-setlinespacing.md)     | Impostare l'interlinea.<br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





