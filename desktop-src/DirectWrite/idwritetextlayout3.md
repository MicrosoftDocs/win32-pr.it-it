---
title: Interfaccia IDWriteTextLayout3
description: Rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato. | Interfaccia IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Scrittura diretta dell'interfaccia IDWriteTextLayout3
- Scrittura diretta dell'interfaccia IDWriteTextLayout3, descritta
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
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321695"
---
# <a name="idwritetextlayout3-interface"></a>Interfaccia IDWriteTextLayout3

Rappresenta un blocco di testo dopo che è stato completamente analizzato e formattato.

## <a name="members"></a>Membri

L'interfaccia **IDWriteTextLayout3** eredita da [**IDWriteTextLayout2**](idwritetextlayout2.md). **IDWriteTextLayout3** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDWriteTextLayout3** dispone di questi metodi.



| Metodo                                                          | Descrizione                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)     | Recupera le proprietà di ogni riga.<br/>                                                                                                                                                                                                                        |
| [**GetLineSpacing**](idwritetextlayout3-getlinespacing.md)     | Ottiene le informazioni sulla spaziatura riga.<br/>                                                                                                                                                                                                                            |
| [**InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) | Invalida il layout, forzando il layout da rimisurare prima di chiamare le metriche o le funzioni di disegno. Questa operazione è utile se la località di un tipo di carattere viene modificata e il layout deve essere ridisegnato o se le dimensioni di un client implementate IDWriteInlineObject cambiano. <br/> |
| [**SetLineSpacing**](idwritetextlayout3-setlinespacing.md)     | Imposta spaziatura riga.<br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





