---
title: Interfaccia IDWriteLocalFontFileLoader
description: Implementazione incorporata dell'interfaccia IDWriteFontFileLoader, che opera sui file del tipo di carattere locale ed espone le informazioni sul file di tipo di carattere locale dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Scrittura diretta dell'interfaccia IDWriteLocalFontFileLoader
- Scrittura diretta dell'interfaccia IDWriteLocalFontFileLoader, descritta
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
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329139"
---
# <a name="idwritelocalfontfileloader-interface"></a>Interfaccia IDWriteLocalFontFileLoader

Implementazione incorporata dell'interfaccia [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , che opera sui file del tipo di carattere locale ed espone le informazioni sul file di tipo di carattere locale dalla chiave di riferimento del file del tipo di carattere. I riferimenti ai file del tipo di carattere creati con [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usano questo caricatore di file di tipo

## <a name="members"></a>Membri

L'interfaccia **IDWriteLocalFontFileLoader** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteLocalFontFileLoader** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDWriteLocalFontFileLoader** dispone di questi metodi.



| Metodo                                                                                  | Descrizione                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**GetFilePathFromKey**](idwritelocalfontfileloader-getfilepathfromkey.md)             | Ottiene il percorso del file del tipo di carattere assoluto dalla chiave di riferimento del file del tipo di carattere.<br/>          |
| [**GetFilePathLengthFromKey**](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | Ottiene la lunghezza del percorso del file assoluto dalla chiave di riferimento del file del tipo di carattere.<br/> |
| [**GetLastWriteTimeFromKey**](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | Ottiene l'ora dell'ultima scrittura del file dalla chiave di riferimento del file del tipo di carattere.<br/>      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



 

