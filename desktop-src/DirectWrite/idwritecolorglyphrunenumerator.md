---
title: Interfaccia IDWriteColorGlyphRunEnumerator
description: Questa interfaccia consente all'applicazione di enumerare le esecuzioni del glifo dei colori.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Scrittura diretta dell'interfaccia IDWriteColorGlyphRunEnumerator
- Scrittura diretta dell'interfaccia IDWriteColorGlyphRunEnumerator, descritta
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742239"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a>Interfaccia IDWriteColorGlyphRunEnumerator

Questa interfaccia consente all'applicazione di enumerare le esecuzioni del glifo dei colori. L'enumeratore enumera i livelli in un ordine di ritorno all'inizio per i livelli appropriati.

## <a name="members"></a>Membri

L'interfaccia **IDWriteColorGlyphRunEnumerator** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteColorGlyphRunEnumerator** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDWriteColorGlyphRunEnumerator** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [**GetCurrentRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | Restituisce l'esecuzione del glifo corrente dell'enumeratore.<br/> |
| [**MoveNext**](idwritecolorglyphrunenumerator-movenext.md)           | Passare al glifo successivo eseguito nell'enumeratore.<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

