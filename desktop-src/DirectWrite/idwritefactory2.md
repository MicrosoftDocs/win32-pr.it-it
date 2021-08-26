---
title: Interfaccia IDWriteFactory2
description: Interfaccia factory radice per tutti DirectWrite oggetti .
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Interfaccia IDWriteFactory1 Direct Write
- Interfaccia IDWriteFactory1 Direct Write , descritta
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370292387f2c42e3f749e24a063e05bb24280ec5c8e8941a430f996fe7f349da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902801"
---
# <a name="idwritefactory2-interface"></a>Interfaccia IDWriteFactory2

Interfaccia factory radice per [tutti](direct-write-portal.md) DirectWrite oggetti.

## <a name="members"></a>Membri

**L'interfaccia IDWriteFactory1** eredita da [**IDWriteFactory1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) **IDWriteFactory2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDWriteFactory1** include questi metodi.



| Metodo                                                                             | Descrizione                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CreateCustomRenderingParams**](idwritefactory2-createcustomrenderingparams.md) | Crea un oggetto parametri di rendering con le proprietà specificate.<br/>                            |
| [**CreateFontFallbackBuilder**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | Crea un oggetto generatore di fallback dei tipi di carattere.<br/>                                                         |
| [**CreateGlyphRunAnalysis**](idwritefactory2-createglyphrunanalysis.md)           | Crea un oggetto di analisi dell'esecuzione del glifo, che incapsula le informazioni usate per eseguire il rendering di un'esecuzione di glifi.<br/> |
| [**GetSystemFontFallback**](idwritefactory2-getsystemfontfallback.md)             | Crea un oggetto di fallback del tipo di carattere dall'elenco di fallback dei tipi di carattere di sistema.<br/>                              |
| [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | Questo metodo viene chiamato su un'esecuzione di glifi per tradurlo in più esecuzioni di glifi a colori.<br/>           |



 

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

[**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

