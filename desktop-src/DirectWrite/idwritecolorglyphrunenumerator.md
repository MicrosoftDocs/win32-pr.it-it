---
title: Interfaccia IDWriteColorGlyphRunEnumerator
description: Questa interfaccia consente all'applicazione di enumerare tramite le esecuzioni del glifo del colore.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Interfaccia IDWriteColorGlyphRunEnumerator Direct Write
- INTERFACCIA IDWriteColorGlyphRunEnumerator Direct Write , descritta
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
ms.openlocfilehash: 8fa665f7000ffaada5bc14f97671fb6e52266c712ef6081b956184653d1f1c95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536141"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a>Interfaccia IDWriteColorGlyphRunEnumerator

Questa interfaccia consente all'applicazione di enumerare tramite le esecuzioni del glifo del colore. L'enumeratore enumera i livelli in ordine inverso a quello frontale per la strattura appropriata.

## <a name="members"></a>Membri

**L'interfaccia IDWriteColorGlyphRunEnumerator** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDWriteColorGlyphRunEnumerator** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDWriteColorGlyphRunEnumerator** include questi metodi.



| Metodo                                                                | Descrizione                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [**GetCurrentRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | Restituisce l'esecuzione del glifo corrente dell'enumeratore.<br/> |
| [**MoveNext**](idwritecolorglyphrunenumerator-movenext.md)           | Passare all'esecuzione successiva del glifo nell'enumeratore.<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

