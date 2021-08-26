---
title: Interfaccia IDWriteLocalFontFileLoader
description: Implementazione predefinita dell'interfaccia IDWriteFontFileLoader, che opera sui file dei tipi di carattere locali ed espone le informazioni sul file del tipo di carattere locale dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Interfaccia IDWriteLocalFontFileLoader Direct Write
- INTERFACCIA IDWriteLocalFontFileLoader Direct Write , descritta
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa073b0d39e5dfbcdb90f2cd67db5f09a04e21c3e36790d4d841e5719490c753
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048691"
---
# <a name="idwritelocalfontfileloader-interface"></a>Interfaccia IDWriteLocalFontFileLoader

Implementazione predefinita dell'interfaccia [**IDWriteFontFileLoader,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) che opera sui file dei tipi di carattere locali ed espone le informazioni sul file del tipo di carattere locale dalla chiave di riferimento del file del tipo di carattere. I riferimenti ai file dei tipi di carattere creati [**con CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usano questo caricatore di file di tipi di carattere.

## <a name="members"></a>Membri

**L'interfaccia IDWriteLocalFontFileLoader** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDWriteLocalFontFileLoader** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDWriteLocalFontFileLoader** include questi metodi.



| Metodo                                                                                  | Descrizione                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**GetFilePathFromKey**](idwritelocalfontfileloader-getfilepathfromkey.md)             | Ottiene il percorso assoluto del file del tipo di carattere dalla chiave di riferimento del file del tipo di carattere.<br/>          |
| [**GetFilePathLengthFromKey**](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | Ottiene la lunghezza del percorso assoluto del file dalla chiave di riferimento del file del tipo di carattere.<br/> |
| [**GetLastWriteTimeFromKey**](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | Ottiene l'ora dell'ultima scrittura del file dalla chiave di riferimento del file del tipo di carattere.<br/>      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



 

